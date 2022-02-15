---
title: JavaScript-Code für [!DNL Analytics for Advertising Cloud]
description: JavaScript-Code für [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 184508ce-df8d-4fa0-b22b-ca0546a61d58
source-git-commit: ac7f6110a523d63482f6c2e1a7d0bd5a12a0bab1
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---

# JavaScript-Code für [!DNL Analytics for Advertising Cloud]

*Werbetreibende, die nur über eine Advertising Cloud-Adobe Analytics-Integration verfügen*

*Advertiser nur mit Advertising Cloud DSP*

Bei Advertising Cloud DSP wird die Variable [!DNL Analytics for Advertising Cloud] -Integration verfolgt Durchsichts- und Clickthrough-Site-Interaktionen. Clickthrough-Besuche werden anhand des standardmäßigen Adobe Analytics-Codes auf Ihren Webseiten verfolgt. die [!DNL Analytics] -Code erfasst die AMO-ID- und EF-ID-Parameter in der URL der Landingpage und verfolgt sie in ihren jeweiligen reservierten eVars. Sie können Durchsichtsbesuche verfolgen, indem Sie ein JavaScript-Snippet in Ihren Webseiten bereitstellen.

Beim ersten Seitenaufruf eines Site-Besuchs prüft der Advertising Cloud-JavaScript-Code, ob der Besucher zuvor eine Anzeige gesehen oder angeklickt hat. Wenn der Benutzer zuvor über einen Clickthrough auf die Site gelangt ist oder noch keine Anzeige gesehen hat, wird der Besucher ignoriert. Wenn der Besucher eine Anzeige gesehen hat und nicht über einen Clickthrough während der [Klick-Lookback-Fenster](/help/integrations/analytics/prerequisites.md#lookback-a4adc) in Advertising Cloud festgelegt ist, verwendet der Advertising Cloud-JavaScript-Code entweder a) die [Experience Cloud-ID-Dienst](https://experienceleague.adobe.com/docs/id-service/using/home.html) zur Generierung einer zusätzlichen Kennung (`SDID`) oder b) verwendet die Adobe Experience Platform [!DNL Web SDK] `generateRandomID` -Methode zur Generierung einer `[!DNL StitchID]`. Jede ID wird verwendet, um Daten aus Advertising Cloud dem Adobe Analytics-Treffer des Besuchers zuzuordnen. Adobe Analytics fragt dann Advertising Cloud nach der AMO-ID und der EF-ID ab, die mit der Anzeigenbelichtung verknüpft sind. Die AMO-ID und EF-IDs werden dann in ihre jeweiligen eVars eingefügt. Diese Werte bleiben für einen bestimmten Zeitraum bestehen (standardmäßig 60 Tage).

[!DNL Analytics] sendet Site-Traffic-Metriken (z. B. Seitenansichten, Besuche und Besuchszeit) und [!DNL Analytics] benutzerspezifische oder standardmäßige Ereignisse stündlich an Advertising Cloud übermitteln, wobei die EF ID als Schlüssel verwendet wird. Diese [!DNL Analytics] Metriken werden dann über das Advertising Cloud-Attributionssystem ausgeführt, um die Konversionen mit dem Klick- und Belichtungsverlauf zu verbinden.

>[!NOTE]
>
>Die JavaScript-Tracking-Logik von Advertising Cloud tritt auf der Adobe auf und hat daher praktisch keine Auswirkungen auf die Seitenladezeit.
>
>Im Gegensatz dazu wird die Logik für die [!DNL DCM] Data Connector zu [!DNL Analytics] (mithilfe von [!DNL Google Campaign Manager 360]) für Advertising Cloud DSP auf Client-Seite. Die clientseitige Zuordnung verlangsamt das Laden der Seite und erhöht das Risiko eines Datenverlusts. Dies liegt daran, dass [!DNL Analytics] JavaScript muss ping [!DNL DoubleClick] und warten auf [!DNL DoubleClick] , um die letzten Klick-/Impressionsdaten an [!DNL Analytics]. Wenn [!DNL DSP] setzt [!DNL DCM] Data Connector angeben, wie lange Sie die Seite verzögern möchten.

## Bereitstellen des JavaScript-Codes

Die JavaScript-Bibliothek besteht aus zwei Zeilen, die [!DNL Analytics] und Advertising Cloud zu kommunizieren. Wenn die Variable [!DNL Analytics for Advertising Cloud] -Integration während der Advertising Cloud-Implementierung abgeschlossen wurde, sollten Sie diesen Code bereits mit Anweisungen zur Bereitstellung erhalten haben.

### Der Code

#### Implementierungen, die den Experience Cloud Identity-Dienst verwenden `visitorAPI.js` code

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

#### Implementierungen, die die Experience Platform verwenden [!DNL Web SDK] `alloy.js`code

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

### Speicherort des Codes

Die [!DNL Analytics for Advertising Cloud] Die JavaScript-Funktion muss nach dem Experience Cloud-ID-Dienst, jedoch vor Ihrem Analytics-App-Measurement-Code stehen, damit die zusätzliche ID (`SDID`) oder `[!DNL StitchID]` kann in Ihrem Analytics-Aufruf enthalten sein.

![Codeplatzierung](/help/integrations/assets/a4adc-code-placement.png)

### Validieren der Codebereitstellung

Sie können eine Validierung mit einem beliebigen Paket-Sniffer-Tool durchführen (z. B. [!DNL Charles], [!DNL Fiddler]oder [!DNL Chrome Developer Tools]), indem die Werte der vier IDs zwischen der Anfrage an Advertising Cloud und der Anfrage, die an gesendet wird, verglichen werden [!DNL Analytics], wie unten beschrieben.

#### So bestätigen Sie den Code mit [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Öffnen [!DNL Chrome Developer Tools] und klicken Sie auf **Netzwerk** Registerkarte.

1. Laden einer Website-Seite, die die Variable [!DNL Analytics for Advertising Cloud] JavaScript.

1. Filtern Sie die [!UICONTROL Network] tab by `last` und überprüfen Sie zwei Zeilen:

   ![Letzte Filterung](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * Die erste Zeile ist der Aufruf der JavaScript-Bibliothek mit dem Titel `last-event-tag-latest.min.js`.
   * Die zweite Zeile ist der Aufruf, der die Anfrage an Advertising Cloud sendet. Er beginnt wie folgt: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      Wenn Sie den Aufruf an Advertising Cloud nicht sehen, ist dies möglicherweise nicht der erste Seitenaufruf Ihres Besuchs. Zu Testzwecken können Sie das Cookie entfernen, sodass der nächste Aufruf der erste Seitenaufruf für den entsprechenden Besuch ist:

      1. Suchen Sie auf der Registerkarte Anwendung die `adcloud` und überprüfen Sie, ob das Cookie `_les_v` (letzter Besuch) mit dem Wert `y` und ein UTC-Epoch-Zeitstempel, der in 30 Minuten abläuft.
      1. Löschen Sie die `ad cloud` Cookie und aktualisieren Sie die Seite.

1. (Implementierungen, die den Experience Cloud Identity-Dienst verwenden `visitorAPI.js` code) Filtern nach `/b/ss` , um den Analytics-Treffer anzuzeigen.

   ![Filtern nach `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. (Implementierungen, die die Experience Platform verwenden [!DNL Web SDK] `alloy.js`code) Filtern nach `/interact` , um zu überprüfen, ob die Anfrage-Payload an das Edge-Netzwerk `advertisingStitchID`.

   ![Filtern nach `/interact`](/help/integrations/assets/a4adc-code-validation-filter-interact.png)

1. Vergleichen Sie die ID-Werte zwischen den beiden Treffern. Alle Werte werden in Abfragezeichenfolgenparametern angezeigt, mit Ausnahme der Report Suite-ID im Analytics-Treffer, bei der es sich um den URL-Pfad unmittelbar nach `/b/ss/`.

   | ID | Analytics-Parameter | Edge Network | Advertising Cloud-Parameter |
   | --- | --- | --- | --- |
   | Experience Cloud IMS-Organisation | `mcorgid` |  | `_les_imsOrgid` |
   | Zusätzliche Daten-ID | sdid |  | `_les_sdid` |
   | Zuordnungs-ID | stitchId | `advertisingStitchID` unter `_adcloud` property |  |
   | Analytics Report Suite | Der Wert nach `/b/ss/` |  | `_les_rsid` |
   | Experience Cloud-Besucher-ID | mid |  | `_les_mid` |

   Wenn die ID-Werte übereinstimmen, wird die JavaScript-Implementierung bestätigt. Advertising Cloud sendet die [!DNL Analytics] Server alle Clickthrough- oder Durchsichts-Tracking-Details, sofern vorhanden.

#### So bestätigen Sie den Code mit [!DNL Adobe Experience Cloud Debugger]

1. Öffnen Sie die [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html) auf Ihrer Homepage.
1. Navigieren Sie zu [!UICONTROL Network] Registerkarte.
1. Im [!UICONTROL Solutions Filter] Symbolleiste, klicken Sie auf [!UICONTROL Advertising Cloud] und [!UICONTROL Analytics].
1. Im [!UICONTROL Request URL – Hostname] Parameterzeile, suchen `lasteventf-tm.everesttech.net`.
1. Im [!UICONTROL Request – Parameters] -Zeile die generierten Signale, ähnlich wie Schritt 3, in &quot;[So bestätigen Sie den Code mit [!DNL Chrome Developer Tools]](#validate-js-chrome).&quot;
   * (Implementierungen, die den Experience Cloud Identity-Dienst verwenden `visitorAPI.js` Code) Stellen Sie sicher, dass `Sdid` -Parameter entspricht dem `Supplemental Data ID` im Adobe Analytics-Filter.
   * (Implementierungen, die die Experience Platform verwenden [!DNL Web SDK] `alloy.js`code) Stellen Sie sicher, dass der Wert der `advertisingStitchID` -Parameter entspricht dem `Sdid` an das Experience Platform Edge Network gesendet.
   * Wenn der Code nicht generiert wird, überprüfen Sie, ob das Advertising Cloud-Cookie im [!UICONTROL Application] Registerkarte. Nachdem sie entfernt wurde, aktualisieren Sie die Seite und wiederholen Sie den Vorgang.

   ![Auditing [!DNL Analytics for Advertising Cloud] JavaScript-Code in [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Voraussetzungen und Schlüsselinformationen für die Implementierung [!DNL Analytics for Advertising Cloud]](prerequisites.md)

