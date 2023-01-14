---
title: Verwenden [!DNL Roku] Bestand
description: Erfahren Sie mehr über DSP Partnerschaft mit [!DNL Roku], einschließlich Lagerbestandsoptionen, genehmigten Drittanbieter-Tracking-Anbietern und Best Practices für [!DNL Roku]-spezifische Platzierungen.
feature: DSP On Demand Inventory, DSP Private Inventory
exl-id: 0cd42782-f006-4aa8-b879-322f86cfac4b
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# Verwenden [!DNL Roku] Bestand

Advertising DSP bietet einzigartige Funktionen für Werbung in [!DNL Roku].

## DSP und [!DNL Roku] Partnerschaft

Roku und DSP haben eine einzigartige Partnerschaft, die mit Ihrer [!DNL DSP] Zielgruppen zu [!DNL Roku] IDs für 1:1-deterministisches Zielgruppen-Targeting für [!DNL Roku] Inventar.

Außerhalb der eigenen DSP (OneView) von Roku hat Advertising DSP ausschließlich Zugriff auf diese Targeting-Funktionen. Advertising DSP ist auch die einzige DSP mit der Berechtigung zum Messen [!DNL Roku] neben allen anderen angeschlossenen TV-Inventaren (CTV). weil [!DNL Roku] gibt nicht alle standardmäßigen RTB- und Impression-Pixelsignale frei, keine anderen DSP können auf Roku-verkaufte CTV-Geräte abzielen oder diese messen.

## [!DNL Roku] Inventaroptionen

Sie können entweder a) private Deal-IDs direkt mit [!DNL Roku] und geben Sie dann die Deal-ID-Daten in DSP oder b) besuchen Sie die [!DNL On Demand] Abonnierte Galerie [!DNL Roku] Profile:

>[!NOTE]
>
>[!DNL Roku] Inventar ist nicht an offenen Marktplätzen und Börsen verfügbar.

* Für Ihre privaten Angebote: [Informationen zu den Deal-IDs in DSP einrichten](/help/dsp/inventory/deal-id-create.md) und anschließend auf &quot;[!UICONTROL Roku Network – Audience]&quot; und &quot;[!UICONTROL The Roku Channel – Audience]&quot; [!DNL Roku] Platzierungen.<!-- Or do you target the deal ID?? I see those strings for Roku On Demand inventory. Clarify if all Roku private deals will show up as one or the other of these in Roku Private inventory in Roku placement settings. -->

* Sie können [Abonnieren Sie Folgendes [!DNL Roku] Inventar innerhalb der [!DNL On Demand] Galerie](/help/dsp/inventory/on-demand-inventory-subscribe.md), und wählen Sie anschließend eines der genehmigten Angebote aus, die unter [!DNL Roku] Platzierungen:

   * &quot;[!UICONTROL Roku Network – Audience]&quot; für das Inventar im gesamten [!DNL Roku] Ökosystem mit Premium-Inhaltspartnern wie [!DNL The CW], [!DNL ABC]und [!DNL ESPN].
   * &quot;[!UICONTROL The Roku Channel – Audience]&quot; [!DNL Roku] eigene und betriebene App-Inhalte (O&amp;O).

### Vorteile der Anpassung privater Marketplace mit [!DNL Roku]

Private Deals ermöglichen es Ihnen, die Deal-Parameter nach Ihren Bedürfnissen anzupassen.

* **Verhandlungspreise:** Arbeiten mit [!DNL Roku] Vertriebsteam, um ein Geschäft auszuhandeln und zu strukturieren, das Ihren Kampagnenanforderungen entspricht.

* **Skalierungspriorität:** Private Marketplace (PMPs) erhalten eine höhere Priorität als Always-on-Angebote (z. B. [!DNL On Demand] Angebote).

* **Frequenzverwaltung:** Die [!DNL Roku] Die standardmäßige Frequenzlimitierung beträgt eine (1) Anzeige pro 30 Minuten pro Benutzer, Sie können die Obergrenze jedoch nach Stunde, Tag, Woche, Monat oder dem gesamten Flugzeitraum anpassen.<!-- Within the DSP placement settings? NO - you negotiate this with Roku, but Christine to confirm with Amanda whether you should be able to edit this in placement. -->

* **[!DNL Roku]Daten-Targeting:** [!DNL Roku] Zielgruppen werden aus [!DNL Roku] Geräte- und Fernsehsignale, Daten, die von [!DNL The Roku Channel] (z. B. Affinität zum TV-Genre, Streaming-TV-Verhalten und Kabelabonnementstatus) sowie zusätzliche Daten aus dem [!DNL Roku] CRM-System (Customer Relationship Management).

* **[!DNL Roku]Content-Targeting:** Private Deals können Apps nach Genre, Anwendung der App-Blockierungsliste, saisonalen und zehnpeilen Ereignissen sowie in [!DNL The Roku Channel] nur.

## [!DNL Roku] Praktika

In DSP Kampagnen [erstellen [!DNL Roku]-spezifische Platzierungen](/help/dsp/campaign-management/placements/placement-create.md) mit dem Platzierungstyp &quot;[!UICONTROL Connected TV (Roku)].&quot; Einschließen [!DNL Roku] Platzierungen in [!DNL Roku]-spezifische Pakete mit definierten Zielen.

Jeder [!DNL Roku] Platzierung muss mindestens eine Zielgruppe enthalten [!DNL Roku] Geschäft oder Quelle. So verwenden Sie DSP eindeutige Zielgruppenabgleich mit [!DNL Roku], ein oder mehrere Zielgruppensegmente einschließen, die mit der [!DNL Roku] (Opt-in) deterministischer Datensatz.

### [!DNL Roku]-Genehmigte Drittanbieter-Tracking-Anbieter

[!DNL Roku] Platzierungen können Drittanbieter-Ereignispixel und Konversionspixel von den folgenden Anbietern enthalten:  [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]und [!DNL Research Now].

### Best Practices nach Platzierungsstrategie

Im Folgenden finden Sie die empfohlenen Vorgehensweisen für [!DNL Roku]-spezifische Platzierungen.

So maximieren Sie die inkrementelle Reichweite:

* Unterdrücken von freigegebenen Zielgruppen in [!DNL Roku O&O] durch Ausschließen von bereits erreichten Zielgruppen mithilfe von [!DNL The Roku Channel].

* Unterdrücken von freigegebenen Zielgruppen in [!DNL All Roku] durch Ausschließen von Zielgruppen, die Sie bereits in der [!DNL Roku] Plattform.

Für die schnellste Einrichtung:

* Targeting vorhandener, jederzeit aktualisierter Angebote für [!DNL The Roku Channel] in [[!DNL On Demand] Bestand](/help/dsp/inventory/on-demand-inventory-subscribe.md) für einen schnellen Zugriff [!DNL Roku] Eigenbesitz und Betriebsvorrat.
* Targeting vorhandener, jederzeit aktualisierter Angebote für [!DNL Roku Network] in [[!DNL On Demand] Bestand](/help/dsp/inventory/on-demand-inventory-subscribe.md) schnell Skalierung über [!DNL Roku] Plattform.

Maximale Skalierung:

* Anpassen einer [!DNL Roku] privater Marktplatz für priorisierten Zugriff auf [!DNL Roku] Lieferung zu einem ausgehandelten Preis.

>[!MORELIKETHIS]
>
>* [Manuelles Erstellen von Details zur Angebots-ID](/help/dsp/inventory/deal-id-create.md)
> * [Abonnieren und Zugriff anfordern für [!DNL On Demand] Premium-Inventarangebote](/help/dsp/inventory/on-demand-inventory-subscribe.md)
>* [Erstellen einer Platzierung](/help/dsp/campaign-management/placements/placement-create.md)

