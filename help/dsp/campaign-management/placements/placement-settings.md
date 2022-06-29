---
title: Platzierungseinstellungen
description: Siehe Beschreibungen der verfügbaren Platzierungseinstellungen.
feature: DSP Placements
exl-id: 36097132-e589-4d49-bf86-54f61eae5b67
source-git-commit: 8b1ae7385d7747f7073448aae5ad0a617f323562
workflow-type: tm+mt
source-wordcount: '3277'
ht-degree: 0%

---

# Platzierungseinstellungen

## [!UICONTROL Basics]

**[!UICONTROL Placement name]** Der Platzierungsname.

>[!TIP]
>Verwenden Sie eine Benennungskonvention, die für Ihre Situation sinnvoll ist. Eine empfohlene Benennungskonvention ist &quot;*\&lt;campaign name=&quot;&quot;>: \&lt;ad unit=&quot;&quot;>: \&lt;duration>: \&lt;targeting>*.&quot;

**[!UICONTROL Status]:** Der Platzierungsstatus: *[!UICONTROL Active]* (Standardeinstellung) oder *[!UICONTROL Paused]*.

>[!TIP]
>Die Best Practice besteht darin, die Platzierung so lange anzuhalten, bis Sie bereit sind, sie zu starten.

**[!UICONTROL Details]:** (Schreibgeschützt) Der anwendbare Anzeigentyp, das Konto, das die Platzierung erstellt oder erstellt hat, und die übergeordnete Kampagne. Um weitere Details anzuzeigen, klicken Sie auf **[!UICONTROL Show more]**.

**[!UICONTROL Templates]:** Öffnet eine Liste vorhandener Platzierungsvorlagen. So füllen Sie die Targeting-Einstellungen aus einer Vorlage automatisch aus:

1. Führen Sie einen der folgenden Schritte aus:

   * Um alle Zielgruppen aus einer Vorlage wiederzuverwenden, aktivieren Sie das Kontrollkästchen neben dem Vorlagennamen.

   * Um einzelne Zieltypen einer Vorlage wiederzuverwenden, erweitern Sie den Vorlagennamen und aktivieren Sie das Kontrollkästchen neben den Zieltypen, die Sie wiederverwenden möchten.

1. Klicken **[!UICONTROL Apply]**.

**[!UICONTROL Ad specs for forecast]:** (Nur Videoanzeigenformate) Die Anzeigendauer und/oder Anzeigenspezifikationen, die zur Berechnung der Prognoseprojektion auf der rechten Seite verwendet werden. Die Felder variieren je nach Anzeigentyp.

**[!UICONTROL Placement tags]:** (Optional) Keywords oder Spitznamen, die Sie bei der Suche nach dieser Platzierung unterstützen.

## Ziele

**[!UICONTROL Package]:** (Optional) Ein Paket, dem die Platzierung zugewiesen ist. Klicken ![Bearbeiten](/help/dsp/assets/edit.png) , um ein vorhandenes Paket auszuwählen oder ein neues zu erstellen. Wenn Sie die Platzierung einem Paket zuweisen, wird die [!UICONTROL Goals] -Abschnitt mit den Flugdaten, dem Versandziel und dem Budget des Pakets aktualisiert.

**[!UICONTROL Flight Dates]:** Das Start- und Enddatum für die Platzierung. Genehmigte Anzeigen können während des Fluges ausgeführt werden, wenn die Platzierung aktiv ist und einem aktiven Paket oder einer aktiven Kampagne zugewiesen wird.

Die Daten für das Paket (falls zutreffend) oder die Kampagne werden standardmäßig automatisch ausgefüllt.

>[!NOTE]
>
>* Die Fluchtdaten müssen innerhalb der Kampagnendaten und der Pauschalflugdaten enthalten sein.


### Platzierungen, die Paketen mit Geschwindigkeit auf Paketebene zugewiesen sind

**[!UICONTROL Placement Funding]:** Budget für die Platzierung:

* *[!UICONTROL Optimize based on performance]:* Steuert das Budget auf Paketebene.
* *[!UICONTROL Set a fixed budget cap]:* Ermöglicht die Festlegung eines täglichen, wöchentlichen, monatlichen oder ganzzeitbasierten Platzierungsbudgets. Geben Sie einen Wert und die Dauer ein (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Max Bid]:** Das Maximum für 1000 Impressionen.

**[!UICONTROL Placement Pre-bid Filters]:** Bis zu fünf KPI-Schwellenwerte (z. B. eine minimale Sichtbarkeitsmetrik oder Clickthrough-Rate), die erfüllt sein müssen, damit Angebote unterbreitet werden können. Sie können als Optimierungstaktiken Pre-Gebot-Filter verwenden, aber Sie wissen, dass jede Regel die Möglichkeiten einschränken kann, für die diese Platzierung Gebote abgeben kann. So fügen Sie Filter hinzu oder bearbeiten sie:

1. Klicken ![Bearbeiten](/help/dsp/assets/edit.png).
1. Führen Sie einen der folgenden Schritte aus:
   * So fügen Sie einen Filter hinzu:
      1. Klicken **[!UICONTROL Add Filter]**.
      1. Weiter zu **[!UICONTROL Only bid if]**, wählen Sie eine Metrik aus und geben Sie einen Wert ein.
   * Um einen Filter zu entfernen, klicken Sie auf **[!UICONTROL X]** in der Filterzeile.
1. Klicken **[!UICONTROL Save]**.

Siehe Beschreibungen der einzelnen Filter vor dem Angebot unter[Vorab-Angebotsfilter auf Platzierungsebene und deren Verwendung](/help/dsp/optimization/optimization-pre-bid-filters.md).&quot;

### Alle anderen Platzierungen

**[!UICONTROL Budget Goal]:** Die Bruttohaushaltsobergrenze und das Budgetintervall (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Gross Budget Goal]:** (Nur Platzierungen in Kampagnen mit Margenverwaltung) Die Obergrenze des Bruttobudgets und das Budgetintervall (*[!UICONTROL All time]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]*).

**[!UICONTROL Optimization Goal]:**  Das Optimierungsziel für das Paket. Beschreibungen der einzelnen Optimierungsziele finden Sie unter[Optimierungsziele und Verwendung](/help/dsp/optimization/optimization-goals.md)&quot;.

**[!UICONTROL Target Goal]:** Das Zielziel, das zum Tracking der Leistung verwendet wird.

>[!NOTE]
>
>Dieses Feld ist nur ein Benchmark und wird nicht für die Entscheidungsfindung verwendet.

**[!UICONTROL Pace on]:** Auf welcher Geschwindigkeit basiert:

* **[!UICONTROL Budget goal]:** (Standard) Diese Option liefert so viele Impressionen wie möglich innerhalb des zugewiesenen Budgets.

* **[!UICONTROL Impressions]:** Diese Option liefert Impressionen, bis eine angegebene Menge innerhalb eines bestimmten Intervalls erreicht wird. Wenn Sie diese Option auswählen, geben Sie die Anzahl der Impressionen und das Intervall an: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* oder *[!UICONTROL Weekly]*.

**[!UICONTROL Max Bid]:** Das Maximum für 1000 Impressionen.

**[!UICONTROL Pacing Fill Strategy]:** (Nur Pakete mit Geschwindigkeit auf Paketebene) So beschleunigen Sie die Anzeigenbereitstellung:

* *[!UICONTROL Even]:* (Standardeinstellung) Die Auslieferung erfolgt gleichmäßig über jeden Flug hinweg, wobei die Zielgruppe 50 % des Versands in der ersten Flughälfte beträgt.

* *[!UICONTROL Frontload]:* Beschleunigt den Versand, sodass er zur Hälfte des Fluges zu 65-75 % vollständig ist.

* *[!UICONTROL Aggressive Frontload]:* Beschleunigt die Auslieferung, sodass 75-85 % der gesamten Flugzeit vollständig sind.

**[!UICONTROL Placement Pre-bid Filters]:** (Optional) Bis zu fünf Filter, die erfüllt sein müssen, damit Angebote unterbreitet werden können. Sie können als Optimierungstaktiken Vorgebotsfilter verwenden. Beachten Sie jedoch, dass jede Regel die Möglichkeiten einschränken kann, für die diese Platzierung Gebote abgeben kann. So fügen Sie Filter hinzu oder bearbeiten sie:

1. Klicken ![Bearbeiten](/help/dsp/assets/edit.png).
1. Führen Sie einen der folgenden Schritte aus:
   * So fügen Sie einen Filter hinzu:
      1. Klicken **[!UICONTROL Add Filter]**.
      1. Weiter zu **[!UICONTROL Only bid if]**, wählen Sie eine Metrik aus und geben Sie einen Wert ein.
   * Um einen Filter zu entfernen, klicken Sie auf **[!UICONTROL X]** in der Filterzeile.
1. Klicken **[!UICONTROL Save]**.

## [!UICONTROL Geo-Targeting]

**[!UICONTROL Audience Location]:** (Optional) Bestimmte Orte, an denen Anzeigen in die Platzierung ein- oder ausgeschlossen werden sollen. Wenn Sie keine Orte angeben, werden alle Orte als Ziel ausgewählt.

>[!NOTE]
>
>Orte für Stadt und DMA sind nicht für Roku-Platzierungen verfügbar.

So legen Sie Speicherorte fest:

1. Klicken ![Bearbeiten](/help/dsp/assets/edit.png).
1. Führen Sie einen der folgenden Schritte aus:
   * Ein- oder Ausschließen eines Landes, eines Bundesstaates, einer Stadt, DMA, eines Bundesgesetzbezirks oder eines Landbezirks
      1. Wählen Sie den Positionstyp in der linken Spalte aus.
      1. (Nach Bedarf) Klicken Sie auf einen Ort, um ihn zu erweitern.
      1. Klicken Sie neben dem Standort auf *[!UICONTROL Include]* , um ihn als Ziel einzubeziehen, oder *[!UICONTROL Exclude]* , um ihn als Zielgruppe auszuschließen.
   * So suchen Sie nach einer Postleitzahl und schließen alle ausgewählten Ergebnisse ein oder aus:
      1. Klicken **[!UICONTROL Search Postal Code]**.
      1. Wählen Sie das Land aus.
      1. Geben Sie den Stadt-Namen ein und klicken Sie auf ![Bearbeiten](/help/dsp/assets/search.png).
      1. Klicken Sie auf das richtige Suchergebnis.
      1. Klicken *[!UICONTROL Include All]* , um alle Orte als Ziele einzubeziehen, oder *[!UICONTROL Exclude All]* , um alle Orte als Ziele auszuschließen.
   * So geben Sie Postleitzahlen ein oder fügen sie ein und schließen sie alle ein oder aus:
      1. Klicken **[!UICONTROL Paste Postal Code]**.
      1. Wählen Sie das Land aus.
      1. Geben Sie bis zu 1000 Postleitzahlen ein oder fügen Sie sie ein.
Fügen Sie eine Postleitzahl pro Zeile hinzu oder geben Sie mehrere Werte ein, die durch Kommas oder Tabs getrennt sind.
      1. Klicken *[!UICONTROL Include All]* , um alle Orte als Ziele einzubeziehen, oder *[!UICONTROL Exclude All]* , um alle Orte als Ziele auszuschließen.
   * So entfernen Sie einen Ort aus dem [!UICONTROL Included] oder [!UICONTROL Excluded] Liste, klicken Sie auf **[!UICONTROL X]** neben der Position in der rechten Spalte.
1. Klicken **[!UICONTROL Done]**.

>[!NOTE]
>
>* Nicht alle Länder verfügen über Standorte für Bundesland-, Stadt- oder Postleitzahlen.
>* DMA (Marktsegment), Federal Legislation Districts und State Legislation Districts sind nur für US-Standorte verfügbar.


## [!UICONTROL Inventory Targeting]

**[!UICONTROL Inventory Sources]:** Inventarquellen, die als Ziele ein- oder ausgeschlossen werden sollen. Bei den meisten Platzierungstypen sind standardmäßig alle Inventartypen und alle Quellen für jeden Typ enthalten. Für [!DNL Roku] Platzierungen, müssen Sie den Inventartyp und die Quellen angeben. Sie können aus den folgenden Lagerbestandsarten wählen:

* [!UICONTROL Public]: (Alle Platzierungstypen außer Roku) Alle offenen Exchange-Inventare, auf die Advertising Cloud Zugriff hat. Sie können das öffentliche Inventar einbeziehen und ausschließen.

   Sie können die Liste nach Quelle oder Feed anzeigen. Wenn Sie die Liste nach Feed anzeigen, können Sie nach Feed-Name, Feed-Schlüssel oder einem ausgewählten charakteristischen Tag suchen.

* [!UICONTROL Private] | [!UICONTROL Roku Private]: Ihre bestehenden privaten Geschäfte (oder vorhandenen privaten Geschäfte) [!DNL Roku] Angebote [!DNL Roku] Platzierungen) mit Herausgebern, die Sie in DSP eingerichtet haben. Sie können das öffentliche Inventar einbeziehen, aber nicht ausschließen.

   Sie können die Liste nach Keyword, Schlüssel, Deal-ID oder benutzerdefiniertem Tag durchsuchen.

* [!UICONTROL On Demand] | [!UICONTROL Roku On Demand]: Alle [Prämie, nicht garantiert [!UICONTROL On Demand] inventory](/help/dsp/inventory/on-demand-inventory-about.md) (oder [!UICONTROL On Demand] [!DNL] Roku-Angebote für [!DNL Roku] Platzierungen), für die Sie sich angemeldet haben [!DNL DSP]. Sie können [!UICONTROL On Demand] Inventar.

   Sie können die Liste nach Quelle oder Feed anzeigen. Wenn Sie die Liste nach Feed anzeigen, können Sie nach Feed-Name, Feed-Schlüssel oder einem ausgewählten Publisher-Bereich, Kategorie-Tag oder charakteristischen Tag suchen.

So legen Sie das Inventar-Targeting fest:

* Um einen Inventartyp auszuschließen, deaktivieren Sie das Kontrollkästchen neben dem Namen.
* So wählen Sie einen Inventartyp aus:
   1. Aktivieren Sie das Kontrollkästchen neben dem Inventartypnamen.
   1. (Optional) Ändern Sie die Quellen, um Folgendes einzuschließen:
      1. Klicken ![Bearbeiten](/help/dsp/assets/edit.png).
      1. ([!UICONTROL Public] und [!UICONTROL On Demand] inventory) Click *[!UICONTROL *View by Source]** oder **[!UICONTROL View by Feed]** , um zu ändern, wie die Quellen aufgelistet werden.
      1. (Falls zutreffend) Filtern Sie den Bestand nach Bedarf.
      1. Geben Sie die Quellen an, die ein- und ausgeschlossen werden sollen:
         * So fügen Sie eine [!UICONTROL Public] oder [!UICONTROL On Demand] Quelle, klicken **[!UICONTROL Include]** neben dem Quellnamen.
         * Einbeziehen [!UICONTROL Private] Quellen:
            * Um den gesamten Bestand in einen Deal einzubeziehen, klicken Sie auf **[!UICONTROL Include all]** neben dem Namen des Deals.
            * Um eine einzelne Inventarquelle einzubeziehen, erweitern Sie den Namen des Deals und klicken Sie dann auf das Kontrollkästchen neben dem Quellnamen.
         * So schließen Sie eine [!UICONTROL Public] oder [!UICONTROL On ] Quelle, klicken **[!UICONTROL Exclude]** neben dem Quellnamen.
   1. (Optional) Um eine CSV-Datei mit den Targeting-Informationen zum Speicherort der Downloads Ihres Browsers herunterzuladen, klicken Sie auf **[!UICONTROL Save & Export]**.
   1. Klicken **[!UICONTROL Save]**.

>[!TIP]
>
>Wenn Sie sich für [!UICONTROL On Demand] Inventar, kann aber die Herausgeber oder Angebote nicht finden, um die Zielgruppe zu erreichen, und dann den Status der Angebote überprüfen. Weitere Informationen zu Status finden Sie unter [Info [!DNL On Demand] Premium-Lagerbestand](/help/dsp/inventory/on-demand-inventory-about.md).

**[!UICONTROL Exclude out-stream]:** (Nur Videoplatzierungen) Schließt ausgehender Traffic aus.

Über dem Inhalt angezeigte Werbeanzeigen werden in der Regel als Popup oder als Inhaltsangabe (im nativen Erlebnis) und nicht als normale Videoanzeigen in einem Videoplayer angezeigt.

## [!UICONTROL Site Targeting]

**[!UICONTROL Traffic type]:** Die Traffic-Typen für die Zielgruppe. Optionen umfassen **[!UICONTROL Websites]** und **[!UICONTROL Apps]**.

**[!UICONTROL Site tier]:** (Verfügbar, wenn **[!UICONTROL Paste list of targeted sites]** is *[!UICONTROL Off]*) Die Qualität der Zielseiten. Die Ebenen 1-3 sind alle markensicher und wurden vom DSP-Zuordnungsteam geprüft und genehmigt.

* *[!UICONTROL Tier 1]:* Premium-Sites und -Anwendungen, die national erkennbar sind.
* *[!UICONTROL Tier 2]:* Tier 1-Ziele sowie Qualitäts-Sites und -Anwendungen, die weniger weit als Tier 1 bekannt sind.
* *[!UICONTROL Tier 3]:* Zielebenen 1-2 sowie legitime und markensichere Websites und Anwendungen, die für eine Nische-Audience geeignet sind. Verwenden Sie Ebene 3 für Zielgruppen- oder Daten-Targeting-Käufe.
* *[!UICONTROL All Sites]:* Zielebenen 1-3 und neues Inventar, das nicht geprüft oder kategorisiert wurde und das Sie für die Reichweite verwenden können.

>[!NOTE]
>
>Der Bestand ist spezifisch für die Anzeigeneinheiten in der Platzierung.

>[!TIP]
>
>Für Leistungskampagnen empfiehlt es sich, *[!UICONTROL All Sites]*.

**[!UICONTROL Site Categories]:** (Optional) verfügbar **[!UICONTROL Paste list of targeted sites]** is *[!UICONTROL Off]*) Sitekategorien innerhalb der ausgewählten Siteebenen, die entweder als Ziele ein- oder ausgeschlossen werden sollen (aber nicht beide). Wählen Sie aus den vertikalen Site-Listen, die Advertising Cloud basierend auf dem Site-Betreff zugeordnet hat:

1. Klicken ![Bearbeiten](/help/dsp/assets/edit.png).
1. Geben Sie die Site-Kategorien an, die entweder ein- oder ausgeschlossen werden sollen:
   * So fügen Sie Site-Kategorien hinzu:
      1. Klicken **[!UICONTROL Include categories]**.
      1. Aktivieren Sie das Kontrollkästchen neben den jeweiligen Kategorien, die als Ziel ausgewählt werden sollen.
   * So schließen Sie Site-Kategorien aus:
      1. Klicken **[!UICONTROL Exclude categories]**.
      1. Aktivieren Sie das Kontrollkästchen neben den Kategorien, die ausgeschlossen werden sollen.
1. (Optional) Um eine CSV-Datei mit den Targeting-Informationen zum Speicherort der Downloads Ihres Browsers herunterzuladen, klicken Sie auf **[!UICONTROL Export]**.
1. Klicken **[!UICONTROL Save]**.

**[!UICONTROL Exclude Sites]:** (Optional) verfügbar **[!UICONTROL Paste list of targeted sites]** is *[!UICONTROL Off]*) Auszuschließende Sites. Sie können entweder nach Sites suchen und diese auswählen oder Domänennamen eingeben oder einfügen:

1. Klicken ![Bearbeiten](/help/dsp/assets/edit.png).
1. Geben Sie die Sites an:
   * So suchen Sie nach einer Site:
      1. Klicken **[!UICONTROL Search]**.
      1. Geben Sie einen Suchbegriff ein, wählen Sie eine Site-Ebene und/oder wählen Sie eine Site-Kategorie aus.
      1. Wählen Sie in den Suchergebnissen die Sites aus, die ausgeschlossen werden sollen:
         * Um eine einzelne Site auszuschließen, aktivieren Sie das Kontrollkästchen daneben.
         * (Wenn mehr als 50 Ergebnisse verfügbar sind) Um die ersten 50 Ergebnisse auszuschließen, klicken Sie auf **[!UICONTROL Exclude these 50]**. Um alle Suchergebnisse auszuschließen, klicken Sie auf **[!UICONTROL Exclude these \<*NN *\>]**.
   * So geben Sie Domänennamen ein:
      1. Klicken **[!UICONTROL Paste]**.
      1. Geben Sie einen oder mehrere Domänennamen in separate Zeilen ein.
      1. Klicken **[!UICONTROL Exclude All]**.
1. Klicken **[!UICONTROL Done]** wenn du fertig bist.

>[!NOTE]
>
>* Zusätzlich zum Advertising Cloud DSP werden auch Blockierungslisten auf Kontoebene und auf Advertiser-Ebene angewendet. [global gesperrte Site-Liste](/help/dsp/introduction/features/brand-safety-media-quality.md), einschließlich Sites, die für Anzeigen als unsicher gelten.
>* Listen blockierter Sites überschreiben immer Listen zielgerichteter Sites. Wenn durch eine Platzierung dieselbe Zielgruppe für eine Anzeige ausgeschlossen und einbezogen wird, wird die Zielgruppe ausgeschlossen.


**[!UICONTROL Language]:** (Optional) Eine Zielsprache.

**[!UICONTROL Site List Preview]:** (Schreibgeschützt) Alle zielgerichteten und blockierten Sites für die Platzierung.

Optional können Sie die Liste der Ziel- und Blockierungssites als CSV-Datei (CSV) mit kommagetrennten Werten exportieren. Um die Liste zu exportieren, klicken Sie auf **[!UICONTROL Export full site list]** und öffnen oder speichern Sie die Datei dann entsprechend der üblichen Vorgehensweise Ihres Browsers.

<!-- **[!UICONTROL Allow unscreened sites]:** (XXX placements only) Allows you to XXXX.   Optional available for https://advertising.adobe.com/configurator/placement/edit/2432022 -->

**[!UICONTROL Paste list of targeted sites]:** Ermöglicht es Ihnen, nur bestimmte Sites als Ziel festzulegen. Wenn Sie diese Option aktivieren, sind die anderen Site-Targeting-Optionen deaktiviert.

**[!UICONTROL Sites]:** (Verfügbar, wenn **[!UICONTROL Paste list of targeted sites]** is *[!UICONTROL On]*) Zu verwendende Sites. Sie können entweder nach Sites suchen und diese auswählen oder Domänennamen eingeben oder einfügen:

1. Klicken ![Bearbeiten](/help/dsp/assets/edit.png).
1. Geben Sie die Sites an:
   * So suchen Sie nach einer Site:
      1. Klicken **[!UICONTROL Search]**.
      1. Geben Sie einen Suchbegriff ein, wählen Sie eine Site-Ebene und/oder wählen Sie eine Site-Kategorie aus.
      1. Wählen Sie in den Suchergebnissen die Sites aus, die einbezogen werden sollen:
         * Um eine einzelne Site auszuschließen, aktivieren Sie das Kontrollkästchen daneben.
         * (Wenn mehr als 50 Ergebnisse verfügbar sind) Um die ersten 50 Ergebnisse einzubeziehen, klicken Sie auf **[!UICONTROL Include these 50]**. Um alle Suchergebnisse einzuschließen, klicken Sie auf **[!UICONTROL Include these \<*NN *\>]**.
   * So geben Sie Domänennamen ein:
      1. click **[!UICONTROL Paste]**.
      1. Geben Sie einen oder mehrere Domänennamen in separate Zeilen ein.
      1. Klicken **[!UICONTROL Include All]**.
1. Klicken **[!UICONTROL Done]**.

## [!UICONTROL Audience Targeting]

**[!UICONTROL Included Audiences]:** Alle Zielgruppenziele für die Platzierung, einschließlich [Drittanbietersegmente, Erstanbietersegmente, Adobe-Segmente, benutzerdefinierte Segmente und gespeicherte Zielgruppen](/help/dsp/audiences/audience-settings.md). Die gesamte und die aktive deduplizierte Zielgruppengröße für alle ausgewählten Segmente und gespeicherten Zielgruppen wird ebenfalls angezeigt. Sie können eine vorhandene Zielgruppe auswählen, eine neue Zielgruppe erstellen, die Sie später wiederverwenden können, oder bestimmte Zielgruppensegmente auswählen:

* Um eine existierende Zielgruppe auszuwählen, klicken Sie auf ![Auswählen](/help/dsp/assets/chevron-down.png) neben [!UICONTROL Included Audiences]und wählen Sie dann die Zielgruppe aus.
* Um eine neue Zielgruppe zu erstellen, klicken Sie auf ![Auswählen](/help/dsp/assets/chevron-down.png) neben [!UICONTROL Included Audiences]und wählen Sie **[!UICONTROL + Create Audience]**. Anweisungen finden Sie unter [Wiederverwendbare Zielgruppe erstellen](/help/dsp/audiences/reusable-audience-create.md), beginnend mit Schritt 3.
* Um bestimmte Zielgruppensegmente auszuwählen, klicken Sie auf **[!UICONTROL Select segments for this placement only]**. Wählen Sie die Segmentlogik aus. Anweisungen finden Sie in Schritt 6 unter &quot;[Wiederverwendbare Zielgruppe erstellen](/help/dsp/audiences/reusable-audience-create.md).&quot; Wenn Sie fertig sind, klicken Sie auf **Speichern**.

**[!UICONTROL Excluded Audiences]:** Alle Zielgruppen, die für die Platzierung ausgeschlossen werden sollen, einschließlich Zielgruppen mit [Drittanbietersegmente, Erstanbietersegmente, Adobe-Segmente, benutzerdefinierte Segmente und gespeicherte Zielgruppen](/help/dsp/audiences/audience-settings.md). Die gesamte und die aktive deduplizierte Zielgruppengröße für alle ausgeschlossenen Zielgruppen wird ebenfalls angezeigt. Sie können eine vorhandene Zielgruppe auswählen oder eine neue Zielgruppe erstellen, die Sie später wiederverwenden können:

* Um eine existierende Zielgruppe auszuwählen, klicken Sie auf ![Auswählen](/help/dsp/assets/chevron-down.png) neben [!UICONTROL Excluded Audiences]und wählen Sie dann die Zielgruppe aus.
* Um eine neue Zielgruppe zu erstellen, klicken Sie auf ![Auswählen](/help/dsp/assets/chevron-down.png) neben [!UICONTROL Excluded Audiences]und wählen Sie **+ Zielgruppe erstellen**. Anweisungen finden Sie unter [Wiederverwendbare Zielgruppe erstellen](/help/dsp/audiences/reusable-audience-create.md), beginnend mit Schritt 3.

**[!UICONTROL Cross Device Targeting]:** (Verfügbar, wenn Sie mindestens ein Segment oder eine Zielgruppe auswählen und die [Die Kampagne ist für benutzerbasiertes geräteübergreifendes Targeting konfiguriert.](/help/dsp/campaign-management/campaigns/campaign-settings.md). Ermöglicht die Erweiterung des Targetings auf alle bekannten Geräte einer Person (entsprechend dem in den Kampagneneinstellungen angegebenen Gerätediagramm), auch auf Geräte, die nicht in den angegebenen Segmenten enthalten sind. Die Gebühren können je nach dem für die Kampagne angegebenen Diagramm gelten. Gerätediagrammdaten sind derzeit nur in Nordamerika verfügbar.

**[!UICONTROL Placement Cap]:** (Optional) Die Häufigkeit, mit der ein eindeutiges Gerät oder eine eindeutige Person (je nach [!UICONTROL Cross Device Level]) werden Anzeigen von der Platzierung bereitgestellt. Optionen umfassen *[!UICONTROL Unlimited]* oder einen bestimmten Betrag pro Tag, Woche oder Monat.

>[!NOTE]
>
> Sie können Frequenzobergrenzen auf Kampagnen-, Paket- und Platzierungsebene festlegen. DSP respektiert die strengste Frequenzgrenze in der Kampagnenhierarchie.

**[!UICONTROL Secondary Cap]:** (Optional) verfügbar, wenn Sie eine numerische [!UICONTROL Placement Cap]) Eine zusätzliche Begrenzung innerhalb der Grenzen der primären Platzierungsbegrenzung. Wählen Sie die Anzahl der Impressionen und den Zeitraum aus (z. B. 3 pro 12 Stunden).

**[!UICONTROL Day Parting]:** (Optional) Bestimmte Wochentage und Tageszeit, an denen Anzeigen ausgeführt werden können. So legen Sie Dayparting-Intervalle fest:
1. Klicken ![Bearbeiten](/help/dsp/assets/edit.png).
1. Wählen Sie die gewünschte Zeitzone aus.
1. Geben Sie die Intervalle an:
   * Um ein voreingestelltes Intervall auszuwählen, klicken Sie auf eine der Intervallschaltflächen. Optionen umfassen *[!UICONTROL Weekends]**, *[!UICONTROL Weekdays]*, *[!UICONTROL Morning]*, *[!UICONTROL Lunch]*, *[!UICONTROL Dinner]* oder *[!UICONTROL Prime]* (primetime).
   * Um ein Intervall manuell auszuwählen, klicken Sie in eine Zelle und ziehen Sie optional, um das Intervall auszuwählen.
1. Klicken **[!UICONTROL Save]**.

**[!UICONTROL Topic Targeting]:** (Optional) für Advertiser verfügbar sein, die mit [!DNL Comscore] und [!DNL Grapeshot] Segmente) Spezifische Segmentnamen oder IDs von [!DNL Comscore] und [!DNL Grapeshot] , um als Ziele einzubeziehen. Für diese Funktion können zusätzliche Gebühren anfallen. Wenden Sie sich an Ihren [!DNL Adobe] Account-Team.

So legen Sie das Thema-Targeting fest:

1. Klicken ![Bearbeiten](/help/dsp/assets/edit.png).
1. Geben Sie die Zielsegmente an:
   1. Wählen Sie in der linken Spalte den Partner aus (*[!UICONTROL Comscore]* oder *[!UICONTROL Grapeshot]*).
   1. Geben Sie im Eingabefeld die Segmentnamen oder Segment-IDs ein.
1. (Optional) Um eine CSV-Datei mit den Themeninformationen zum Speicherort der Downloads Ihres Browsers herunterzuladen, klicken Sie auf **[!UICONTROL Export]**.
1. Klicken **[!UICONTROL Save]**.

>[!TIP]
>
>* Beim Thema-Targeting wird der Bestand begrenzt, für den die Platzierung ein Angebot machen kann. Verwenden Sie daher das Thema-Targeting nur für einen geringen Prozentsatz Ihres Gesamtkaufs.
>
>* Einrichten eines negativen Targetings innerhalb des Segments auf [!DNL Comscore] oder [!DNL Grapeshot].


**[!UICONTROL Device Targeting]:** (Optional) Spezifische Geräteinformationen, einschließlich Gerätetypen, Hersteller, Betriebssysteme, Browser und Konnektivitätstypen, die als Ziele ein- und ausgeschlossen werden. So legen Sie das Geräte-Targeting fest:

1. Klicken ![Bearbeiten](/help/dsp/assets/edit.png).
1. Geben Sie die Gerätedetails an, die ein- und ausgeschlossen werden sollen:
   1. Wählen Sie in der linken Spalte die Kategorie aus.
   1. Festlegen der Zielgruppenbestimmung:
      * Um einen Wert einzubeziehen, klicken Sie auf **[!UICONTROL Include]** neben dem Wertnamen.
      * Um einen Wert auszuschließen, klicken Sie auf **[!UICONTROL Exclude]** neben dem Wertnamen.
1. (Optional) Um eine CSV-Datei mit den Geräte-Targeting-Informationen zum Speicherort der Downloads Ihres Browsers herunterzuladen, klicken Sie auf **[!UICONTROL Export]**.
1. Klicken **[!UICONTROL Save]**.

**[!UICONTROL ISP Targeting]:** (Optional) Spezifische Internet-Dienstanbieter (ISPs), die als Ziele entweder ein- oder ausschließen (aber nicht beides). So legen Sie das ISP-Targeting fest:

1. Klicken ![Bearbeiten](/help/dsp/assets/edit.png).
1. Geben Sie die ISPs an, die ein- oder ausgeschlossen werden sollen:
   * So schließen Sie ISPs ein:
      1. Klicken **[!UICONTROL Include ISPs]**.
      1. (Optional) Filtern Sie die Liste nach Keyword.
      1. Aktivieren Sie das Kontrollkästchen neben den jeweiligen ISP, die als Ziel ausgewählt werden sollen.
   * So schließen Sie ISPs aus:
      1. Klicken **[!UICONTROL Exclude ISPs]**.
      1. (Optional) Filtern Sie die Liste nach Keyword.
      1. Aktivieren Sie das Kontrollkästchen neben jedem ISP, der ausgeschlossen werden soll.
1. (Optional) Um eine CSV-Datei mit den ISP-Targeting-Informationen zum Speicherort der Downloads Ihres Browsers herunterzuladen, klicken Sie auf **[!UICONTROL Export]**.
1. Klicken **[!UICONTROL Save]**.

## [!UICONTROL Brand Safety and Media Targeting]

**[!UICONTROL Contextual filtering]:** Typen [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]und [!DNL Peer39] anzuwendende Kontextfilter. Die Standardeinstellungen auf Advertiser-Ebene werden für neue Platzierungen ausgewählt, Sie können jedoch die Einstellungen ändern:

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block sites that are]:** (Optional) Ein oder mehrere Arten von Inventarkontext, der standardmäßig blockiert werden soll. Es können zusätzliche Gebühren erhoben werden.

* [!UICONTROL Peer 39]:

   * **Target-Sites, die:** (Optional) Ein oder mehrere Arten von Bestandsattributen, die standardmäßig als Ziel dienen sollen. Es können zusätzliche Gebühren erhoben werden.

* [!UICONTROL ComScore]:

   * **Blockieren Sie Sites, die:** (Optional) Ein oder mehrere Arten von Bestandsattributen, die standardmäßig blockiert werden sollen. Es können zusätzliche Gebühren erhoben werden.

* [!UICONTROL Integral Ad Science]

   * **[!UICONTROL Adult Content]:** (Optional) Der Grad des Erwachseneninhalts, für den Anzeigen standardmäßig blockiert werden sollen: *[!UICONTROL Do Not Block]* (Standardeinstellung), *[!UICONTROL Standard]* oder *[!UICONTROL Strict]*. Es können zusätzliche Gebühren erhoben werden.

   * **[!UICONTROL Alcohol Content]:** (Optional) Der Alkoholgehalt, für den Anzeigen standardmäßig blockiert werden sollen: *[!UICONTROL Do Not Block]* (Standardeinstellung), *[!UICONTROL Standard]* oder *[!UICONTROL Strict]*. Es können zusätzliche Gebühren erhoben werden.

**[!UICONTROL Pre-bid fraud blocking]:** Arten von zu blockierenden Websites auf der Grundlage von betrügerischem Traffic und verdächtigen Aktivitäten, die durch [!DNL DoubleVerify], [!DNL Integral Ad Science]und [!DNL Peer39]. Die Standardeinstellungen auf Advertiser-Ebene werden für neue Platzierungen ausgewählt, Sie können jedoch die Einstellungen ändern:

* [!UICONTROL DoubleVerify]:

   * **[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Standardmäßig werden alle 100 % ungültigen Traffic, einschließlich Traffic auf entführten Geräten, für neue Platzierungen blockiert. Es können zusätzliche Gebühren erhoben werden.

   * **[!UICONTROL Also block sites with]:** (Optional) Eine zusätzliche Stufe von Betrug und ungültigem Traffic, die dazu führt, dass DSP Anzeigen standardmäßig blockieren:  *[!UICONTROL None]* (Standardeinstellung, die zusätzlichen Traffic nicht blockiert), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* oder *[!UICONTROL >25% Average Fraud/IVT levels]*. Es können zusätzliche Gebühren erhoben werden.

* [!UICONTROL Peer 39]:

   * **[!UICONTROL Block sites that are]:** (Optional) Ein oder mehrere Arten von Betrug, durch den Anzeigen standardmäßig blockiert DSP: *[!UICONTROL Fraud]* (die alle betrügerischen Websites blockiert), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* und/oder *[!UICONTROL Fraud: Zero Ads]*. Es können zusätzliche Gebühren erhoben werden.

* [!UICONTROL Integral Ad Science]:

   * **[!UICONTROL Block sites that are]:** (Optional) Ein Typ von verdächtigen Website- oder App-Aktivitäten, der dazu führt, dass DSP Anzeigen standardmäßig blockieren: *[!UICONTROL None]* (die Standardeinstellung, die keine auf verdächtigen Aktivitäten basierenden Anzeigen blockiert), *[!UICONTROL Suspicious Activity - High Risk]* oder *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Es können zusätzliche Gebühren erhoben werden.

**[!UICONTROL Ads.txt filtering]:**

Welche Ebene von [Ads.txt](https://iabtechlab.com/ads-txt-about/) Filterung vor dem Gebot , die verwendet wird, indem die Liste der autorisierten digitalen Verkäufer jedes Herausgebers genutzt wird. Die Standardeinstellung auf Advertiser-Ebene wird für neue Platzierungen ausgewählt, Sie können jedoch die Einstellungen ändern:

* *[!UICONTROL Opt out of ads.txt (default)]*: Inventar von allen Verkäufern zu kaufen.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: Zur Priorisierung des Kaufinventars von autorisierten Direktverkäufern und Wiederverkäufern einer Domain.
* *[!UICONTROL Ads.txt sellers only]*: Um Inventar nur von autorisierten Direktverkäufern und Wiederverkäufern einer Domain zu kaufen.
* *[!UICONTROL Ads.txt sellers only]*: Um Inventar nur von autorisierten Direktverkäufern einer Domain zu kaufen.

**[!UICONTROL DoubleVerify Authentic Brand Safety]:** (Advertiser, die mit der [!UICONTROL DoubleVerify Authentic Brand Safety] Option) Aktiviert [!DNL DoubleVerify Authentic Brand Safety]: blockiert Impressionen nach dem Angebot mithilfe der benutzerdefinierten Markensicherheitsregeln, die für die angegebene Segment-ID konfiguriert sind. DSP stellt Ihr Konto für die Verwendung der in den Advertiser-Einstellungen angegebenen Segment-ID in Rechnung.

## [!UICONTROL Tracking] {#placement-tracking}

>[!NOTE]
>
>([!DNL Roku] Platzierungen) Drittanbieter für die Nachverfolgung, die von [!DNL Roku] include [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]und [!DNL Research Now].

**[!UICONTROL Event Pixels]:** (Optional) Drittanbieter-Pixel für Ereignisverfolgung, die standardmäßig an alle neuen Anzeigen in der Platzierung angehängt werden. So legen Sie Ereignispixel fest:

1. Klicken ![Bearbeiten](/help/dsp/assets/edit.png).
1. Führen Sie einen der folgenden Schritte aus:
   * Um ein vorhandenes Pixel auszuwählen, aktivieren Sie das Kontrollkästchen in der Pixelzeile.
   * So erstellen Sie ein neues Pixel:
      1. Klicken **[!UICONTROL Create]**.
      1. Geben Sie die folgenden Informationen ein:
         * **[!UICONTROL Pixel name]:** Der Pixelname; die maximale Länge beträgt 500 Zeichen. Verwenden Sie einen Namen, mit dem Sie das Pixel leicht identifizieren können.
         * **[!UICONTROL Pixel event fires on]:** Das Ereignis, bei dem das Pixel Trigger wird, um ausgelöst zu werden. Die verfügbaren Ereignisse variieren je nach Anzeigentyp.
         * **[!UICONTROL Pixel type]:** Gibt an, ob das Pixel ein *[!UICONTROL IMG URL]* (1x1-Pixel-Bilddatei), *[!UICONTROL HTML]* oder *[!UICONTROL JavaScript URL]*.
         * **[!UICONTROL Pixel URL]:** Die URL des Pixelbilds.
      1. Klicken **[!UICONTROL Create and attach]**.
   1. Klicken **[!UICONTROL Save]**.

**[!UICONTROL Conversion Pixels]:** (Optional) Konversions-Tracking-Pixel, die standardmäßig an alle neuen Anzeigen in der Platzierung angehängt werden. So legen Sie Konversionspixel fest:

1. Klicken ![Bearbeiten](/help/dsp/assets/edit.png).
1. Führen Sie einen der folgenden Schritte aus:
   * Um ein vorhandenes Pixel auszuwählen, aktivieren Sie das Kontrollkästchen in der Pixelzeile.
   * So erstellen Sie ein neues Pixel:
      1. Klicken **[!UICONTROL Create]**.
      1. Geben Sie die folgenden Informationen ein:
         * **[!UICONTROL Conversion pixel name]:** Der Pixelname; die maximale Länge beträgt 500 Zeichen. Verwenden Sie einen Namen, mit dem Sie das Pixel leicht identifizieren können.
         * **[!UICONTROL Conversion category]:** Der Konversionstyp.
         * **[!UICONTROL Impression conversion window]:** Die Anzahl der Tage, nach denen eine Ad-Impression auftritt, in denen die Impression einer Konversion zugeordnet werden kann. Der Standardwert ist 30 Tage.
         * **[!UICONTROL Click conversion window]:** Die Anzahl der Tage nach einem Anzeigenklick, in denen der Klick einer Konversion zugeordnet werden kann. Der Standardwert ist 30 Tage.
         * **[!UICONTROL Notes]:** (Optional) Eine Beschreibung oder andere Informationen zum Pixel.
      1. Klicken **[!UICONTROL Create and attach]**.
      1. Implementieren Sie das Konversionspixel auf den relevanten Webseiten:
         1. Navigieren Sie im Hauptmenü zu **[!UICONTROL Resources]>[!UICONTROL Conversion pixels]**.
         1. Klicken Sie in der Pixelzeile auf **[!UICONTROL edit]**.
         1. Kopieren Sie die Werte im [!UICONTROL HTML Tag] und [!UICONTROL Flash Tag] bei Bedarf Felder, die dem Werber oder Website-Kontakt zur Verfügung gestellt werden.

            Möglicherweise muss die IT-Abteilung des Werbetreibenden oder eine andere Gruppe die Tag-Bereitstellung planen oder darüber informiert werden.
   1. Klicken **[!UICONTROL Save]**.

**[!UICONTROL 3rd-party Fees]:** (Optional) Ein statischer Drittanbieter-Gebührensatz, der als nicht abrechnungsfähige Kosten pro 1000 Impressionen verfolgt wird. Die Standardeinstellung auf Paketebene wird bei neuen Platzierungen automatisch angewendet, sofern kein anderer Wert eingegeben wird.

>[!NOTE]
>
>Abrechenbare Gebühren werden im [!UICONTROL Net CPM] Metrik.

>[!MORELIKETHIS]
>
>* [Über die Platzierungsverwaltung](placement-about.md)
>* [Erstellen einer Platzierung](placement-create.md)
>* [Eine Platzierung bearbeiten](placement-edit.md)
>* [Tastaturbefehle](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [Häufig gestellte Fragen zu Campaign Management](/help/dsp/campaign-management/campaign-management-faq.md)

