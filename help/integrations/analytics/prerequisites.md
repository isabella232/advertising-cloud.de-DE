---
title: Voraussetzungen und Schlüsselinformationen für die Implementierung [!DNL Analytics for Advertising]
description: Voraussetzungen und Schlüsselinformationen für die Implementierung [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%

---

# Voraussetzungen und Schlüsselinformationen für die Implementierung [!DNL Analytics for Advertising]

*Advertiser mit Advertising DSP und[!DNL Advertising Search]*

Lesen Sie die folgenden Informationen, bevor Sie Adobe Advertising mit Adobe Analytics integrieren.

## Anforderungen für die Berichterstellung für Adobe-Werbedaten in [!DNL Analytics]

* Eine der folgenden Optionen:
   * Adobe Experience Platform Web SDK: `alloy.js`
   * Experience Cloud Identity-Dienst: `visitorAPI.js` Version 2.0 oder höher
* Jede Version von Adobe Analytics (einschließlich [!DNL Prime], [!DNL Premium]oder [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` Version 2.1 oder höher

>[!TIP]
>
>Verwenden Sie zur Verbesserung der Datenintegrität die neueste Version jeder Bibliothek.

## Voraussetzungen für die Freigabe von Analytics-Segmenten für Adobe Advertising

* Experience Cloud Identity-Dienst: `visitorAPI.js` Version 2.1 oder höher
* Adobe Analytics: `!DNL appMeasurement.js` Version 1.8 oder höher

## Berichterstattungsanforderungen [!DNL Analytics] Daten in Adobe Advertising

Stellen Sie dem Implementierungsteam von Adobe Advertising Folgendes bereit:

* Die [!DNL Analytics] Report Suite-ID, die für die Berichterstellung über Paid-Media-Aktivitäten und für die Einspeisung von Site-Aktivitäten zur Optimierung und Berichterstellung in Adobe Advertising verwendet wird
* Die Organisations-ID des Experience Cloud (Organisations-ID) des Unternehmens.

Sie finden beide IDs auf der [Registerkarte &quot;Zusammenfassung&quot;des Adobe Experience Cloud Debuggers](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html).

![Bildschirm &quot;Experience Cloud Debugger Summary&quot;](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Daten in Adobe Advertising {#lookback-a4adc}

weil [!DNL Analytics] -Daten zur Berichterstellung und Optimierung an Adobe Advertising gesendet werden, unterliegen die Daten den Attributionsregeln, einschließlich der Impressions- und Klick-Lookback-Fenster, die für den Advertiser in Adobe Advertising konfiguriert sind.

![Lookback-Fenstereinstellungen auf Advertiser-Ebene in Adobe Advertising](/help/integrations/assets/a4adc-lookbacks.png)

* Adobe Advertising Attributions-Klick-Lookback-Fenster: Die Anzahl der Tage nach dem ersten Klick, in denen der Klick einer Konversion zugeordnet werden kann. Standardmäßig beträgt dieser Wert 60 Tage. die Höchstdauer beträgt 90 Tage
* Adobe Advertising Attributions-Impressions-Lookback-Fenster: Die Anzahl der Tage, nach denen eine Ad-Impression auftritt, in denen die Impression einer Konversion zugeordnet werden kann. Standardmäßig beträgt dieser Wert 14 Tage. die Höchstdauer beträgt 30 Tage

   >[!NOTE]
   >
   > Das Impression-Lookback-Fenster ist spezifisch für Adobe Advertising, nicht [!DNL Analytics for Advertising], Reporting.

Die [!DNL Analytics for Advertising] JavaScript verwendet diese Einstellungen, um zu bestimmen, wie weit ein Durchsichtseintrag oder Clickthrough-Eintrag für die Site als gültig zurückbetrachtet werden soll. Weitere Informationen zur Bestimmung von Durchsichten und Clickthroughs finden Sie unter[Von Analytics verwendete Adobe Advertising-IDs](ids.md).&quot;

## Adobe Advertising Data in [!DNL Analytics]

[!DNL Analytics] legt Adobe Advertising-IDs (AMO-IDs) im Analytics-Treffer fest, vorbehaltlich der Persistenzeinstellung des Advertisers, die sowohl für Clickthroughs als auch für Durchsichten gilt. Die Persistenzeinstellung wird auf dem Adobe Advertising-Backend konfiguriert und Ihre [!DNL Adobe] Kontoteam kann es ändern.

* [!DNL Analytics for Advertising] Ablauf der eVar: Standardmäßig 60 Tage für AMO-IDs

>[!NOTE]
>
>Um Daten für einen anderen Zeitrahmen zu segmentieren, können Sie [Einrichten benutzerdefinierter Segmente](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) mit verschiedenen Lookback-Fenstern in Analysis Workspace.

## Unterstützte Anzeigenumgebungen

* Suche
* Anzeige
* Video
* Online-Video
* Nativ

Wenden Sie sich an [!DNL Adobe] Kontoteam für die neuesten unterstützten Anzeigenumgebungen in den einzelnen Kanälen.

## Was Sie vor der Implementierung wissen sollten

* Das Implementierungsteam für Adobe Advertising richtet die Integration ein.

* Für diese Integration werden keine zusätzlichen Kosten in Rechnung gestellt, auch keine Server-Aufrufe führen zu zusätzlichen [!DNL Analytics] oder Werbekosten für Adoben.

* [!DNL Analytics for Advertising] ist serverunabhängig: Ein Durchsichts- oder Clickthrough-Vorgang kann von jedem Anzeigen-Server aus erfolgen und die richtigen IDs werden bei der Site-Eingabe generiert.

* Die Integration übergibt nur [!DNL Analytics] Standardereignisse und benutzerspezifische Ereignisse in Adobe Advertising zur Angebotsoptimierung nachfolgender Paid-Media- und Werbemaßnahmen. Es ist nicht vorbei [!DNL Analytics] Segmente, berechnete Metriken und eVars zur Adobe Advertising zur Angebotsoptimierung.

* Adobe Advertising erstellt beständige IDs in [!DNL Analytics] basierend auf der letzten Anzeige, auf die geklickt oder angezeigt wurde, bevor der Benutzer die Site aufruft, basierend auf der [Klick- und Viewthrough-Lookback-Fenster](#lookback-a4adc) konfiguriert in Adobe Advertising. Wenn ein Site-Besucher beide Arten von Site-Einstiegsinteraktionen in seinem Profil aufweisen sollte und sich der Klick innerhalb des Lookback-Zeitraums befindet, würde die Clickthrough-ID des Besuchers die Durchsichts-ID für die Site-Berichterstellung außer Kraft setzen.

* [!DNL Analytics for Advertising] Das Konversions-Tracking in Adobe Analytics verwendet ein konfigurierbares Tracking-Lookback-Fenster (standardmäßig 60 Tage). Adobe Advertising-Berichte spiegeln Site-Konversionen und Interaktionen am Ende dieses Tracking-Lookback-Fensters wider.

* Alle Anzeigentypen werden unterstützt. Es werden jedoch nicht alle Anzeigenumgebungen unterstützt.

   Beispielsweise werden Anzeigen mit angeschlossenem TV (CTV) nicht verfolgt, da in CTV keine Klicks auftreten und auf demselben Gerät keine Konversionen stattfinden können. Wenn die Anzeige jedoch in einer Desktop-Umgebung angezeigt wird, können einige Viewthrough-Site-Einstiegsdaten verfolgt werden.

* [!DNL Analytics] Konversionen werden derzeit verfolgt und nur einem Besucher auf demselben Gerät zugeordnet.

* [!DNL Analytics for Advertising] unterstützt keine In-App-Durchsichtskonvertierungen.

* Advertiser, die eine serverseitige Weiterleitungsimplementierung von [!DNL Analytics].

### Zusätzliche ID

Sobald der Experience Cloud Identity-Dienst für eine Site implementiert wurde, enthalten Treffer Daten aus [!DNL Analytics] oder Adobe Advertising enthält eine zusätzliche ID.

Beispiel: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Für eine genaue Datenintegration werden alle Adobe Advertising-Aufrufe von einem [!DNL Analytics for Advertising] -Aktivität, um Inhalte bereitzustellen oder die Zielmetrik aufzuzeichnen, muss über eine entsprechende [!DNL Analytics] Treffer, der dieselbe zusätzliche ID aufweist.

Fehlerbehebung in [!DNL Analytics]müssen Sie sicherstellen, dass die zusätzliche ID für [!DNL Analytics] Treffer. Im [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using-v2/summary.html), können Sie diese ID auf der Registerkarte Adobe Advertising als `sdid` Parameter.

>[!NOTE]
>
> Diese Implementierung funktioniert ähnlich wie die [!DNL Analytics for Target] Integration.

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising]](overview.md)
>* [JavaScript-Code für Analytics für Advertising](/help/integrations/analytics/javascript.md)

