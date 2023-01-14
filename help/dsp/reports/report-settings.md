---
title: Benutzerdefinierte Berichtseinstellungen
description: Siehe Beschreibungen der benutzerdefinierten Berichtseinstellungen.
feature: DSP Custom Reports
exl-id: 1d37fc96-0f9b-4eb2-ba8d-9534f627adaf
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '966'
ht-degree: 0%

---

# Benutzerdefinierte Berichtseinstellungen

**[!UICONTROL Name]** Der Berichtsname. Die maximale Länge beträgt 180 Zeichen.

**[!UICONTROL Report Type]** Berichtstyp: *[!UICONTROL Custom]* (die die meisten verfügbaren Optionen enthält), *[!UICONTROL Billing]*, *[!UICONTROL Conversion]*, *[!UICONTROL Device]*, *[!UICONTROL Frequency (by Impression)]*,  *[!UICONTROL Frequency (by App/Site)]*, *[!UICONTROL Geo]*, *[!UICONTROL Margin]*, *[!UICONTROL Media Performance]*,  *[!UICONTROL Segment]* oder *[!UICONTROL Site]*.

## [!UICONTROL Apply Filters] Abschnitt

**[!UICONTROL Timezone]:** Die Zeitzone für die Berichterstellung.

**[!UICONTROL Observe Daylight Savings Time]:** Betrachtet die Sommerzeit in den gemeldeten Zeiten.

**\[Datumsbereich\]:** Der Datumsbereich, für den Daten generiert werden sollen. Die Anzahl der Tage variiert je nach Bericht und ausgewählten Dimensionen. Wählen Sie eine aus:

* **[!UICONTROL Previous N days]:** Umfasst Daten für eine bestimmte Anzahl von Tagen vor heute.

* **[!UICONTROL Custom]:** Umfasst Daten zwischen bestimmten Start- und Enddaten. Um Daten über den Vortag zu berichten, wählen Sie **[!UICONTROL Present]**.

* **[!UICONTROL Last Calendar Month]:** Umfasst Daten für den vorherigen Kalendermonat.

**[!UICONTROL Add Filters]:** (Optional) Zusätzliche Dimensionen zum Filtern der Daten, unabhängig davon, ob die Dimensionen als Spalten im Bericht enthalten sind: *[!UICONTROL Account]*,\* *[!UICONTROL Advertiser]*, *[!UICONTROL Campaign]*, *[!UICONTROL Placement]*, *[!UICONTROL Ad]*, *[!UICONTROL Ad Type]*, *[!UICONTROL Video]*, *[!UICONTROL Video Duration]*, *[!UICONTROL Country]* und *[!UICONTROL Package]*.

\* *[!UICONTROL Account]* ist nur für die folgenden Berichtstypen verfügbar, wenn Ihr Unternehmen für [kontoübergreifende Berichterstattung](report-about.md#cross-account-reporting):  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)]und [!UICONTROL Conversion]. Wenden Sie sich an [!DNL Adobe] Account-Team finden Sie weitere Informationen zur kontoübergreifenden Berichterstellung.

Gehen Sie wie folgt vor, um einen oder mehrere Filter anzuwenden:

* Wählen Sie eine Dimension aus und wählen Sie den Operator (*gleich* oder *nicht gleich*) und wählen Sie dann den entsprechenden Wert aus. Wenn Sie beispielsweise nur Daten für Pre-Pup-Anzeigen zurückgeben möchten, geben Sie &quot;[!UICONTROL Ad Type equals Preroll].&quot;
* (Optional) Fügen Sie dem Filter zusätzliche Kriterien hinzu.
* (Optional) Fügen Sie zusätzliche Filter hinzu, von denen jeder ein oder mehrere Kriterien aufweist.

## [!UICONTROL Build Your Report] Abschnitt

**[!UICONTROL Select To Add As Report Headers]:**  Die Datenspalten oder Kopfzeilen, die in den Bericht aufgenommen werden sollen. Um eine Spalte hinzuzufügen, erweitern Sie die Kategorie und aktivieren Sie das Kontrollkästchen neben dem Spaltennamen. Alle nicht verfügbaren Metriken sind deaktiviert. Zu den verfügbaren Datenkategorien gehören:

* [!UICONTROL  Dimensions]
* [!UICONTROL Metrics]
* [!UICONTROL Conversion Metrics] (sortiert nach Advertiser)
* [!UICONTROL Custom Goals] (sortiert nach Advertiser)

**[!UICONTROL Drag to Re-Order Report Headers Below]:** Die Reihenfolge der Spaltenüberschriften. Sie können jede Spalte per Drag-and-Drop verschieben, um die Reihenfolge anzupassen.

## [!UICONTROL Multi-Touch Conversion Options] Abschnitt

**[!UICONTROL Format]:** Gibt an, ob ein Bericht in *[!UICONTROL CSV]* (kommagetrennte Werte) oder *[!UICONTROL Tab]* (tabulatorgetrennte Werte).

**[!UICONTROL Report Headers]:** Ob *[!UICONTROL Include]* oder *[!UICONTROL Do Not Include]* Spaltenüberschriften.

**[!UICONTROL Attribution Rule Settings]:** (Alle [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment]und [!UICONTROL Site] Berichte mit [!UICONTROL Conversion Metrics] oder [!UICONTROL Custom Goals] Spalten; Advertiser mit Adobe Advertising-Konversions-Tracking) Wie werden im Bericht Konversionsdaten in einer Reihe von Ereignissen zugeordnet, die zu einer Konversion führen? Sie können mehrere Regeln auswählen, wenn Sie Unterschiede zwischen den Regeln vergleichen möchten.

>[!NOTE]
>
>Konversionspfade umfassen alle Impressionen und Klicks innerhalb der Impressions- oder Klick-Lookback-Fenster des Advertisers, die in [!DNL Adobe Advertising Search]. Klicks erhalten während der Konversionszuordnung Vorrang vor Impressionen. Alle Klicks in einem Konversionspfad erhalten die volle Gutschrift auf Grundlage der Attributionsregel. Impressionen erhalten nur dann eine Gutschrift, wenn im Konversionspfad keine Klicks verfolgt werden.

* *[!UICONTROL Last Event]:* Ordnet Konversionen dem letzten Klick oder der letzten Impression im Konversionspfad zu.

* *[!UICONTROL Weight Last More]:* Ordnet allen Ereignissen im Konversionspfad Konversionen zu, gibt jedoch dem letzten Ereignis die höchste Gewichtung und den vorherigen Ereignissen eine schrittweise geringere Gewichtung zu.

* *[!UICONTROL Even Distribution]:* Weist Konversionen gleichmäßig jedem Ereignis im Konversionspfad zu.

* *[!UICONTROL Weight First More]:* Ordnet allen Ereignissen im Konversionspfad Konversionen zu, gibt jedoch dem ersten Ereignis die höchste Gewichtung und den folgenden Ereignissen eine schrittweise geringere Gewichtung zu.

* *[!UICONTROL First Event]:* Ordnet Konversionen dem ersten Klick oder der ersten Impression im Konversionspfad zu.

* *[!UICONTROL U-shaped]:* Ordnet die Konversion allen Ereignissen im Konversionspfad zu, gibt jedoch dem ersten und letzten Ereignis die höchste Gewichtung, bei einer nacheinander geringeren Gewichtung der Ereignisse in der Mitte des Konversionspfads.

* *[!UICONTROL Display Only]:*  Ordnet Konversionen dem letzten DSP Klick oder Impression im Konversionspfad zu. Dazu gehören Video- und vernetzte TV-Anzeigen sowie Klicks auf [!DNL Adobe Advertising Search] Anzeigen.

* *[!UICONTROL Social Only]:* Obsolete

<!-- See also [How Attribution Rules Are Calculated for Adobe Advertising](). -->

**[!UICONTROL Paths as Columns]:**  (Alle [!UICONTROL Custom], [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo], [!UICONTROL Segment]und [!UICONTROL Site] Berichte mit [!UICONTROL Conversion Metrics] oder [!UICONTROL Custom Goals] -Spalten) Welche Konversionstypen werden in Berichten aufgeführt, wenn auf demselben Gerät frühere Ereignisse aufgetreten sind. Sie können bis zu drei Typen einbeziehen. Für jeden ausgewählten Typ wird für jede Konversionsmetrik eine separate Spalte eingefügt und dem angegebenen Suffix ([!UICONTROL (tl)], [!UICONTROL (ct)]oder [!UICONTROL (vt)]):

* *[!UICONTROL Total (TL) = CT + VT \* VT weight]:* Umrechnungen, die Klicks (CT für Clickthrough) und Impressionen (VT für Durchsicht) zugeordnet werden. Auf Impressionen zugeordnete Konversionen werden mit der angegebenen Durchsichtsgewichtung multipliziert. Die standardmäßige Durchsichtsgewichtung beträgt 100 %, d. h. Konversionen, die Impressionen zugeordnet werden, werden als 100 % des Werts der Konversionen gezählt, die den Klicks zugeordnet sind.

* *[!UICONTROL With Clicks (CT)]:* Umfasst nur Konversionen, die Klicks zugeordnet sind.

* *[!UICONTROL Impressions Only (VT)]:* Umfasst nur Konversionen, die Impressionen zugeordnet wurden, da im Konversionspfad keine Klicks verfolgt wurden.

**[!UICONTROL Conversion Reporting Based On]:**  So melden Sie Konversionsdaten:

* *[!UICONTROL Conversion Timestamp]:* (Standard) Konversionen werden mit dem Konvertierungsdatum verknüpft.

* *[!UICONTROL Event Timestamp]:* Konversionen werden basierend auf dem Datum der Impression oder des Klicks gemeldet, der die Konversion verursacht hat, wie durch die angegebene [!UICONTROL Attribution Rule Settings].

## [!UICONTROL Add Report Destinations] Abschnitt

**[!UICONTROL Destination Type]:** Wählen Sie einen der folgenden Zieltypen aus:

* *[!UICONTROL S3]:* So senden Sie den abgeschlossenen Bericht an eine oder mehrere [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]) -Speicherorte, die Sie im **[!UICONTROL Destination Name]** -Feld.
* *[!UICONTROL sFTP]:* So senden Sie den abgeschlossenen Bericht an einen oder mehrere SFTP-Standorte, die Sie im Abschnitt **[!UICONTROL Destination Name]** -Feld.
* *[!UICONTROL FTP]:* So senden Sie den abgeschlossenen Bericht an einen oder mehrere FTP-Speicherorte, die Sie im Abschnitt **[!UICONTROL Destination Name]** -Feld.
* *[!UICONTROL FTP SSL](Aktuell in Beta):* So senden Sie den abgeschlossenen Bericht an einen oder mehrere FTP-SSL-Speicherorte, die Sie im Abschnitt **[!UICONTROL Destination Name]** -Feld.
* *[!UICONTROL Email]:* Angabe der E-Mail-Adresse(n), an die abgeschlossene Berichte oder Benachrichtigungen gesendet werden sollen, wenn der Bericht aufgrund von Fehlern abgebrochen wird. Um mehrere Adressen anzugeben, trennen Sie sie durch Kommas oder Leerzeichen.

>[!NOTE]
>
> Sie können den Zieltyp nach dem Speichern des Berichts nicht mehr ändern.

**[!UICONTROL Destination Name]:** (Nur S3-, FTP-, sFTP- und FTP-SSL-Zieltypen) Die Namen der Berichtsziele, an die der benutzerdefinierte Bericht gesendet wird.

* Um ein vorhandenes Ziel anzugeben, wählen Sie einen Zielnamen aus der Liste aus. Sie können mehrere Zielnamen separat auswählen.

* So erstellen Sie ein neues Ziel:

   1. Klicken **Neues Ziel hinzufügen**.

   1. Geben Sie die [Berichtszieleinstellungen](/help/dsp/reports/report-destinations/report-destination-settings.md)und klicken Sie auf **Speichern**.

   1. Klicken Sie in den Berichtseinstellungen auf **Aktualisieren Sie die Zielnamen.**

      Das neue Ziel ist jetzt in der Liste der vorhandenen Ziele verfügbar und Sie können es optional zum Bericht hinzufügen.

**[!UICONTROL Frequency]:** (Für jeden [!UICONTROL Destination Name] Wie oft wird der Bericht an das Ziel gesendet: *[!UICONTROL Once]*, *[!UICONTROL Daily]*, *[!UICONTROL Weekly]* oder *[!UICONTROL Monthly]*.

## [!UICONTROL Save Report] Abschnitt

**[!UICONTROL Send & Save]:** Zeitpunkt des Berichtversands: *[!UICONTROL On Schedule]* oder *[!UICONTROL Run Now]*. Geplante Berichte werden um 9:00 Uhr in der Zeitzone des Kontos bereitgestellt.

>[!NOTE]
>
>Sie können [jederzeit einen benutzerspezifischen Bericht ausführen](report-run-now.md) von [!UICONTROL Reports] anzeigen.

>[!MORELIKETHIS]
>
>* [Über benutzerdefinierte Berichte](/help/dsp/reports/report-about.md)
>* [Benutzerspezifischen Bericht erstellen](/help/dsp/reports/report-create.md)
>* [Benutzerspezifischen Bericht duplizieren](/help/dsp/reports/report-copy.md)
>* [Benutzerspezifischen Bericht bearbeiten](/help/dsp/reports/report-edit.md)
>* [Benutzerspezifischen Bericht ausführen](/help/dsp/reports/report-run-now.md)
>* [Benutzerdefinierte Berichtseinstellungen](/help/dsp/reports/report-settings.md)
>* [Über Berichtsziele](/help/dsp/reports/report-destinations/report-destination-about.md)

* [Verfügbare Berichtsspalten](/help/dsp/reports/report-columns.md)
