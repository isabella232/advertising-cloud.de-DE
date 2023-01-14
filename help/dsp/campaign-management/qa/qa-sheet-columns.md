---
title: Spalten in heruntergeladenen/hochgeladenen Arbeitsblättern
description: Referenzieren Sie die Spalten in heruntergeladenen und hochgeladenen Excel QA-Tabellen.
feature: DSP Placements
exl-id: 8a8dceed-f77d-4b6b-a842-f57528125c92
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '782'
ht-degree: 0%

---

# Spalten in heruntergeladenen/hochgeladenen Arbeitsblättern

<!-- rename -- not specific enough - I think you can download Excel files of other things too -->

<!-- see notes within the table about descriptions that need to be edited -->

>[!TIP]
>
> In einer heruntergeladenen Tabelle werden alle bearbeitbaren Spalten blau hervorgehoben.

| Abschnitt | Spalte | Beschreibung | Bearbeitbar? |
|---------|--------|-------------|-----------|
| [!UICONTROL Basic] | [!UICONTROL Placement ID] | Die numerische ID der Platzierung. | — |
| [!UICONTROL Basic] | [!UICONTROL Placement Name] | Der Name der Platzierung. | Ja |
| [!UICONTROL Basic] | [!UICONTROL Labels] | Alle angewendeten Beschriftungen für die Berichterstellung. | — |
| [!UICONTROL Basic] | [!UICONTROL Edit Link] | Ein Link zum Öffnen der Platzierung im Bearbeitungsmodus. | — |
| [!UICONTROL Basic] | [!UICONTROL Status] | Der Platzierungsstatus: *[!UICONTROL active]* oder *[!UICONTROL inactive]*. | Ja |
| [!UICONTROL Basic] | [!UICONTROL Placement Type] | Der Platzierungstyp. | — |
| [!UICONTROL Basic] | [!UICONTROL Package Name] | Der Name des übergeordneten Pakets, sofern zutreffend. | — |
| [!UICONTROL Goals] | [!UICONTROL Start Date] | Das Startdatum der Platzierung. | — |
| [!UICONTROL Goals] | [!UICONTROL End Date] | Das Enddatum der Platzierung. | — |
| [!UICONTROL Goals] | [!UICONTROL Day parting] | Ob Dayparting *[!UICONTROL ON]* oder *[!UICONTROL OFF]*.<br><b>Hinweis:</b> Um den tatsächlichen Dayparting-Zeitplan zu überprüfen, öffnen Sie die Platzierungseinstellungen in DSP. | — |
| [!UICONTROL Goals] | [!UICONTROL Budget] | Das Platzierungsbudget, falls vorhanden. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Budget Interval] | Das Budgetintervall: &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />*, *[!UICONTROL Weekly]*, *[!UICONTROL Monthly]* oder *[!UICONTROL All Time]*.[!UICONTROL >Daily] | Ja |
| [!UICONTROL Goals] | [!UICONTROL Optimization Goal] | Ziel des Pakets. | — |
| [!UICONTROL Goals] | [!UICONTROL Optimization Target] | Der Zielwert des Ziels. | — |
| [!UICONTROL Goals] | [!UICONTROL Pace on] | Ob die Platzierung in Richtung *[!UICONTROL Budget]* oder *[!UICONTROL Impressions]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Max Bid] | Das Höchstangebot für die Platzierung. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Flight Pacing] | Die Flugplatzierungsstrategie für die Platzierung: *[!UICONTROL Even]*, *[!UICONTROL slightly ahead]*, *[!UICONTROL frontload]* oder *[!UICONTROL aggressive frontload]*. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Intraday Pacing] | Die Intraday-Geschwindigkeit für die Platzierung: *[!UICONTROL Even]* oder *[!UICONTROL ASAP]*. | Ja |
| [!UICONTROL Goals] | [!UICONTROL  Pre-Bid Filters] | Alle anzuwendenden Filterkriterien vor dem Angebot. | — |
| [!UICONTROL Goals] | [!UICONTROL Bidding Rules] | Ob Angebotsregeln (nicht mehr unterstützt) *[!UICONTROL ON]* oder *[!UICONTROL OFF]*. | — |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap] | Die primäre Frequenzbegrenzung für die Platzierung während der angegebenen [!UICONTROL Frequency Cap Interval]. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Frequency Cap Interval] | Das Intervall für die primäre Häufigkeitsbegrenzung: *[!UICONTROL Day]*, *[!UICONTROL Week]* oder *[!UICONTROL Month]*. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap] | Die sekundäre Frequenzbegrenzung für die Platzierung während der angegebenen [!UICONTROL Secondary Frequency Cap Interval] | Ja |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval] | Die Art des Intervalls für die sekundäre Häufigkeitsbegrenzung: *[!UICONTROL Week]*, *[!UICONTROL Day]*, *[!UICONTROL Hour]* oder *[!UICONTROL Minute]*. Die anwendbare Anzahl von Wochen, Tagen, Stunden oder Minuten wird durch die Variable [!UICONTROL Secondary Frequency Cap Interval Value]. | Ja |
| [!UICONTROL Goals] | [!UICONTROL Secondary Frequency Cap Interval Value] | Die Anzahl der Wochen, Tage, Stunden oder Minuten, für die die Variable [!UICONTROL Secondary Frequency Cap] gilt. Wenn die sekundäre Begrenzung beispielsweise drei Impressionen pro sechs Stunden beträgt, wäre der Wert hier <b>6&lt;/>. | Ja |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included #] | Anzahl der geografischen Zielorte, *[!UICONTROL All]* oder *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Included] | Die geografischen Zielorte, getrennt durch Semikolons, oder *[!UICONTROL All Locations]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded #] | Anzahl der ausgeschlossenen geografischen Standorte oder *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Location] | [!UICONTROL Audience Location - Excluded] | die ausgeschlossenen geografischen Standorte, getrennt durch Semikolons, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Included #] | die Anzahl der gezielten öffentlichen Inventargeschäfte, sofern vorhanden, *[!UICONTROL All]* oder *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Public Inventory - Excluded #] | die Anzahl der ausgeschlossenen öffentlichen Inventargeschäfte, sofern vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Included #] | die Anzahl der zielgerichteten privaten Inventargeschäfte, sofern vorhanden; *[!UICONTROL All]* oder *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL Private Inventory - Excluded #] | die Anzahl der ausgeschlossenen privaten Inventargeschäfte, sofern vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Included #] | Anzahl der Zielkontakte [!UICONTROL On-Demand Inventory] Geschäfte, falls angegeben, *[!UICONTROL All]* oder *[!UICONTROL None]*. | — |
| [!UICONTROL Inventory] | [!UICONTROL On Demand Inventory - Excluded #] | die Anzahl der ausgeschlossenen On-Demand-Lagerergänzungen, sofern vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Traffic Type] | Zieltyp des Traffics: *[!UICONTROL Website]* und/oder *[!UICONTROL Apps]* | — |
| [!UICONTROL Sites] | [!UICONTROL Exclude out-stream] | Ob die Option &quot;Inventar-Targeting&quot;zum Ausschließen von ausgehendem Traffic lautet &lt;i span=&quot;&quot; id=&quot;0&quot; translate=&quot;no&quot; />* oder *[!UICONTROL OFF]*.[!UICONTROL >ON]<br>Über dem Inhalt angezeigte Werbeanzeigen werden in der Regel als Popup oder als Inhaltsangabe (im nativen Erlebnis) und nicht als normale Videoanzeigen in einem Videoplayer angezeigt. | — |
| [!UICONTROL Sites] | [!UICONTROL Site Tier] | Die Qualität der Zielstandorte: *[!UICONTROL Tier 1]*, *[!UICONTROL Tier 2]*, *[!UICONTROL Tier 3]* oder *[!UICONTROL All Sites]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Included #] | die Anzahl der Zielgruppenkategorien, sofern vorhanden, oder *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Categories - Excluded #] | die Anzahl der ausgeschlossenen Site-Kategorien, sofern vorhanden, oder *[!UICONTROL All]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Excluded Sites] | Ausgeschlossene Sites, sofern angegeben, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Sites] | [!UICONTROL Language] | Die Zielsprachen der Site. | — |
| [!UICONTROL Sites] | [!UICONTROL Allow unscreened sites] | (Nur Standardplatzierungen für die Anzeige) Gibt an, ob die Anzeigenbereitstellung auf nicht geprüften Sites zulässig ist: *[!UICONTROL ON]* oder *[!UICONTROL OFF]*. Wenn die Platzierung auf den privaten Bestand ausgerichtet ist, kann diese Option Anzeigen auf blockierten Sites bereitstellen. | — |
| [!UICONTROL Sites] | [!UICONTROL Targeted Sites] | die Anzahl der Zielseiten, sofern vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Included] | Zielgruppenzielgruppen, sofern vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Audience - Excluded] | die ausgeschlossenen Zielgruppen, sofern angegeben, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Demographic booster] | Ob oder nicht [!DNL Comscore] demografische Segmente sind für die Platzierung (und andere Platzierungen in der Kampagne) aktiviert: *[!UICONTROL ON]* oder *[!UICONTROL OFF]*. Diese Funktion kann nur für Kampagnen aktiviert werden, für die die Variable [!DNL Audience Verification] aktiviert ist für [!DNL Nielsen] und/oder [!DNL Comscore].  Es fallen zusätzliche Gebühren an. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Extend across screens] | Ob das Anzeigen-Targeting geräteübergreifend erweitert werden soll: *[!UICONTROL ON]* oder *[!UICONTROL OFF]*. Geräteübergreifendes Targeting erweitert Ihr Targeting auf das gesamte bekannte Gerät einer Person entsprechend dem in den Kampagneneinstellungen angegebenen Gerätediagramm. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting] - Include # | die Anzahl der Zielthema-Codes, sofern vorhanden, oder *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Topic Targeting - Excluded #] | die Anzahl der ausgeschlossenen Themencodes, sofern vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Included #] | die Anzahl der Zielgeräteziele, sofern vorhanden, oder *[!UICONTROL All]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL Device Targeting - Excluded #] | Anzahl der ausgeschlossenen Geräteziele, sofern vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Included #] | Anzahl der ISP-Anbieter, falls angegeben, oder *[!UICONTROL All]/i>. | — |
| [!UICONTROL Audience Targeting] | [!UICONTROL ISP Targeting - Excluded #] | die Anzahl der ausgeschlossenen ISP-Anbieter, sofern angegeben, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Contextual Filtering #] | die Anzahl der angewendeten Filter zur Markensicherheit, sofern angegeben, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Fraud blocking #] | die Anzahl der angewendeten Blockierungsfilter für Betrug vor dem Angebot, sofern vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Brand Safety - Pre-Bid Viewability #] | die Anzahl der angewendeten Sichtbarkeitsfilter vor dem Gebot, sofern vorhanden, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Brand Safety] | [!UICONTROL Site Safety Block] | Gibt an, ob der Site-Sicherheitsblock aktiviert ist: *[!UICONTROL ON]* oder *[!UICONTROL OFF]*.<!-- Whether or not the advertiser-level setting Enable Site Safety Block is enabled: *ON* or *OFF*.I don’t see this option at the placement level. Should there be one? --> | — |
| [!UICONTROL Tracking] | [!UICONTROL Tracking Pixels #] | Die Anzahl der an die Platzierung angehängten Pixel für Drittanbieter-Ereignisverfolgung oder *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL Conversion Pixels #] | Die Anzahl der Konversions-Tracking-Pixel, die an die Platzierung angehängt sind, oder *[!UICONTROL None]*. | — |
| [!UICONTROL Tracking] | [!UICONTROL 3rd-party fees] | Ein statischer Drittanbieter-Gebührensatz, der als nicht abrechnungsfähige Kosten pro 1000 Impressionen verfolgt werden kann, falls zutreffend. | — |
| [!UICONTROL Ads] | [!UICONTROL # of Ads Attached] | die Anzahl der Anzeigen, die mit der Platzierung verbunden sind (sofern vorhanden), oder *[!UICONTROL None]*. | — |
| [!UICONTROL Ads] | [!UICONTROL Ad Names] | die Namen der mit der Platzierung verknüpften Anzeigen, sofern vorhanden, oder *[!UICONTROL None]*. | — |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Informationen zum Korrigieren der Platzierungseinstellungen für eine Kampagne mithilfe von Tabellen](qa-about.md)
>* [Platzierungseinstellungen für eine Kampagne herunterladen](qa-sheet-download.md)
>* [Platzierungseinstellungen für eine Kampagne hochladen](qa-sheet-upload.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)

