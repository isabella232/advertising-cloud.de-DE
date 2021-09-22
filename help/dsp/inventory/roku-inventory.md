---
title: Verwenden von [!DNL Roku] Bestand
description: 'Erfahren Sie mehr über DSP Partnerschaft mit [!DNL Roku], including inventory options, approved third-party tracking vendors, and best practices for [!DNL Roku]-spezifischen Platzierungen. '
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: 0cd42782-f006-4aa8-b879-322f86cfac4b
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---

# Verwenden von [!DNL Roku] Inventar

Advertising Cloud DSP bietet einzigartige Werbefunktionen für [!DNL Roku].

## Die Partnerschaft Advertising Cloud DSP und [!DNL Roku]

Roku und Advertising Cloud DSP verfügen über eine eindeutige Partnerschaft, die Ihre [!DNL DSP]-Zielgruppen mit [!DNL Roku]-IDs für das deterministische 1:1-Zielgruppen-Targeting für [!DNL Roku]-Inventar abgleicht.

Außerhalb der eigenen DSP (OneView) von Roku hat Advertising Cloud DSP ausschließlich Zugriff auf diese Targeting-Funktionen. Advertising Cloud DSP ist auch die einzige DSP, die berechtigt ist, die [!DNL Roku]-Bereitstellung neben dem gesamten anderen angeschlossenen TV-Inventar (CTV) zu messen. Da [!DNL Roku] nicht alle standardmäßigen RTB- und Impression-Pixelsignale gemeinsam nutzt, können keine anderen DSP über das Roku-verkaufte CTV-Angebot hinweg Zielgruppen bestimmen oder messen.

## [!DNL Roku] Inventaroptionen

Sie können entweder a) private Deal-IDs direkt mit [!DNL Roku] einrichten und dann die Deal-ID-Daten in DSP eingeben oder b) die Galerie [!DNL On Demand] besuchen, um [!DNL Roku]-Profile zu abonnieren:

>[!NOTE]
>
>[!DNL Roku] Inventar ist nicht an offenen Marktplätzen und Börsen verfügbar.

* Bei Ihren privaten Angeboten richten Sie [Informationen über die Deal-IDs in DSP](/help/dsp/inventory/deal-id-create.md) ein und richten dann &quot;[!UICONTROL Roku Network – Audience]&quot;und &quot;[!UICONTROL The Roku Channel – Audience]&quot;innerhalb von [!DNL Roku] Platzierungen ein.<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals will show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* Sie können [folgende [!DNL Roku] inventory within the [!DNL On Demand] Galerie](/help/dsp/inventory/on-demand-inventory-subscribe.md) abonnieren und dann genehmigte Angebote innerhalb von [!DNL Roku] Platzierungen als Ziel auswählen:

   * &quot;[!UICONTROL Roku Network – Audience]&quot;für Inventar im gesamten [!DNL Roku]-Ökosystem mit Premium-Inhaltspartnern wie [!DNL The CW], [!DNL ABC] und [!DNL ESPN].
   * &quot;[!UICONTROL The Roku Channel – Audience]&quot;für [!DNL Roku] eigene und betriebene (O&amp;O) App-Inhalte.

### Vorteile der Anpassung privater Marketplace mit [!DNL Roku]

Private Deals ermöglichen es Ihnen, die Deal-Parameter nach Ihren Bedürfnissen anzupassen.

* **Verhandlungspreise:** Arbeiten Sie mit dem  [!DNL Roku] Verkaufsteam zusammen, um ein Geschäft auszuhandeln und zu strukturieren, das Ihren Kampagnenanforderungen entspricht.

* **Skalierungspriorität:** Private Marktplätze (PMPs) erhalten eine höhere Priorität als Angebote, die immer verfügbar sind (z. B.  [!DNL On Demand] Angebote).

* **Frequenzverwaltung:** Die  [!DNL Roku] standardmäßige Frequenzlimitierung beträgt eine (1) und pro 30 Minuten pro Benutzer. Sie können die Obergrenze jedoch nach Stunde, Tag, Woche, Monat oder dem gesamten Flugzeitraum anpassen.<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]Data Targeting:** [!DNL Roku] Zielgruppen werden aus  [!DNL Roku] Geräte- und TV-Signalen, von verfolgten Daten ( [!DNL The Roku Channel] z. B. Affinität zum TV-Genre, Streaming-TV-Verhalten und Kabelabonnementstatus) sowie zusätzlichen Daten aus dem  [!DNL Roku] Customer Relationship Management (CRM)-System erstellt.

* **[!DNL Roku]Content-Targeting:** Private Angebote können für Apps nach Genre, Anwendung der App-Blockierungsliste, saisonalen und zehnpol-Ereignissen und  [!DNL The Roku Channel] nur innerhalb von Zielgruppen ausgewählt werden.

## [!DNL Roku] Praktika

In DSP Kampagnen [erstellen Sie [!DNL Roku]-spezifische Platzierungen](/help/dsp/campaign-management/placements/placement-create.md) mit dem Platzierungstyp &quot;[!UICONTROL Connected TV (Roku)]&quot;. Sie werden [!DNL Roku] Platzierungen in [!DNL Roku]-spezifische Pakete mit definierten Zielen einbeziehen.

Jede [!DNL Roku]-Platzierung muss mindestens einen [!DNL Roku] -Deal oder eine Quelle enthalten. Um DSP eindeutige Zielgruppenabgleich mit [!DNL Roku] zu nutzen, schließen Sie mindestens ein Zielgruppensegment ein, das mit dem [!DNL Roku] (Opt-in) deterministischen Datensatz abgeglichen werden kann.

### [!DNL Roku]-Genehmigte Drittanbieter-Tracking-Anbieter

[!DNL Roku] Platzierungen können Drittanbieter-Ereignispixel und Konversionspixel von den folgenden Anbietern enthalten:   [!DNL Acxiom],  [!DNL comScore],  [!DNL Data Plus Math],  [!DNL Experian],  [!DNL Factual],  [!DNL Kantar],  [!DNL Marketing Evolution],  [!DNL Neustar],  [!DNL Nielsen],  [!DNL Nielsen Catalina Solutions],  [!DNL NinthDecimal],  [!DNL Oracle],  [!DNL Placed] und  [!DNL Polk]  [!DNL Research Now].

### Best Practices nach Platzierungsstrategie

Im Folgenden finden Sie die empfohlenen Vorgehensweisen für [!DNL Roku]-spezifische Platzierungen.

So maximieren Sie die inkrementelle Reichweite:

* Unterdrücken Sie die angezeigten Zielgruppen in [!DNL Roku O&O], indem Sie bereits erreichte Zielgruppen mit [!DNL The Roku Channel] ausschließen.

* Unterdrücken Sie die angezeigten Zielgruppen in [!DNL All Roku], indem Sie Zielgruppen ausschließen, die Sie bereits auf der [!DNL Roku]-Plattform erreicht haben.

Für die schnellste Einrichtung:

* Targeting vorhandener, immer genutzter Angebote für [!DNL The Roku Channel] in [[!DNL On Demand] Inventar](/help/dsp/inventory/on-demand-inventory-subscribe.md), um schnell auf [!DNL Roku] eigene und betriebene Bestände zugreifen zu können.
* Richten Sie vorhandene, immer verfügbare Angebote für [!DNL Roku Network] in [[!DNL On Demand] Inventar](/help/dsp/inventory/on-demand-inventory-subscribe.md) ein, um schnell eine Skalierung auf der [!DNL Roku]-Plattform zu erzielen.

Maximale Skalierung:

* Passen Sie einen [!DNL Roku] privaten Marktplatz für priorisierten Zugriff auf [!DNL Roku]-Angebote zu einem ausgehandelten Preis an.

>[!MORELIKETHIS]
>
>* [Manuelles Erstellen von Details zur Angebots-ID](/help/dsp/inventory/deal-id-create.md)
> * [Abonnieren und Anfordern des Zugriffs  [!DNL On Demand] auf Premium Inventory Deals](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [Erstellen einer Platzierung](/help/dsp/campaign-management/placements/placement-create.md)

