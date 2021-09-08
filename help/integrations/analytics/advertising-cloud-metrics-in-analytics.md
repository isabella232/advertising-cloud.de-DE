---
title: Advertising Cloud-Metriken in Analysis Workspace
description: Advertising Cloud-Metriken in Analysis Workspace
feature: Integration with Adobe Analytics
exl-id: d740bd19-c643-4917-9cfd-f9cf0affd07e
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---

# Advertising Cloud-Metriken in Analysis Workspace

*Werbetreibende, die nur über eine Advertising Cloud-Adobe Analytics-Integration verfügen*

>[!NOTE]
>
>* Advertising Cloud übergibt Traffic-Metriken und -Dimensionen an [!DNL Analytics] täglich.
>* [!DNL Analytics] erfasst Advertising Cloud-Clickthroughs und Durchsichten in Echtzeit.


## Traffic-Metriken aus Advertising Cloud

>[!NOTE]
>
>Alle Advertising Cloud-Traffic-Metriken in [!DNL Analytics] beginnen mit &quot;AMO&quot;.

| Traffic-Metrik | Beschreibung |
| -------------- | ----------- |
| [!UICONTROL AMO Impressions] | Die Anzahl der Advertising Cloud-Impressionen. |
| [!UICONTROL AMO Clicks] | Die Anzahl der Advertising Cloud-Klicks insgesamt. |
| [!UICONTROL AMO Cost] | Die Ausgaben der Advertising Cloud in der Währung der Report Suite. |
| [!UICONTROL AMO ID Instance] | Die Häufigkeit, mit der die Advertising Cloud ID festgelegt wird. |
| [!UICONTROL AMO Minutes Viewed] | Die Anzahl der Minuten, in denen ein Advertising Cloud-Video angesehen wurde. |
| [!UICONTROL AMO Views] | Die Anzahl der Ansichten auf einer Anzeige. Eine Ansicht wird gezählt, wenn der Viewer das Advertising Cloud-Video startet. |
| [!UICONTROL AMO Views 25% Complete] | Die Anzahl der Ansichten, bei denen mindestens 25 % eines Advertising Cloud-Videos angesehen wurden. |
| [!UICONTROL AMO Views 50% Complete] | Die Anzahl der Ansichten, bei denen mindestens 50 % eines Advertising Cloud-Videos angesehen wurden. |
| [!UICONTROL AMO Views 75% Complete] | Die Anzahl der Ansichten, bei denen mindestens 75 % eines Advertising Cloud-Videos angesehen wurden. |
| [!UICONTROL AMO Views 100% Complete] | Die Anzahl der Ansichten, bei denen 100 % eines Advertising Cloud-Videos angesehen wurden. |
| [!UICONTROL AMO Viewable Impressions] | Die Anzahl der Impressionen, die gemäß der Platzierungskonfiguration als sichtbar gemessen wurden. |
| [!UICONTROL AMO Not Viewable Impressions] | Die Anzahl der Impressionen, die als nicht sichtbar identifiziert wurden. Dieser Wert wird berechnet als ([!UICONTROL AMO Measurable Impressions] - [!UICONTROL AMO Viewable ]). |
| [!UICONTROL AMO Measurable Impressions] | Die Anzahl der Impressionen, für die die Sichtbarkeitsinstrumentierung erfolgreich initialisiert wurde. Dieser Wert wird berechnet als (instrumentierte Impressionen - die Anzahl nicht messbarer Impressionen). |

## Nützliche benutzerspezifische berechnete Metriken für Advertising Cloud

Ziehen Sie die Erstellung der folgenden Metriken für Ihre Advertising Cloud-Daten in Erwägung.

* Klicks zur Einstiegsseiteninstanz ([!UICONTROL AMO ID Instances] / [!UICONTROL AMO Clicks]): Dies ist der Prozentsatz der Personen, die auf die Anzeige geklickt und sie zur Landingpage weitergeleitet haben.
* Messbare Rate ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Impressions] * 100)
* Sichtbare Impressionsrate ([!UICONTROL AMO Viewable Impressions] / [!UICONTROL AMO Measureable Impressions] * 100)
* Kosten pro Ansicht ([!UICONTROL AMO Cost] / [!UICONTROL AMO Views])
* Kosten pro Klick ([!UICONTROL AMO Cost] / [!UICONTROL AMO Clicks])

## Advertising Cloud-Dimensionen

>[!NOTE]
>
>Alle Advertising Cloud-Dimensionen in [!DNL Analytics] werden von &quot;(AMO-ID)&quot;gefolgt.

| Dimension | Anwendbare Advertising Cloud-Daten | Beschreibung |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] und  [!DNL Search] Daten | Advertising Cloud DSP oder der Name der Suchmaschine |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] und  [!DNL Search] Daten | Der Kontoname. |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] und  [!DNL Search] Daten | RTB ([!DNL DSP]) oder der Name des Anzeigennetzwerks ([!DNL Search]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] und  [!DNL Search] Daten | Der Kampagnenname. |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] und  [!DNL Search] Daten | Der Name des Pakets ([!DNL DSP]) oder Portfolios ([!DNL Search]). |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] data | Der Platzierungsname. |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search] data | Der Anzeigengruppenname. |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search] data | Das Keyword. |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search] data | Der Übereinstimmungstyp für die Suche. |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search] data | Keyword und Übereinstimmungstyp. |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] und  [!DNL Search] Daten | Der Anzeigentyp, z. B. `text`, `video`, `display` oder `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] und  [!DNL Search] Daten | Der Anzeigentyp ([!DNL DSP]) oder der Anzeigentitel ([!DNL Search]). |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] und  [!DNL Search] Daten | Die Anzeigenbeschreibung ([!DNL DSP]) oder der Anzeigentext ([!DNL Search]). |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search] data | Die in der Anzeige angezeigte URL. |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search] data | Die Ziel-URL für die Anzeige. |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] und  [!DNL Search] Daten | Ob der Einstieg in die Landingpage eine Durchsicht oder ein Clickthrough war. |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search] data | Das Produktziel für eine Produktlistenanzeige. |

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising Cloud]](overview.md)
>* [[!DNL Analytics] Daten in Advertising Cloud](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

