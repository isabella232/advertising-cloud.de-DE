---
title: Voraussetzungen und Schlüsselinformationen für die Implementierung [!DNL Analytics for Advertising Cloud]
description: Voraussetzungen und Schlüsselinformationen für die Implementierung [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 08e54e2b-ed9b-4489-8de5-ab1379b7133c
source-git-commit: bfbfc293ad04b294c813ce7c8a11200e70fc812f
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 0%

---

# Voraussetzungen und Schlüsselinformationen für die Implementierung [!DNL Analytics for Advertising Cloud]

*Advertiser mit Advertising Cloud DSP und Advertising Cloud Search*

Lesen Sie die folgenden Informationen, bevor Sie Advertising Cloud in Adobe Analytics integrieren.

## Anforderungen für die Berichterstellung für Advertising Cloud-Daten in [!DNL Analytics]

* Experience Cloud Identity-Dienst: `visitorAPI.js` Version 2.0 oder höher
* Jede Version von Adobe Analytics (einschließlich [!DNL Prime], [!DNL Premium]oder [!DNL Ultimate])
* Adobe Analytics: `appMeasurement.js` Version 2.1 oder höher

>[!TIP]
>
>Um die Datenintegrität zu verbessern, verwenden Sie die neueste Version des Experience Cloud Identity-Diensts mit CNAME-Unterstützung sowie die neueste Version von Analytics AppMeasurement für JavaScript.

## Voraussetzungen für die Freigabe von Analytics-Segmenten für Advertising Cloud

* Experience Cloud Identity-Dienst: `visitorAPI.js` Version 2.1 oder höher
* Adobe Analytics: `!DNL appMeasurement.js` Version 1.8 oder höher

## Berichterstattungsanforderungen [!DNL Analytics] Daten in Advertising Cloud

Stellen Sie dem Advertising Cloud-Implementierungsteam Folgendes zur Verfügung:

* Die [!DNL Analytics] Report Suite-ID, die für die Berichterstellung über Paid-Media-Aktivitäten und für die Bereitstellung von Site-Aktivitäten zur Optimierung und Berichterstellung in Advertising Cloud verwendet wird
* Die Organisations-ID des Experience Cloud (Organisations-ID) des Unternehmens.

Sie finden beide IDs auf der [Zusammenfassungsbildschirm des Adobe Experience Cloud Debuggers](https://experienceleague.adobe.com/docs/debugger/using/run-debugger.html).

![Bildschirm &quot;Experience Cloud Debugger Summary&quot;](/help/integrations/assets/a4adc-debugger-summary.png)

## [!DNL Analytics] Daten in Advertising Cloud {#lookback-a4adc}

weil [!DNL Analytics] -Daten zur Berichterstellung und Optimierung an Advertising Cloud gesendet werden, unterliegen die Daten den Attributionsregeln, einschließlich der Impressions- und Klick-Lookback-Fenster, die für den Advertiser in Advertising Cloud konfiguriert sind.

![Einstellungen des Lookback-Fensters auf Advertiser-Ebene in Advertising Cloud](/help/integrations/assets/a4adc-lookbacks.png)

* Advertising Cloud Attributions-Klick-Lookback-Fenster: Die Anzahl der Tage nach dem ersten Klick, in denen der Klick einer Konversion zugeordnet werden kann. Standardmäßig beträgt dieser Wert 60 Tage. die Höchstdauer beträgt 90 Tage
* Advertising Cloud Attributions-Impression-Lookback-Fenster: Die Anzahl der Tage, nach denen eine Ad-Impression auftritt, in denen die Impression einer Konversion zugeordnet werden kann. Standardmäßig beträgt dieser Wert 14 Tage. die Höchstdauer beträgt 30 Tage

   >[!NOTE]
   >
   > Das Impression-Lookback-Fenster ist spezifisch für Advertising Cloud, nicht [!DNL Analytics for Advertising Cloud], Reporting.

Die [!DNL Analytics for Advertising Cloud] JavaScript verwendet diese Einstellungen, um zu bestimmen, wie weit ein Durchsichtseintrag oder Clickthrough-Eintrag für die Site als gültig zurückbetrachtet werden soll. Weitere Informationen zur Bestimmung von Durchsichten und Clickthroughs finden Sie unter[Von Analytics verwendete Advertising Cloud IDs](ids.md).&quot;

## Advertising Cloud-Daten in [!DNL Analytics]

[!DNL Analytics] legt Advertising Cloud-IDs (AMO-IDs) im Analytics-Treffer fest, vorbehaltlich der Persistenzeinstellung des Advertisers, die sowohl für Clickthroughs als auch für Durchsichten gilt. Die Persistenzeinstellung wird auf dem Advertising Cloud-Backend konfiguriert und Ihre [!DNL Adobe] Der Kundenbetreuer kann dies ändern.

* [!DNL Analytics for Advertising Cloud] Ablauf der eVar: Standardmäßig 60 Tage für AMO-IDs

>[!NOTE]
>
>Um Daten für einen anderen Zeitrahmen zu segmentieren, können Sie [Einrichten benutzerdefinierter Segmente](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html) mit verschiedenen Lookback-Fenstern in Analysis Workspace.

## Unterstützte Anzeigenumgebungen

* Suche
* Anzeige
* Video
* Online-Video
* Nativ

Wenden Sie sich an [!DNL Adobe] Kundenbetreuer für die neuesten unterstützten Anzeigenumgebungen in den einzelnen Kanälen.

## Was Sie vor der Implementierung wissen sollten

* Für diese Integration werden keine zusätzlichen Kosten in Rechnung gestellt, auch keine Server-Aufrufe führen zu zusätzlichen [!DNL Analytics] oder Advertising Cloud-Gebühren.

* [!DNL Analytics for Advertising Cloud] ist serverunabhängig: Ein Durchsichts- oder Clickthrough-Vorgang kann von jedem Anzeigen-Server aus erfolgen und die richtigen IDs werden bei der Site-Eingabe generiert.

* Die Integration übergibt nur [!DNL Analytics] Standardereignisse und benutzerspezifische Ereignisse an Advertising Cloud zur Angebotsoptimierung nachfolgender Paid-Media- und Werbemaßnahmen. Es ist nicht vorbei [!DNL Analytics] Segmente, berechnete Metriken und eVars an Advertising Cloud zur Angebotsoptimierung.

* Advertising Cloud erstellt beständige IDs in [!DNL Analytics] basierend auf der letzten Anzeige, auf die geklickt oder angezeigt wurde, bevor der Benutzer die Site aufruft, basierend auf der [Klick- und Viewthrough-Lookback-Fenster](#lookback-a4adc) in Advertising Cloud konfiguriert. Wenn ein Site-Besucher innerhalb seines Profils beide Arten von Site-Einstiegsinteraktionen hätte und sich der Klick innerhalb des Lookback-Zeitraums befindet, würde die Clickthrough-ID des Besuchers die Durchsichts-ID für die Site-Berichterstellung außer Kraft setzen.

* [!DNL Analytics for Advertising Cloud] Das Konversions-Tracking in Adobe Analytics verwendet ein konfigurierbares Tracking-Lookback-Fenster (standardmäßig 60 Tage). Advertising Cloud-Berichte spiegeln Site-Konversionen und Interaktionen am Ende dieses Tracking-Lookback-Fensters wider.

* Alle Anzeigentypen werden unterstützt. Es werden jedoch nicht alle Anzeigenumgebungen unterstützt.

   Beispielsweise werden Anzeigen mit angeschlossenem TV (CTV) nicht verfolgt, da in CTV keine Klicks auftreten und auf demselben Gerät keine Konversionen stattfinden können. Wenn die Anzeige jedoch in einer Desktop-Umgebung angezeigt wird, können einige Viewthrough-Site-Einstiegsdaten verfolgt werden.

* [!DNL Analytics] Konversionen werden derzeit verfolgt und nur einem Besucher auf demselben Gerät zugeordnet.

* [!DNL Analytics for Advertising Cloud] unterstützt keine In-App-Durchsichtskonvertierungen.

* Advertiser, die eine serverseitige Weiterleitungsimplementierung von [!DNL Analytics].

### Zusätzliche ID

Sobald der Experience Cloud Identity-Dienst für eine Site implementiert wurde, enthalten Treffer Daten aus [!DNL Analytics] oder Advertising Cloud eine zusätzliche ID enthält.

Beispiel: `sdid=2F3C18E511F618CC-45F83E994AEE93A0`

Für eine genaue Datenintegration werden alle Advertising Cloud-Aufrufe verwendet, die von einer [!DNL Analytics for Advertising Cloud] -Aktivität, um Inhalte bereitzustellen oder die Zielmetrik aufzuzeichnen, muss über eine entsprechende [!DNL Analytics] Treffer, der dieselbe zusätzliche ID aufweist.

Fehlerbehebung in [!DNL Analytics]müssen Sie sicherstellen, dass die zusätzliche ID für [!DNL Analytics] Treffer. Im [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html), können Sie diese ID auf der Registerkarte Advertising Cloud als `sdid` Parameter.

>[!NOTE]
>
> Diese Implementierung funktioniert ähnlich wie die [!DNL Analytics for Target] Integration.

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising Cloud]](overview.md)
>* [JavaScript-Code für Analytics für Advertising Cloud](/help/integrations/analytics/javascript.md)

