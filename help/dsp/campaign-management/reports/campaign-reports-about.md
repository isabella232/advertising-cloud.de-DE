---
title: Über In-Platform-Berichte
description: Erfahren Sie mehr über die Berichtsdaten in den Kampagnenverwaltungsansichten.
feature: DSP Campaign Data Views
exl-id: e9f7dafe-e0db-4fec-bf5b-858cbcfdde45
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 0%

---

# Über In-Platform-Berichte

<!-- rename "About Performance Reports in Campaign Management Views?" -->
Die Ansichten der Kampagnenverwaltung beinhalten umfassende Berichtdaten. Die verfügbaren Berichte helfen Ihnen dabei, die Pakete und Platzierungen zu identifizieren, die eine gute Leistung erbringen, und jene, die Ihre Aufmerksamkeit benötigen. Schnellaktion-Schaltflächen machen Sie auch produktiver.

## Liste aller Kampagnen

Die [!UICONTROL Campaigns]-Ansicht öffnet eine Liste aller Kampagnen in Ihrem Konto. Die Zeile [!UICONTROL Subtotals] zeigt entweder die Summe oder den Durchschnittswert jeder Metrik für alle sichtbaren Zeilen an.

![Kampagnenliste](/help/dsp/assets/campaigns-list.png)

Standardmäßig enthält jede Kampagnenzeile die Geschwindigkeit und Versandmetriken. Zu den Aktionsmetriken gehören [!UICONTROL Gross Spend (Lifetime)], die eine Messung der tatsächlichen On-Target-Ausgaben im Vergleich zu den erwarteten On-Target-Ausgaben für alle Kampagnenkits enthalten, sodass Sie leistungsschwache Kampagnen auf einen Blick erkennen können. Sie können optional [die Spaltenansicht](column-view-change.md) ändern oder sogar [eine benutzerdefinierte Spaltenansicht](column-view-create.md) erstellen.

Sie können [die Datentabellen](campaign-data-views-about.md) auf zusätzliche Weise weiter anpassen und [die sichtbaren Daten filtern](campaign-data-filter.md).

Um eine Kampagne detaillierter anzuzeigen, klicken Sie auf den Kampagnennamen.

## Berichterstellung für einzelne Kampagnen

Innerhalb einer Kampagne können Daten nach Kampagnenentität gefiltert werden: [!UICONTROL Packages], [!UICONTROL Placements] und [!UICONTROL Ads]. Sie können die sichtbaren Daten [ weiter filtern, um nur die Pakete, Platzierungen oder Anzeigen einzuschließen, die Sie sehen möchten.](campaign-data-filter.md)

![Tabs zur Kampagnenentität](/help/dsp/assets/campaign-subtabs.png)

In jeder Entitäts-Registerkarte enthält jede Zeile standardmäßig Geschwindigkeit- und Versandmetriken. Sie können jedoch [die Spaltenansicht](column-view-change.md) ändern oder sogar [eine benutzerdefinierte Spaltenansicht](column-view-create.md) erstellen, um sie auf alle Unterregisterkarten für die Kampagne anzuwenden. Sie können [die Datentabellen](campaign-data-views-about.md) auf zusätzliche Weise weiter anpassen. Jede Datentabelle enthält eine Zeile [!UICONTROL Subtotals], die entweder die Summe oder den Durchschnittswert jeder Metrik für alle sichtbaren Zeilen anzeigt.

Sie können für jede Kampagne auch Trend-Diagramme für Zeitreihen mit drei Metriken anpassen, die in jeder Entitätsansicht verfügbar sind. Standardmäßig sind Daten für [!UICONTROL Net Spend], [!UICONTROL Impressions] und [!UICONTROL Net CPM] in separaten Diagrammen (Trellis-Diagrammen) enthalten. Sie können die Metriken optional ändern.

![Trends für drei Metriken trennen](/help/dsp/assets/trend-chart-separate.png)

Sie können die drei Metriken optional auch überlagern, um Anomalien und Bereiche zu erkennen, in denen Skalierung oder Leistung verbessert werden können.

![Trenddiagramm mit Überlagerung](/help/dsp/assets/trend-chart.png)

Sie können [die Trenddiagramme](campaign-data-visualization-manage.md) nach Kampagne anpassen. Dieselben Metriken werden für alle Trenddiagramme der Kampagne beibehalten.

### Platzierungsinspektor

Für jede Platzierung können Sie [eine (Detailansicht [!UICONTROL Inspector])](placement-details-view.md) öffnen, die die folgenden detaillierten Daten enthält:

* **[!UICONTROL Sites]:** Alle Sites, auf denen die Platzierung Impressionen gehabt hat.

   Die Registerkarte [!UICONTROL Sites] enthält Such- und Filterfunktionen, dieselben standardmäßigen und benutzerdefinierten Spaltenansichtsoptionen, die auf der Hauptseite verfügbar sind, und eine [!UICONTROL Exclude]-Schaltfläche in jeder Zeile, damit Sie eine Site schnell von der Platzierung ausschließen können.

* **[!UICONTROL Ads]:** Alle Anzeigen in der Platzierung.

   Die Registerkarte [!UICONTROL Ads] enthält Such- und Filterfunktionen, dieselben standardmäßigen und benutzerdefinierten Spaltenansichtsoptionen, die auf der Hauptseite verfügbar sind, und Schnellaktionsschaltflächen in jeder Zeile, z. B. [!UICONTROL Pause] (damit Sie eine Anzeige schnell anhalten können).

* **[!UICONTROL Frequency]:** Daten für jede Anzeigenfrequenzebene für die Platzierung, einschließlich:
   * die Häufigkeit der Anzeige (z. B. &quot;1&quot;für alle Instanzen, in denen Benutzer eine Anzeige einmal gesehen haben);
   * die geschätzte eindeutige Anzahl von Geräten/Browsern oder Personen (abhängig von der angegebenen [!UICONTROL Cross Device Level] für die Platzierung), die Impressionen auf der angegebenen Frequenzebene erhalten haben
   * die geschätzte Anzahl von Impressionen auf der angegebenen Frequenzebene
   * die geschätzte Durchschnittshäufigkeit für das angegebene Frequenzniveau. Dieser Wert ist gleich (Geschätzte Impressionen)/(Geschätzte Individuen).

![Platzierungsinspektor](/help/dsp/assets/placement-inspector-sites.png)

Sie können die Daten auf den Registerkarten [!UICONTROL Sites], [!UICONTROL Ads] oder [!UICONTROL Frequency] als Bericht im XLSM-Format in den standardmäßigen Download-Ordner Ihres Browsers exportieren.

### Sonstige Berichtstypen auf Kampagnenebene

Sehen Sie sich für andere Datenaufschlüsselungen [die veralteten Berichtsseiten auf Kampagnenebene](/help/dsp/campaign-management/campaigns/campaign-view-report.md) von [!UICONTROL Campaigns Classic] an. Der alte Bericht enthält Abschnitte zu [!UICONTROL Geography], [!UICONTROL Device], [!UICONTROL Viewability] und [!UICONTROL Audience Performance] -Daten.

>[!MORELIKETHIS]
>
>* [Anzeigen von Sites, Anzeigen und Frequenzdetails für eine Platzierung](placement-details-view.md)
>* [Über Datenansichten in Campaign](campaign-data-views-about.md)
>* [Benutzerdefinierte Spaltenansicht erstellen](column-view-create.md)
>* [Spaltenansicht ändern](column-view-change.md)
>* [Datenvisualisierungen verwalten](campaign-data-visualization-manage.md)
>* [Daten aus einer Kampagnenverwaltungsansicht exportieren](campaign-export-data.md)
>* [Detaillierte Berichte für eine Kampagne anzeigen](/help/dsp/campaign-management/campaigns/campaign-view-report.md)

