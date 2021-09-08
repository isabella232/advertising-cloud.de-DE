---
title: Kampagneneinstellungen
description: Siehe Beschreibungen der verfügbaren Kampagnenparameter.
feature: Campaigns
exl-id: ff2e22ff-8073-4532-884b-36e0c1f22641
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '990'
ht-degree: 0%

---

# Kampagneneinstellungen

## [!UICONTROL Basic Campaign Details]

**[!UICONTROL Name]:** Der Kampagnenname.

**[!UICONTROL Advertiser]:**  (Schreibgeschützt für vorhandene Kampagnen) Der entsprechende Advertiser (Marke). Wählen Sie einen bestehenden Advertiser aus oder erstellen Sie einen neuen.

**[!UICONTROL Advertiser URL]:** Die offizielle Seite des Werbetreibenden. Dieses Feld beschleunigt Ihren Prozess zur Anzeigenvalidierung mit Inventarpartnern.

**[!UICONTROL Timezone]:**  (Schreibgeschützt für vorhandene Kampagnen) Die Zeitzone für die Berichterstellung und Gebote.

**[!UICONTROL Customer PO]:**  (Optional) Eine Kundenbestellung für die Einfügebestellung/Bestellung.

**[Kampagnendaten]:**  Das Start- und Enddatum der Kampagne.

## [!UICONTROL Campaign Goals]

**[!UICONTROL Margin Management]:** Ob Ränder für die Kampagne verwaltet werden sollen:  *[!UICONTROL Yes]* oder  *[!UICONTROL No]* (Standard).

Wenn Sie *[!UICONTROL Yes]auswählen, geben Sie* den Randtyp und den Betrag an:

* **[!UICONTROL Margin Type]:** Der Typ des Rands. Sobald Sie die Margenverwaltung aktiviert und die Kampagne gespeichert haben, können Sie den Margentyp nicht mehr ändern.

   * *[!UICONTROL Fixed]:*  (Standardeinstellung) Ermöglicht Advertising Cloud DSP die automatische Berechnung und Begrenzung der Ausgaben basierend auf einem festen Marge-Prozentsatz des  [!UICONTROL Gross Budget].

   * *[!UICONTROL Dynamic]:* Ermöglicht die Verwaltung von Rändern bis zur Platzierungsebene durch Angabe eines separaten  [!UICONTROL Budget Reserve %] und  [!UICONTROL Gross Budget] für jedes Paket und jede Platzierung in der Kampagne. Advertising Cloud DSP optimiert sich auf der Grundlage der finanziellen Effizienz jeder Platzierung, ohne eine bestimmte Marge zu garantieren. Verwenden Sie dies für Einfügeaufträge, die aus mehreren Zeileneinträgen bestehen, für die Sie vereinbart haben, eine feste Menge von Einheiten oder Einheitentypen zu einem festen Preis bereitzustellen.

* **[!UICONTROL Fixed Margin %]:**  (Nur Kampagnen mit festen Rändern) Das standardmäßige Markup für jede Einfügereihenfolge  <!-- impression? -->in Prozent. Dieser Betrag wird vom [!UICONTROL Gross Budget] abgezogen, um das Netto-Kampagnenbudget zu bestimmen.

* **[!UICONTROL Budget Reserve %]:**  (Nur Kampagnen mit festen Rändern; (optional) Erhält einen bestimmten Prozentsatz von  [!UICONTROL Gross Budget] als Schutz. Dieser Betrag wird vom [!UICONTROL Gross Budget] abgezogen, um das Netto-Kampagnenbudget zu bestimmen.

**[!UICONTROL Gross Budget]:**  (Nur Kampagnen mit Margenverwaltung) Das Bruttokampagnenbudget, bevor die festgelegten Grenzanpassungen angewendet werden.

Sie können optional ein zusätzliches Bruttobudget für Tag, Woche oder Monat hinzufügen:

1. Klicken **[!UICONTROL Add an additional Gross Budget]**.

1. Geben Sie den Wert **[!UICONTROL Gross Budget]** ein und wählen Sie das Budgetintervall aus: *[!UICONTROL Daily],* *[!UICONTROL Weekly],* oder *[!UICONTROL Monthly]*.

Das Nettogesamtbudget, das die Ausgabenobergrenze für die Kampagne darstellt, wird automatisch anhand der Margeneinstellungen berechnet und unter diesem Wert angegeben.

**[!UICONTROL Budget]:**  (Kampagnen ohne Margenverwaltung) Das Gesamtbudget der Kampagne.

**[!UICONTROL Estimated Tax Withholding]:** Hält einen Prozentsatz der Gesamtausgaben für Anzeigengebühren, Ad-Serving-Gebühren und/oder Datengebühren auf Kontoebene für landesweite oder lokale Steuern ein. Bei den Sätzen handelt es sich um Schätzungen für Budgetierungs- und Schrittzwecke, sodass die fakturierten Steuersätze variieren können.

So schätzen Sie die einzubehaltenden Steuern:

1. Klicken **[!UICONTROL Update rates here]**.

1. Geben Sie **[!UICONTROL Estimated tax rate]** als Prozentsatz an.

1. Aktivieren Sie das Kontrollkästchen neben jedem Gebührentyp, für den Steuern einbehalten werden sollen. Zu den Gebührentypen gehören:

   * *[!UICONTROL Include estimated tax - ads fee]:* Gilt für alle Advertising Cloud DSP-Medienausgaben, einschließlich Steuern auf Kampagnenverwaltungsgebühren.

   * *[!UICONTROL Include estimated tax - ad serving fee]:* Gilt für alle Ausgaben in Advertising Cloud DSP mit Ausnahme von Medien und Daten. Ausgeschlossen sind Steuern für Kampagnenverwaltungsgebühren

   * *[!UICONTROL Include estimated tax - data fee]:* Gilt für alle Datenausgaben in Advertising Cloud DSP.

1. Klicken **[!UICONTROL Submit]**.

>[!NOTE]
>
>* In den USA können die Bundesstaaten bei der Einbeziehung von Steuergebühren für Anzeigen, Adserving und Daten variieren. Für Organisationen in anderen Ländern sind alle drei Kategorien von Steuergebühren zur Berücksichtigung der Mehrwertsteuer einzubeziehen.
>
>* Sie können diese Werte auch in den Gebühreneinstellungen des Kontos konfigurieren.<!--[fee settings](/help/dsp/admin/tax-withholdings.md). -->


**[!UICONTROL Cross Device Level]:** (Schreibgeschützt für bestehende Kampagnen, die seit dem 22. Juni 2020 erstellt wurden; nicht verfügbar für Kampagnen, die vor dem 22. Juni 2020 erstellt wurden. Die Ebene, auf der Advertising Cloud Anzeigen ansprechen und Frequenzobergrenzen anwenden wird:  *Dasselbe* Gerät zum Targeting eines Geräts oder einer  ** Person für alle bekannten Geräte.

**[!UICONTROL Device Graph]:**  (Schreibgeschützt für bestehende Kampagnen; Kampagnen mit benutzerspezifischem geräteübergreifendem Targeting) Das Gerätediagramm, das für geräteübergreifendes Targeting und Frequenzmanagement verwendet werden soll:

* *[!UICONTROL LiveRamp - U.S. only]:* Verfügbar für alle Advertiser für geräteübergreifendes Targeting mit einer CPM-Rate von 0,35 USD für Impressionen, die mithilfe des  [!DNL LiveRamp] Gerätediagramms bereitgestellt werden (d. h. für Geräte, die nicht in den Zielgruppensegmenten gefunden werden). Sie können geräteübergreifendes Targeting auf Platzierungsebene einrichten.

   Diese Option steht auch allen Advertisern ohne Gebühren für Frequenzverwaltung und Attributionsmessung zur Verfügung.

* *[!UICONTROL Adobe Co-op U.S. and Canada only]:* Nur für Adobe Experience Cloud- [!DNL Device Co-op] Teilnehmer verfügbar ohne Aufpreis.

>[!TIP]
>
>Wenn der Werbetreibende auch geräteübergreifende Attribution verwendet, empfiehlt es sich, dieselben Gerätediagrammeinstellungen für Targeting und Frequenzverwaltung zu verwenden, die auch in den geräteübergreifenden Attributionseinstellungen des Werbetreibenden angegeben sind. Wenn Sie ein anderes Gerätediagramm für diese Kampagne auswählen, kann es zu Berichtsdiskrepanzen kommen.

**[!UICONTROL Frequency Cap]:** (Optional) Die Häufigkeit, mit der ein eindeutiges Gerät oder eine eindeutige Person (je nach  [!UICONTROL Cross Device Level]spezifiziertem Element) von einer Kampagne bedient wird. Zu den Optionen gehören *[!UICONTROL Unlimited]* oder ein bestimmter Betrag pro Tag, Woche oder Monat.

>[!NOTE]
>
> Sie können Frequenzobergrenzen auf Kampagnen-, Paket- und Platzierungsebene festlegen. DSP respektiert die strengste Frequenzgrenze in der Kampagnenhierarchie.

**[!UICONTROL Packages]:** Die  [](/help/dsp/campaign-management/packages/package-about.md) Pakete, die in die Kampagne aufgenommen werden sollen. Wählen Sie vorhandene Pakete aus und/oder erstellen Sie Pakete, die einbezogen werden sollen. Wenn Sie Pakete erstellen, finden Sie weitere Informationen unter Beschreibungen der [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md).

## [!UICONTROL Campaign Measurement]

>[!NOTE]
>
>Die folgenden Einstellungen ermöglichen nur Mess- und Berichterstellungsfunktionen. Die Leistungsoptimierung wird nur auf Paket- und Platzierungsebene ausgeführt.

### [!UICONTROL 3rd Party Metrics]

#### [!UICONTROL Viewability, Fraud, & Brand Safety]

**[!UICONTROL IAS]:**  (Optional) Ermöglicht die  [!DNL IAS] Messung und Berichterstellung von Sichtbarkeit, Betrug, Markensicherheit und Zielgruppenüberprüfung mithilfe der angegebenen Einstellungen. Es fallen zusätzliche Gebühren an.

* **[!UICONTROL Measure On]:** Das Verzeichnis, in dem Folgendes gemessen werden soll:  *[!UICONTROL Display and VPAID video inventory]* (Standard) oder  *[!UICONTROL Display, VPAID & VAST video inventory]*.

   >[!NOTE]
   >
   >Die Sichtbarkeit von Videos ist nur im VPAID-Inventar messbar.

* **[!UICONTROL IAS Account ID (AnID)]:**  (Werbetreibende mit eigenen  [!DNL IAS] Konten; (optional) Die  [!DNL IAS] Konto-ID des Unternehmens, die direkt zur Verwendung aufgerechnet  [!DNL IAS] wird.

* **[!UICONTROL IAS Team ID]:**  (Werbetreibende mit eigenen  [!DNL IAS] Konten; optional) Die Team-ID für das  [!DNL IAS] Konto des Unternehmens, die direkt zur Verwendung aufgerechnet  [!DNL IAS] wird.  <!-- verify -->

**[!UICONTROL MOAT]:**  (Optional) Ermöglicht die  [!DNL MOAT] Messung und Berichterstellung von Sichtbarkeit, Betrug, Markensicherheit und Zielgruppenüberprüfung. Es fallen zusätzliche Gebühren an.

#### Zielgruppenüberprüfung

**[!UICONTROL Nielsen]:**  (Optional) Ermöglicht die  [!DNL Nielsen] Messung und Berichterstellung der Zielgruppenüberprüfung mithilfe der angegebenen Einstellungen. Es fallen zusätzliche Gebühren an.

* **[!UICONTROL Target Gender]:** Das Geschlecht, das als Ziel ausgewählt werden soll:  *[!UICONTROL Both]* (Standardeinstellung)  *[!UICONTROL Male]* oder  *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** Die Altersgruppe, die als Ziel ausgewählt werden soll. Verwenden Sie die linken und rechten Schieberegler, um den Bereich nach Bedarf zu reduzieren.

* **[!UICONTROL Target Country]:**  (Optional) Ein Land, das als Ziel ausgewählt werden soll. [!DNL Nielsen] misst nur Impressionen, die in unterstützten Ländern bereitgestellt werden.

**[!UICONTROL comScore vCE]:**  (Optional) Ermöglicht die  [!DNL Comscore validated Campaign Essentials (vCE)] Messung und Berichterstellung der Zielgruppenüberprüfung mithilfe der angegebenen Einstellungen. Es fallen zusätzliche Gebühren an.

* **[!UICONTROL Target Gender]:** Das Geschlecht, das als Ziel ausgewählt werden soll:  *[!UICONTROL Both]* (Standardeinstellung)  *[!UICONTROL Male]* oder  *[!UICONTROL Female]*

* **[!UICONTROL Target Age]:** Die Altersgruppe, die als Ziel ausgewählt werden soll. Verwenden Sie die linken und rechten Schieberegler, um den Bereich nach Bedarf zu reduzieren.

* **[!UICONTROL Target Country]:**  (Optional) Ein Land, das als Ziel ausgewählt werden soll. [!DNL Comscore] misst nur Impressionen, die in unterstützten Ländern bereitgestellt werden.

### [!UICONTROL 1st Party Metrics]

**[!UICONTROL Viewability sensitivity]:** Ermöglicht die Messung und Berichterstellung der Sichtbarkeit von Erstanbietern mithilfe der  [!DNL IAB Open Video Viewability (OpenVV)] Technologie, basierend auf der angegebenen Empfindlichkeitsstufe:

* *[!UICONTROL Standard (50% of ad in view for two consecutive seconds)]*

* *[!UICONTROL Strict (100% of ad in view and audio on for 50% duration)]*

>[!MORELIKETHIS]
>
>* [Über Campaign Management](campaign-about.md)
>* [Erstellen einer Kampagne](campaign-create.md)
>* [Eine Kampagne bearbeiten](campaign-edit.md)

