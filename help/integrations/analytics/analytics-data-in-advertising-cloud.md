---
title: '"[!DNL Analytics] Daten in Advertising Cloud"'
description: '"[!DNL Analytics] Daten in Advertising Cloud"'
feature: Integration with Adobe Analytics
exl-id: 79fbc809-9965-41c1-971f-3652cc78fee3
source-git-commit: 2c94b6c02b4e24878639dd9edbc0455e1751f679
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# [!DNL Analytics] Daten in Advertising Cloud

*Werbetreibende, die nur über eine Advertising Cloud-Adobe Analytics-Integration verfügen*

## Analytics-Segmente

Alle in erstellten Segmente [!DNL Analytics] und in Experience Cloud veröffentlicht.

Es dauert 24 bis 48 Stunden, bis neue Segmente in Advertising Cloud angezeigt werden. Aktualisierungen vorhandener Segmente werden innerhalb von etwa acht Stunden synchronisiert.

<!-- I added "metric" to some of the links below, even though it looks redundant, because of syntax limitations: If you use [!DNL] or [!UICONTROL] as the sole text of a link (such as [[!UICONTROL Revenue]], the tag is included in the link text (such as "[!UICONTROL Revenue]") when it's published. -->

## Metriken zur Site-Interaktion

>[!NOTE]
>
>* [!DNL Analytics] übergibt Ereignisse für den EF ID-eVar an Advertising Cloud.  Die Standardintegration unterstützt nicht das Senden berechneter Metriken oder anderer Dimensionen (eVars) an Advertising Cloud. Wenn die berechnete Metrik jedoch vollständig in einem benutzerspezifischen Ereignis erfasst werden kann, kann Advertising Cloud das benutzerspezifische Ereignis erfassen.
>* [!DNL Analytics] übergibt Daten stündlich an Advertising Cloud.


* [!UICONTROL Timespent_secs_1stvisit]: Die Anzahl der Sekunden, die während des ersten Besuchs des Besuchers auf der Site verbracht wurden.
* [!UICONTROL Timespent_secs_total]: Die Gesamtanzahl der Sekunden, die innerhalb des Klick-Lookback-Fensters bei allen Besuchen auf der Site verbracht wurden.
* [!UICONTROL Pageviews_1stvisit]: Die Anzahl der Seitenansichten auf der Site während des ersten Besuchs des Besuchers.
* [!UICONTROL Pageviews_total]: Die Gesamtzahl der Seitenansichten auf der Site für alle Besuche im Klick-Lookback-Fenster.
* [[!UICONTROL Bounces] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/bounces.html)
* [[!UICONTROL Visits] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html)
* [!UICONTROL ef_id_instances]: Die Häufigkeit, mit der die [!DNL Analytics] erfasst [!UICONTROL EF ID].

## Konversionsmetriken

[!DNL Analytics] übergibt täglich Konversionsmetriken an Advertising Cloud.

### Standardkonversionsmetriken

* [[!UICONTROL Revenue] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/revenue.html)
* [[!UICONTROL Orders] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/orders.html)
* [[!UICONTROL Units] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/units.html)
* [[!UICONTROL Carts] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/carts.html)
* [[!UICONTROL Cart Views] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-views.html)
* [[!UICONTROL Checkouts] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/checkouts.html)
* [[!UICONTROL Cart Additions] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-additions.html)
* [[!UICONTROL Cart Removals] Metrik](https://experienceleague.adobe.com/docs/analytics/components/metrics/cart-removals.html)

### Benutzerspezifische Konversionsmetriken

Diese Metriken sind spezifisch für die Report Suite, sodass die verfügbaren Metriken für jeden Kunden und jede Report Suite variieren.

### Reservierte Konversionsmetriken

Diese Metriken sind spezifisch für die Report Suite, sodass die verfügbaren Metriken für jeden Kunden und jede Report Suite variieren.

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Advertising Cloud-Metriken in Analysis Workspace](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)

