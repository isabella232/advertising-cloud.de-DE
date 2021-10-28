---
title: Über In-Platform-Berichte
description: Erfahren Sie mehr über die Berichtsdaten in den Kampagnenverwaltungsansichten.
feature: DSP Campaign Data Views
exl-id: e9f7dafe-e0db-4fec-bf5b-858cbcfdde45
source-git-commit: 8814d14667f3ba1517fafcefcf2c095b89ba7493
workflow-type: tm+mt
source-wordcount: '931'
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

Sie können für jede Kampagne auch Trend-Diagramme für Zeitreihen mit drei Metriken anpassen, die in jeder Entitätsansicht verfügbar sind. Standardmäßig werden Daten für [!UICONTROL Net Spend], [!UICONTROL Impressions]und [!UICONTROL Net CPM] sind in separaten Diagrammen (Trellis-Diagrammen) enthalten. Sie können die Metriken optional ändern. Um stündliche Daten in Trend-Diagrammen für Zeitreihen zu aktivieren, ändern Sie Ihre Datumsauswahl auf einen einzelnen Tag (heute, gestern oder einen bestimmten Tag).

![Trends für drei Metriken trennen](/help/dsp/assets/trend-chart-separate.png)

Sie können die drei Metriken optional auch überlagern, um Anomalien und Bereiche zu erkennen, in denen Skalierung oder Leistung verbessert werden können.

![Trenddiagramm mit Überlagerung](/help/dsp/assets/trend-chart.png)

Sie können [Trenddiagramme anpassen](campaign-data-visualization-manage.md) nach Kampagne, und die gleichen Metriken werden in allen Trenddiagrammen für die Kampagne beibehalten.

### Platzierung [!UICONTROL Inspector] {#placement-inspector}

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

* **[!UICONTROL Inventory]:** Informationen zu allen Angeboten, die auf die Platzierung ausgerichtet sind.

   Die [!UICONTROL Inventory] enthält Such- und Filterfunktionen, dieselben standardmäßigen und benutzerdefinierten Spaltenansichtsoptionen, die auf der Hauptseite verfügbar sind, und Schnellaktionsschaltflächen in jeder Zeile, z. B. [!UICONTROL Edit] und [!UICONTROL View Report]. Die [!UICONTROL Inventory] -Registerkarte ermöglicht die schnelle Fehlerbehebung, indem Leistungsstatistiken angezeigt werden, z. B. [!UICONTROL Auctions], [!UICONTROL Bids]und [!UICONTROL Win Rate].

#### Fehlerbehebung beim Inventar

| Problem | Mögliche Ursache | Maßnahmen |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | Der Herausgeber hat nicht damit begonnen, Angebotsanfragen zu senden. | Wenden Sie sich an den Herausgeber, um den Deal zu aktivieren. |
|  | Das Geschäft wurde falsch eingerichtet, z. B. durch Eingabe einer falschen externen Deal-ID. | Bestätigen Sie die Geschäftsdetails und bearbeiten Sie den Deal. |
| [!UICONTROL Auctions but no Bids] | Das Platzierungs-Targeting stimmt nicht mit den eingehenden Angebotsanfragen für den Deal überein. <br><br> Eine Platzierung könnte beispielsweise auf eine Region ausgerichtet sein, die für den Deal nicht infrage kommt. | Bearbeiten Sie die Platzierungsziele nach Bedarf, um Targeting-Inkongruenzen zu vermeiden. |
|  | Die Platzierung verfügt nicht über eine aktive Anzeige mit dem erforderlichen Medientyp für das Geschäft. | Erstellen Sie eine Anzeige mit dem richtigen Medientyp und fügen Sie sie an die Platzierung an. |
|  | Die Platzierung hat kein angemessenes Budget. | Erhöhen Sie das Platzierungsbudget, um Gebote für eingehende Anforderungen zu ermöglichen. |
|  | Die Platzierungs-Flugdaten überschneiden sich nicht mit den Impressions-Sendedaten für den Deal. | Bearbeiten Sie bei Bedarf die Flugdaten der Platzierung. |
| [!UICONTROL Low Win Rate] | Das Höchstgebot der Platzierung (Untergrenze oder Festbetrag) liegt unter dem für das Geschäft erforderlichen Minimum. | Erhöhen Sie die [!UICONTROL Max Bid] nach Bedarf. |
|  | Die Platzierung verwendet Filter vor dem Angebot, die das Angebot einschränken. | Verringern Sie die Schwellenwerte der Filter vor dem Angebot, um mehr Gebote zu ermöglichen. |
|  | Das Zielgruppen-Targeting für die Platzierung ist zu restriktiv. | Überprüfen Sie, ob die angegebenen Zielgruppen über ausreichend aktive Benutzer verfügen, und erweitern Sie die Zielgruppe nach Möglichkeit. |

![Platzierungsinspektor](/help/dsp/assets/placement-inspector.png)

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

