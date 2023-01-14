---
title: Adobe Advertising-Metriken in Analysis Workspace
description: Adobe Advertising-Metriken in Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: d740bd19-c643-4917-9cfd-f9cf0affd07e
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Adobe Advertising-Metriken in Analysis Workspace

*Werbetreibende mit nur einer Adobe Advertising-Adobe Analytics-Integration*

>[!NOTE]
>
>* Adobe Advertising übergibt Traffic-Metriken und -Dimensionen an [!DNL Analytics] täglich.
>* [!DNL Analytics] erfasst Adobe Advertising-Clickthroughs und Durchsichten in Echtzeit.


## Traffic-Metriken aus Adobe Advertising

>[!NOTE]
>
>Alle Adobe Advertising-Traffic-Metriken in [!DNL Analytics] Beginnen Sie mit &quot;AMO&quot;.

| Traffic-Metrik | Beschreibung |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | Die Anzahl der Adobe Advertising-Impressionen. |
| [!UICONTROL AMO Clicks] | Die Anzahl der Adobe-Werbe-Klicks insgesamt. |
| [!UICONTROL AMO Cost] | Die Werbeausgaben für Adoben in der Währung der Report Suite. |
| [!UICONTROL AMO ID Instance] | Die Häufigkeit, mit der die Adobe Advertising ID festgelegt wurde. |
| [!UICONTROL AMO Minutes Viewed] | Die Anzahl der Minuten, in denen ein Adobe Advertising-Video angesehen wurde. |
| [!UICONTROL AMO Views] | Die Anzahl der Ansichten auf einer Anzeige. Eine Ansicht wird gezählt, wenn der Viewer das Adobe Advertising-Video startet. |
| [!UICONTROL AMO Views 25% Complete] | Die Anzahl der Ansichten, bei denen mindestens 25 % eines Adobe Advertising-Videos angesehen wurden. |
| [!UICONTROL AMO Views 50% Complete] | Die Anzahl der Ansichten, bei denen mindestens 50 % eines Adobe Advertising-Videos angesehen wurden. |
| [!UICONTROL AMO Views 75% Complete] | Die Anzahl der Ansichten, bei denen mindestens 75 % eines Adobe Advertising-Videos angesehen wurden. |
| [!UICONTROL AMO Views 100% Complete] | Die Anzahl der Ansichten, bei denen 100 % eines Adobe Advertising-Videos angesehen wurden. |
| [!UICONTROL AMO Viewable Impressions] | Die Anzahl der Impressionen, die gemäß der Platzierungskonfiguration als sichtbar gemessen wurden. |
| [!UICONTROL AMO Not Viewable Impressions] | Die Anzahl der Impressionen, die als nicht sichtbar identifiziert wurden. Dieser Wert wird als ([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable ]). |
| [!UICONTROL AMO Measurable Impressions] | Die Anzahl der Impressionen, für die die Sichtbarkeitsinstrumentierung erfolgreich initialisiert wurde. Dieser Wert wird berechnet als (instrumentierte Impressionen - die Anzahl nicht messbarer Impressionen). |

## Nützliche benutzerspezifische berechnete Metriken für Adobe Advertising

Erwägen Sie die Erstellung der folgenden Metriken für Ihre Adobe Advertising-Daten.

* Klicks zur Landingpage-Instanz ([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks]): Dies ist der Prozentsatz der Personen, die auf die Anzeige geklickt und sie zur Landingpage weitergeleitet haben.
* Messrate ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* Sichtbare Impressionsrate ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* Kosten pro Ansicht ([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* Kosten pro Klick ([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

## Adobe Advertising-Dimensionen

>[!NOTE]
>
>Alle Adobe Advertising-Dimensionen in [!DNL Analytics] gefolgt von &quot;(AMO-ID).&quot;

| Dimension | Anwendbare Adobe Advertising-Daten | Beschreibung |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] und [!DNL Search] data | Advertising DSP oder der Name der Suchmaschine |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] und [!DNL Search] data | Der Kontoname. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] und [!DNL Search] data | RTB ([!DNL DSP]) oder dem Namen des Werbenetzwerks ([!DNL Search]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] und [!DNL Search] data | Der Kampagnenname. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] und [!DNL Search] data | Das Paket ([!DNL DSP]) oder Portfolio ([!DNL Search]). |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] data | Der Platzierungsname. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search] data | Der Anzeigengruppenname. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search] data | Das Keyword. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search] data | Der Übereinstimmungstyp für die Suche. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search] data | Keyword und Übereinstimmungstyp. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] und [!DNL Search] data | Der Anzeigentyp, z. B. `text`, `video`, `display`oder `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] und [!DNL Search] data | Der Anzeigentyp ([!DNL DSP]) oder Anzeigentitel ([!DNL Search]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] und [!DNL Search] data | Die Anzeigenbeschreibung ([!DNL DSP]) oder Anzeigenkörper ([!DNL Search]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search] data | Die in der Anzeige angezeigte URL. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search] data | Die Ziel-URL für die Anzeige. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] und [!DNL Search] data | Ob der Einstieg in die Landingpage eine Durchsicht oder ein Clickthrough war. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search] data | Das Produktziel für eine Produktlistenanzeige. |

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Daten in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

