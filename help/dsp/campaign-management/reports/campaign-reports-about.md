---
title: Über In-Platform-Berichte
description: Erfahren Sie mehr über die Berichtsdaten in den Kampagnenverwaltungsansichten.
feature: DSP Campaign Data Views
exl-id: e9f7dafe-e0db-4fec-bf5b-858cbcfdde45
source-git-commit: b2393d5e66ba5d3d2dc9816825c05eda076eaad1
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# Über In-Platform-Berichte

<!-- rename "About Performance Reports in Campaign Management Views?" -->
Die Ansichten der Kampagnenverwaltung beinhalten umfassende Berichtdaten. Die verfügbaren Berichte helfen Ihnen dabei, die Pakete und Platzierungen zu identifizieren, die eine gute Leistung erbringen, und jene, die Ihre Aufmerksamkeit benötigen. Schnellaktion-Schaltflächen machen Sie auch produktiver.

## Liste aller Kampagnen

Die [!UICONTROL Campaigns] -Ansicht eine Liste aller Kampagnen in Ihrem Konto. Die [!UICONTROL Subtotals] -Zeile zeigt entweder die Summe oder den Durchschnittswert jeder Metrik über alle sichtbaren Zeilen hinweg.

![Kampagnenliste](/help/dsp/assets/campaigns-list.png)

Standardmäßig enthält jede Kampagnenzeile die Geschwindigkeit und Versandmetriken. Schrittmetriken beinhalten [!UICONTROL Gross Spend (Lifetime)], das eine Messung der tatsächlichen On-Target-Ausgaben im Vergleich zu den erwarteten On-Target-Ausgaben für alle Kampagnenkits enthält, sodass Sie leistungsschwache Kampagnen auf einen Blick erkennen können. Sie können optional [Spaltenansicht ändern](column-view-change.md) oder sogar [Erstellen einer benutzerdefinierten Spaltenansicht](column-view-create.md).

Sie können [Datentabellen anpassen](campaign-data-views-about.md) auf zusätzliche Weise und [die sichtbaren Daten filtern](campaign-data-filter.md).

Um eine Kampagne detaillierter anzuzeigen, klicken Sie auf den Kampagnennamen.

## Berichterstellung für einzelne Kampagnen {#single-campaign-reporting}

Innerhalb einer Kampagne können Daten nach Kampagnenentität gefiltert werden: [!UICONTROL Packages], [!UICONTROL Placements]und [!UICONTROL Ads]. Sie können [die sichtbaren Daten filtern](campaign-data-filter.md) , um nur die Pakete, Platzierungen oder Anzeigen einzuschließen, die Sie sehen möchten.

![Tabs zur Kampagnenentität](/help/dsp/assets/campaign-subtabs.png)

In jeder Entitäts-Registerkarte enthält jede Zeile standardmäßig Pacing- und Versandmetriken. Sie können jedoch [Spaltenansicht ändern](column-view-change.md) oder sogar [Erstellen einer benutzerdefinierten Spaltenansicht](column-view-create.md) auf alle Unterregisterkarten der Kampagne anwenden. Sie können [Datentabellen anpassen](campaign-data-views-about.md) auf zusätzliche Weise. Jede Datentabelle enthält eine [!UICONTROL Subtotals] -Zeile, die entweder die Summe oder den Durchschnittswert jeder Metrik über alle sichtbaren Zeilen hinweg anzeigt.

Sie können für jede Kampagne auch Trend-Diagramme für Zeitreihen mit drei Metriken anpassen, die in jeder Entitätsansicht verfügbar sind. Standardmäßig werden Daten für [!UICONTROL Net Spend], [!UICONTROL Impressions]und [!UICONTROL Net CPM] sind in separaten Diagrammen (Trellis-Diagrammen) enthalten. Sie können die Metriken optional ändern.

![Trends für drei Metriken trennen](/help/dsp/assets/trend-chart-separate.png)

Sie können die drei Metriken optional auch überlagern, um Anomalien und Bereiche zu erkennen, in denen Skalierung oder Leistung verbessert werden können.

![Trenddiagramm mit Überlagerung](/help/dsp/assets/trend-chart.png)

Sie können [Trenddiagramme anpassen](campaign-data-visualization-manage.md) nach Kampagne, und die gleichen Metriken werden in allen Trenddiagrammen für die Kampagne beibehalten.

### Platzierungsinspektor

Für jede Platzierung können Sie [Öffnen einer (Detailansicht) [!UICONTROL Inspector])](placement-details-view.md), der die folgenden detaillierten Daten enthält:

* **[!UICONTROL Sites]:** Alle Sites, auf denen die Platzierung Impressionen gehabt hat.

   Die [!UICONTROL Sites] Registerkarte enthält Such- und Filterfunktionen, dieselben standardmäßigen und benutzerdefinierten Spaltenansichtsoptionen, die auf der Hauptseite verfügbar sind, und eine [!UICONTROL Exclude] in jeder Zeile, damit Sie eine Site schnell aus der Platzierung ausschließen können.

* **[!UICONTROL Ads]:** Alle Anzeigen in der Platzierung.

   Die [!UICONTROL Ads] enthält Such- und Filterfunktionen, dieselben standardmäßigen und benutzerdefinierten Spaltenansichtsoptionen, die auf der Hauptseite verfügbar sind, und Schnellaktionsschaltflächen in jeder Zeile, z. B. [!UICONTROL Pause] (sodass Sie eine Anzeige schnell anhalten können).

* **[!UICONTROL Frequency]:** Daten für jede Anzeigenfrequenzebene für die Platzierung, einschließlich:
   * die Häufigkeit der Anzeige (z. B. &quot;1&quot;für alle Instanzen, in denen Benutzer eine Anzeige einmal gesehen haben);
   * die geschätzte eindeutige Anzahl von Geräten/Browsern oder Personen (je nach spezifiziertem [!UICONTROL Cross Device Level] für die Platzierung), die Impressionen auf der angegebenen Frequenzebene erhalten haben
   * die geschätzte Anzahl von Impressionen auf der angegebenen Frequenzebene
   * die geschätzte Durchschnittshäufigkeit für das angegebene Frequenzniveau. Dieser Wert ist gleich (Geschätzte Impressionen)/(Geschätzte Individuen).

![Platzierungsinspektor](/help/dsp/assets/placement-inspector-sites.png)

Sie können die Daten im [!UICONTROL Sites], [!UICONTROL Ads]oder [!UICONTROL Frequency] zum standardmäßigen Download-Ordner Ihres Browsers als Bericht im XLSM-Format.

### Sonstige Berichtstypen auf Kampagnenebene

Für andere Datenaufschlüsselungen anzeigen [Legacy-Berichtsseiten auf Kampagnenebene](/help/dsp/campaign-management/campaigns/campaign-view-report.md) von [!UICONTROL Campaigns Classic]. Der alte Bericht enthält Abschnitte zu [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability]und [!UICONTROL Audience Performance] Daten.

>[!MORELIKETHIS]
>
>* [Anzeigen von Sites, Anzeigen und Frequenzdetails für eine Platzierung](placement-details-view.md)
>* [Über Datenansichten in Campaign](campaign-data-views-about.md)
>* [Benutzerdefinierte Spaltenansicht erstellen](column-view-create.md)
>* [Spaltenansicht ändern](column-view-change.md)
>* [Datenvisualisierungen verwalten](campaign-data-visualization-manage.md)
>* [Daten aus einer Kampagnenverwaltungsansicht exportieren](campaign-export-data.md)
>* [Detaillierte Berichte für eine Kampagne anzeigen](/help/dsp/campaign-management/campaigns/campaign-view-report.md)

