---
title: JavaScript-Code für  [!DNL Analytics for Advertising Cloud]
description: JavaScript-Code für  [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 184508ce-df8d-4fa0-b22b-ca0546a61d58
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 0%

---

# JavaScript-Code für [!DNL Analytics for Advertising Cloud]

*Werbetreibende, die nur über eine Advertising Cloud-Adobe Analytics-Integration verfügen*

*Advertiser nur mit Advertising Cloud DSP*

Bei Advertising Cloud DSP verfolgt die Integration [!DNL Analytics for Advertising Cloud] die Durchsichts- und Clickthrough-Site-Interaktionen. Clickthrough-Besuche werden anhand des standardmäßigen Adobe Analytics-Codes auf Ihren Webseiten verfolgt. Der [!DNL Analytics]-Code erfasst die AMO-ID- und EF-ID-Parameter in der Landingpage-URL und verfolgt sie in ihren jeweiligen reservierten eVars. Sie können Durchsichtsbesuche verfolgen, indem Sie zwei Zeilen JavaScript-Code auf Ihren Webseiten bereitstellen.

Beim ersten Seitenaufruf eines Site-Besuchs prüft der Advertising Cloud-JavaScript-Code, ob der Besucher zuvor eine Anzeige gesehen oder angeklickt hat. Wenn der Benutzer zuvor über einen Clickthrough auf die Site gelangt ist oder noch keine Anzeige gesehen hat, wird der Besucher ignoriert. Wenn der Besucher eine Anzeige gesehen hat und nicht über einen Clickthrough während des in Advertising Cloud festgelegten [Klick-Lookback-Fensters](/help/integrations/analytics/prerequisites.md#lookback-a4adc) auf die Site gelangt ist, generiert der Advertising Cloud-JavaScript-Code mithilfe des [Experience Cloud-ID-Diensts](https://experienceleague.adobe.com/docs/id-service/using/home.html) eine zusätzliche ID (`SDID`), die zum Verknüpfen von Daten aus Advertising Cloud mit dem Adobe Analytics-Treffer des Besuchers verwendet wird. Adobe Analytics fragt dann Advertising Cloud nach der AMO-ID und der EF-ID ab, die mit der Anzeigenbelichtung verknüpft sind. Die AMO-ID und EF-IDs werden dann in ihre jeweiligen eVars eingefügt. Diese Werte bleiben für einen bestimmten Zeitraum bestehen (standardmäßig 60 Tage).

[!DNL Analytics] sendet stündlich Site-Traffic-Metriken (z. B. Seitenansichten, Besuche und Besuchszeit) sowie  [!DNL Analytics]  benutzerdefinierte oder Standardereignisse an Advertising Cloud, wobei die EF ID als Schlüssel verwendet wird. Diese [!DNL Analytics] -Metriken werden dann über das Advertising Cloud-Attributionssystem ausgeführt, um die Konversionen mit dem Klick- und Belichtungsverlauf zu verbinden.

>[!NOTE]
>
>Die JavaScript-Tracking-Logik von Advertising Cloud tritt auf der Adobe auf und hat daher praktisch keine Auswirkungen auf die Seitenladezeit.
>
>Im Gegensatz dazu tritt die Logik für den [!DNL DCM]-Data Connector zu [!DNL Analytics] (unter Verwendung von [!DNL Google Campaign Manager 360]) für Advertising Cloud DSP clientseitig auf. Die clientseitige Zuordnung verlangsamt das Laden der Seite und erhöht das Risiko eines Datenverlusts. Dies geschieht, weil das JavaScript [!DNL Analytics] [!DNL DoubleClick] pingen muss und darauf warten muss, dass [!DNL DoubleClick] die letzten Klick-/Impressionsdaten an [!DNL Analytics] zurückgibt. Wenn Ihr [!DNL DSP]-Team den [!DNL DCM]-Data Connector eingerichtet, müssen Sie angeben, wie lange Sie die Seite verzögern möchten.

## Bereitstellen des JavaScript-Codes

Die JavaScript-Bibliothek besteht aus zwei Zeilen, mit denen [!DNL Analytics] und Advertising Cloud miteinander kommunizieren können. Wenn die [!DNL Analytics for Advertising Cloud]-Integration während der Advertising Cloud-Implementierung abgeschlossen wurde, sollten Sie diesen Code mit Anweisungen zur Bereitstellung erhalten haben.

Wenn Sie noch keinen Code haben, wenden Sie sich an das Advertising Cloud-Supportteam.

### Speicherort des Codes

Die JavaScript-Funktion [!DNL Analytics for Advertising Cloud] muss nach dem Experience Cloud-ID-Dienst, jedoch vor Ihrem Analytics-App-Measurement-Code stehen, damit die zusätzliche ID (`SDID`) in Ihren Analytics-Aufruf aufgenommen werden kann.

![Codeplatzierung](/help/integrations/assets/a4adc-code-placement.png)

### Validieren der Codebereitstellung

Sie können eine Validierung mit einem beliebigen Paket-Sniffer-Typ von Tool durchführen (z. B. [!DNL Charles], [!DNL Fiddler] oder [!DNL Chrome Developer Tools]), indem Sie die Werte der vier IDs zwischen der Anfrage an Advertising Cloud und der Anfrage an [!DNL Analytics] vergleichen, wie unten beschrieben.

#### So bestätigen Sie den Code mit [!DNL Chrome Developer Tools] {#validate-js-chrome}

1. Öffnen Sie [!DNL Chrome Developer Tools] und klicken Sie auf die Registerkarte **Netzwerk** .
1. Laden Sie eine Website-Seite, die das JavaScript [!DNL Analytics for Advertising Cloud] enthält.
1. Filtern Sie die Registerkarte [!UICONTROL Network] nach `last` und überprüfen Sie zwei Zeilen:

   ![Letzte Filterung](/help/integrations/assets/a4adc-code-validation-filter-last.png)

   * Die erste Zeile ist der Aufruf der JavaScript-Bibliothek mit dem Titel `last-event-tag-latest.min.js`.
   * Die zweite Zeile ist der Aufruf, der die Anfrage an Advertising Cloud sendet. Er beginnt wie folgt: `_les_imsOrgId=[your_imsOrgId_here]&_les_url=[your_encoded_url]`

      Wenn Sie den Aufruf an Advertising Cloud nicht sehen, ist dies möglicherweise nicht der erste Seitenaufruf Ihres Besuchs. Zu Testzwecken können Sie das Cookie entfernen, sodass der nächste Aufruf der erste Seitenaufruf für den entsprechenden Besuch ist:

      1. Suchen Sie auf der Registerkarte &quot;Application&quot;das Cookie `adcloud` und überprüfen Sie, ob das Cookie `_les_v` (letzter Besuch) mit dem Wert `y` und einem UTC-Epochenzeitstempel enthält, der in 30 Minuten abläuft.
      1. Löschen Sie das Cookie `ad cloud` und aktualisieren Sie die Seite.
1. Filtern Sie nach `/b/ss`, um den Analytics-Treffer anzuzeigen.

   ![Filtern nach  `/b/ss`](/help/integrations/assets/a4adc-code-validation-filter-bss.png)

1. Vergleichen Sie die ID-Werte zwischen den beiden Treffern. Alle Werte befinden sich in Abfragezeichenfolgenparametern mit Ausnahme der Report Suite-ID im Analytics-Treffer, der der URL-Pfad unmittelbar nach `/b/ss/` ist.

   | ID | Analytics-Parameter | Advertising Cloud-Parameter |
   |--- |--- |--- |
   | Experience Cloud IMS-Organisation | `mcorgid` | `_les_imsOrgid` |
   | Zusätzliche Daten-ID | sdid | `_les_sdid` |
   | Analytics Report Suite | Der Wert nach `/b/ss/` | `_les_rsid` |
   | Experience Cloud-Besucher-ID | mid | `_les_mid` |

   Wenn die ID-Werte übereinstimmen, wird die JavaScript-Implementierung bestätigt. Advertising Cloud sendet dem [!DNL Analytics]-Server alle Clickthrough- oder Durchsichts-Tracking-Details, sofern vorhanden.

#### So bestätigen Sie den Code mit [!DNL Adobe Experience Cloud Debugger]

1. Öffnen Sie [[!DNL Adobe Experience Cloud Debugger]](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html) auf Ihrer Homepage.
1. Gehen Sie zur Registerkarte [!UICONTROL Network] .
1. Klicken Sie in der Symbolleiste [!UICONTROL Solutions Filter] auf [!UICONTROL Advertising Cloud] und [!UICONTROL Analytics].
1. Suchen Sie in der Parameterzeile [!UICONTROL Request URL – Hostname] nach `lasteventf-tm.everesttech.net`.
1. Prüfen Sie in der Zeile [!UICONTROL Request – Parameters*] die erzeugten Signale, ähnlich wie in Schritt 3 unter &quot;[So bestätigen Sie den Code mit [!DNL Chrome Developer Tools]](#validate-js-chrome)&quot;.
   * Vergewissern Sie sich, dass der Parameter `SDID` mit dem Parameter `Supplemental Data ID` im Adobe Analytics-Filter übereinstimmt.
   * Wenn der Code nicht generiert wird, überprüfen Sie, ob das Advertising Cloud-Cookie auf der Registerkarte [!UICONTROL Application] entfernt wurde. Nachdem sie entfernt wurde, aktualisieren Sie die Seite und wiederholen Sie den Vorgang.

   ![Auditing von  [!DNL Analytics for Advertising Cloud] JavaScript-Code in  [!DNL Experience Cloud Debugger]](/help/integrations/assets/a4adc-js-audit-debugger.png)

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Voraussetzungen und Schlüsselinformationen für die Implementierung [!DNL Analytics for Advertising Cloud]](prerequisites.md)

