---
title: Benutzerdefinierte Berichtseinstellungen
description: Siehe Beschreibungen der benutzerdefinierten Berichtseinstellungen.
feature: Custom Reports
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---


# Benutzerdefinierte Berichtseinstellungen

**[!UICONTROL Name]** Der Berichtsname. Die maximale Länge beträgt 180 Zeichen.

**[!UICONTROL Report Type]** Berichtstyp:  *[!UICONTROL Custom]* (die die meisten verfügbaren Optionen enthält),  *[!UICONTROL Billing]*,  *[!UICONTROL Conversion]*,  *[!UICONTROL Device]*,  *[!UICONTROL Frequency (by Impression)]*,   *[!UICONTROL Frequency (by App/Site)]*,  *[!UICONTROL Geo]*,  *[!UICONTROL Margin]*,  *[!UICONTROL Media Performance]*,   *[!UICONTROL Segment]* oder  *[!UICONTROL Site]*.

## [!UICONTROL Apply Filters] Abschnitt

**[!UICONTROL Timezone]:** Die Zeitzone für die Berichterstellung.

**[!UICONTROL Observe Daylight Savings Time]:** Betrachtet die Sommerzeit in den gemeldeten Zeiten.

**\[Datumsbereich\]:** Der Datumsbereich, für den Daten generiert werden sollen. Die Anzahl der Tage variiert je nach Bericht und ausgewählten Dimensionen. Wählen Sie eine aus:

* **[!UICONTROL Previous N days]:** Umfasst Daten für eine bestimmte Anzahl von Tagen vor heute.

* **[!UICONTROL Custom]:** Umfasst Daten zwischen bestimmten Start- und Enddaten. Um Daten über den Vortag zu melden, wählen Sie **[!UICONTROL Present]** aus.

* **[!UICONTROL Last Calendar Month]:** Umfasst Daten zum vorherigen Kalendermonat.

**[!UICONTROL Add Filters]:** (Optional) Zusätzliche Dimensionen zum Filtern der Daten, unabhängig davon, ob die Dimensionen als Spalten im Bericht enthalten sind:  *[!UICONTROL Account]*,\*  *[!UICONTROL Advertiser]*,  *[!UICONTROL Campaign]*,  *[!UICONTROL Placement]*,  *[!UICONTROL Ad]*,  *[!UICONTROL Ad Type]*,  *[!UICONTROL Video]*,  *[!UICONTROL Video Duration]*,  *[!UICONTROL Country]* und  *[!UICONTROL Package]*.

\* *[!UICONTROL Account]* ist nur dann für die folgenden Berichtstypen verfügbar, wenn Ihr Unternehmen für [kontoübergreifende Berichte](report-about.md#cross-account-reporting) konfiguriert ist:  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)] und [!UICONTROL Conversion]. Wenden Sie sich an Ihren Kundenbetreuer, um weitere Informationen zur kontoübergreifenden Berichterstellung zu erhalten.

Gehen Sie wie folgt vor, um einen oder mehrere Filter anzuwenden:

* Wählen Sie eine Dimension aus, wählen Sie den Operator (*equals* oder *not equals*) und wählen Sie dann den entsprechenden Wert aus. Wenn Sie beispielsweise nur Daten für Pre-oll-Anzeigen zurückgeben möchten, geben Sie &quot;[!UICONTROL Ad Type equals Preroll]&quot;an.
* (Optional) Fügen Sie dem Filter zusätzliche Kriterien hinzu.
* (Optional) Fügen Sie zusätzliche Filter hinzu, von denen jeder ein oder mehrere Kriterien aufweist.

## [!UICONTROL Build Your Report] Abschnitt

**[!UICONTROL Select To Add As Report Headers]**  : Die Datenspalten oder Kopfzeilen, die in den Bericht aufgenommen werden sollen. Um eine Spalte hinzuzufügen, erweitern Sie die Kategorie und aktivieren Sie das Kontrollkästchen neben dem Spaltennamen. Alle nicht verfügbaren Metriken sind deaktiviert. Zu den verfügbaren Datenkategorien gehören:

* [!UICONTROL  Dimensions]
* [!UICONTROL Metrics]
* [!UICONTROL Conversion Metrics] (sortiert nach Advertiser)
* [!UICONTROL Custom Goals] (sortiert nach Advertiser)

**[!UICONTROL Drag to Re-Order Report Headers Below]:** Die Reihenfolge der Spaltenüberschriften. Sie können jede Spalte per Drag-and-Drop verschieben, um die Reihenfolge anzupassen.

## [!UICONTROL Multi-Touch Conversion Options] Abschnitt

**[!UICONTROL Format]:** Gibt an, ob ein Bericht im Format  *[!UICONTROL CSV]* (kommagetrennte Werte) oder  *[!UICONTROL Tab]* (tabulatorgetrennte Werte) erstellt werden soll.

**[!UICONTROL Report Headers]:** Gibt an, ob  *[!UICONTROL Include]* oder  *[!UICONTROL Do Not Include]* Spaltenüberschriften verwendet werden sollen.

**[!UICONTROL Attribution Rule Settings]:** (Alle  [!UICONTROL Custom],  [!UICONTROL Conversion],  [!UICONTROL Device],  [!UICONTROL Geo],  [!UICONTROL Segment]und  [!UICONTROL Site] Berichte mit  [!UICONTROL Conversion Metrics] oder  [!UICONTROL Custom Goals] Spalten; wie Sie Konversionsdaten in einer Reihe von Ereignissen zuordnen, die zu einer Konversion führen (nur bei Advertisern mit Advertising Cloud-Konversions-Tracking). Sie können mehrere Regeln auswählen, wenn Sie Unterschiede zwischen den Regeln vergleichen möchten.

>[!NOTE]
>
>Konversionspfade umfassen alle Impressionen und Klicks innerhalb der Impressions- oder Klick-Lookback-Fenster des Advertisers, die in Advertising Cloud Search konfiguriert sind. Klicks erhalten während der Konversionszuordnung Vorrang vor Impressionen. Alle Klicks in einem Konversionspfad erhalten die volle Gutschrift auf Grundlage der Attributionsregel. Impressionen erhalten nur dann eine Gutschrift, wenn im Konversionspfad keine Klicks verfolgt werden.

* *[!UICONTROL Last Event]:* Ordnet Konversionen dem letzten Klick oder der letzten Impression im Konversionspfad zu.

* *[!UICONTROL Weight Last More]:* Ordnet allen Ereignissen im Konversionspfad Konversionen zu, gibt jedoch dem letzten Ereignis die höchste Gewichtung und den vorherigen Ereignissen eine schrittweise geringere Gewichtung zu.

* *[!UICONTROL Even Distribution]:* Ordnet Konversionen jedem Ereignis im Konversionspfad gleich.

* *[!UICONTROL Weight First More]:* Ordnet allen Ereignissen im Konversionspfad Konversionen zu, gibt jedoch dem ersten Ereignis die höchste Gewichtung und den folgenden Ereignissen eine schrittweise geringere Gewichtung zu.

* *[!UICONTROL First Event]:* Ordnet Konversionen dem ersten Klick oder der ersten Impression im Konversionspfad zu.

* *[!UICONTROL U-shaped]:* Ordnet die Konversion allen Ereignissen im Konversionspfad zu, gibt jedoch dem ersten und letzten Ereignis die meiste Gewichtung zu, wobei die Ereignisse in der Mitte des Konversionspfads nach und nach weniger berücksichtigt werden.

* *[!UICONTROL Display Only]:*  Ordnet Konversionen dem letzten Klick oder der letzten DSP im Konversionspfad zu. Dazu gehören Video- und vernetzte Fernsehanzeigen sowie Klicks auf Advertising Cloud Search-Anzeigen.

* *[!UICONTROL Social Only]:* Obsolete

<!-- See also [How Attribution Rules Are Calculated for Adobe Advertising Cloud](). -->

**[!UICONTROL Paths as Columns]:**   (Alle  [!UICONTROL Custom],  [!UICONTROL Conversion],  [!UICONTROL Device],  [!UICONTROL Geo],  [!UICONTROL Segment] und  [!UICONTROL Site] Berichte mit  [!UICONTROL Conversion Metrics] oder  [!UICONTROL Custom Goals] Spalten) Welche Konversionstypen werden gemeldet, wenn auf demselben Gerät frühere Ereignisse aufgetreten sind. Sie können bis zu drei Typen einbeziehen. Für jeden ausgewählten Typ wird eine separate Spalte für jede Konversionsmetrik eingefügt und mit dem angegebenen Suffix ([!UICONTROL (tl)], [!UICONTROL (ct)] oder [!UICONTROL (vt)]) angehängt:

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* Umrechnungen, die Klicks (CT für Clickthrough) und Impressionen (VT für Durchsicht) zugeordnet werden. Auf Impressionen zugeordnete Konversionen werden mit der angegebenen Durchsichtsgewichtung multipliziert. Die standardmäßige Durchsichtsgewichtung beträgt 100 %, d. h. Konversionen, die Impressionen zugeordnet werden, werden als 100 % des Werts der Konversionen gezählt, die den Klicks zugeordnet sind.

* *[!UICONTROL With Clicks (CT)]:* Umfasst nur Konversionen, die Klicks zugeordnet sind.

* *[!UICONTROL Impressions Only (VT)]:* Umfasst nur Konversionen, die Impressionen zugeordnet wurden, da im Konversionspfad keine Klicks verfolgt wurden.

**[!UICONTROL Cross Device Level]:**  (Alle  [!UICONTROL Custom],  [!UICONTROL Conversion],  [!UICONTROL Device],  [!UICONTROL Geo],  [!UICONTROL Segment]und  [!UICONTROL Site] Berichte mit  [!UICONTROL Conversion Metrics] oder  [!UICONTROL Custom Goals] Spalten; nur für Advertiser mit geräteübergreifender Attribution anwendbar) Die Ebene, auf der Konversionen verfolgt werden sollen:  *[!UICONTROL People]* oder  *[!UICONTROL Household]*.

Erfahren Sie mehr über [geräteübergreifende Lösungen](/help/dsp/introduction/features/cross-device-solutions.md).

**[!UICONTROL Cross-Device Breakout]:** (Alle  [!UICONTROL Custom],  [!UICONTROL Conversion],  [!UICONTROL Device],  [!UICONTROL Geo],  [!UICONTROL Segment]und  [!UICONTROL Site] Berichte mit  [!UICONTROL Conversion Metrics] oder  [!UICONTROL Custom Goals] Spalten; nur für Advertiser mit geräteübergreifender Attribution anwendbar) Der Detaillierungsgrad der geräteübergreifenden Konversionen, die in den Bericht aufgenommen werden sollen. Wenn Sie eine detaillierte Aufschlüsselung wünschen, können Sie bis zu drei Ebenen wählen, von denen jede in eine eigene Spalte aufgenommen wird.

* *[!UICONTROL Total People (TP)]:* Umfasst die Gesamtkonversionen, die sowohl Konversionen mit demselben Gerät als auch geräteübergreifende Konversionen enthalten (falls zutreffend). Im Bericht wird &quot;[!UICONTROL (tp)]&quot;an den Namen und Regeltyp der Konversionsmetrik angehängt.

* *[!UICONTROL Same Device (SD)]:* Umfasst nur Konversionen, für die im Konversionspfad nur ein einzelnes Gerät verfolgt wurde. Im Bericht wird &quot;[!UICONTROL (sd)]&quot;an den Namen und Regeltyp der Konversionsmetrik angehängt.

* *[!UICONTROL Cross Device (XD)]:* Umfasst nur Konversionen, für die im Konversionspfad mehr als ein Gerät verfolgt wurde. Im Bericht wird &quot;[!UICONTROL (xd)]&quot;an den Namen und Regeltyp der Konversionsmetrik angehängt.

**[!UICONTROL Conversion Reporting Based On]:**  So melden Sie Konversionsdaten:

* *[!UICONTROL Conversion Timestamp]:*  (Die Standardeinstellung) Konversionen werden mit dem Konvertierungsdatum verknüpft.

* *[!UICONTROL Event Timestamp]:* Konversionen werden basierend auf dem Datum der Impression oder des Klicks gemeldet, die die Konversion verursacht haben, wie durch das angegebene  [!UICONTROL Attribution Rule Settings]festgelegt.

## [!UICONTROL Add Email Recipients] Abschnitt

**[!UICONTROL Email]:** E-Mail-Adresse(n), an die abgeschlossene Berichte oder Benachrichtigungen gesendet werden sollen, wenn der Bericht aufgrund von Fehlern abgebrochen wird. Um mehrere Adressen anzugeben, trennen Sie sie durch Kommas oder Leerzeichen.

**[!UICONTROL Frequency]:** Wie oft wird der Bericht gesendet:  *[!UICONTROL Once]*,  *[!UICONTROL Daily]*,  *[!UICONTROL Weekly]* oder  *[!UICONTROL Monthly]*.

## [!UICONTROL Save Report] Abschnitt

**[!UICONTROL Send & Save]:** Wann der Bericht gesendet werden soll:  *[!UICONTROL On Schedule]* oder  *[!UICONTROL Run Now]*. Geplante Berichte werden um 9:00 Uhr in der Zeitzone des Kontos bereitgestellt.

>[!NOTE]
>
>Sie können [jederzeit einen benutzerspezifischen Bericht](report-run-now.md) aus der [!UICONTROL Reports] -Ansicht ausführen.

>[!MORELIKETHIS]
>
>* [Über benutzerdefinierte Berichte](/help/dsp/reports/report-about.md)
>* [Benutzerspezifischen Bericht erstellen](/help/dsp/reports/report-create.md)
>* [Benutzerspezifischen Bericht duplizieren](/help/dsp/reports/report-copy.md)
>* [Benutzerspezifischen Bericht bearbeiten](/help/dsp/reports/report-edit.md)
>* [Benutzerspezifischen Bericht ausführen](/help/dsp/reports/report-run-now.md)
>* [Benutzerdefinierte Berichtseinstellungen](/help/dsp/reports/report-settings.md)

* [Verfügbare Berichtsspalten](/help/dsp/reports/report-columns.md)
