---
title: Übersicht über die Kampagnenverwaltung in Advertising Cloud DSP
description: Erfahren Sie mehr über die Kampagnenverwaltungshierarchie und -komponenten.
feature: Packages, Placements, Ads, Creatives
exl-id: c94e08d0-0dd5-4cf9-8df2-9eb4c591375c
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---

# Übersicht über die Kampagnenverwaltung in Advertising Cloud DSP

Advertising Cloud DSP-Kampagnen weisen die folgende Hierarchie auf:

* Kampagne
   * Paket(e)
      * Platzierung(en)
         * Anzeigen
            * Kreativ(e)

<!-- Do clients think in terms of insertion orders? If yes, then work in the following info.:
In Advertising Cloud DSP, an insertion order is represented as a campaign, and line items are represented as packages. Each package will include placements, which can use different strategies and tactics to deliver the line item requirements.
-->

## [!UICONTROL Campaigns]

[](/help/dsp/campaign-management/campaigns/campaign-about.md) Kampagnen bilden den übergeordneten Rahmen der Flugeinstellungen. Jede Kampagne wird mit einem Advertiser, Start- und Enddaten, einem Gesamtbudget, einer geräteübergreifenden Targeting-Option und einer standardmäßigen Frequenzbegrenzung sowie Berichtsoptionen für Sichtbarkeit, Betrug, Markensicherheit und Zielgruppenüberprüfung konfiguriert. Alle Einstellungen auf Kampagnenebene gelten automatisch für jedes Paket und jede Platzierung innerhalb der Kampagne.

## [!UICONTROL Packages]

Jede Kampagne kann ein oder mehrere [Pakete](/help/dsp/campaign-management/packages/package-about.md) enthalten, von denen jede eine Reihe von Platzierungen enthält.

Verwenden Sie Pakete, um Platzierungen für die Bereitstellung in einem festgelegten Budget, Leistungsziel und einer benutzerdefinierten Schrittstrategie zu gruppieren. DSP optimiert Pakete, indem Budgets auf die leistungsstärksten Platzierungen im Paket umgestellt werden. Sie können Pakete nach Platzierungsformat, Inventartyp, Datenanbieter, Persona oder anderen unterscheidbaren Eigenschaften organisieren.

Pakete sind optional, werden jedoch empfohlen.

## [!UICONTROL Placements]

Eine [placement](/help/dsp/campaign-management/placements/placement-about.md) speichert Targeting-Parameter für eine oder mehrere Anzeigen desselben Anzeigentyps. Sie können eine Platzierung für eine einzelne Kampagne oder ein einzelnes Paket erstellen und ihr dann Anzeigen zuweisen.

## [!UICONTROL Ads]

[](/help/dsp/campaign-management/ads/ad-about.md) Fügen Sie kreative Assets und Tracking-URLs hinzu. Sie können entweder Ihre kreativen Assets hochladen und DSP die Werbeanzeigen bereitstellen, die sie kostenlos nutzen, oder Sie können Werbe-Tags von Drittanbietern hochladen.

Sobald Ihre Anzeigen eingerichtet sind, müssen Sie jede Anzeige an eine Platzierung anhängen. Sie können eine einzelne Anzeige an eine oder mehrere Platzierungen anhängen.

Alle aktiven, genehmigten Anzeigen in einer aktiven Platzierung in einer aktiven Kampagne können auf der Grundlage der Platzierungs-Targeting-Parameter ausgeführt werden.

## [!UICONTROL Creatives]

Sie können Audio- und Videodateien hochladen, um sie in Anzeigen für bestimmte Kampagnen zu verwenden.
<!-- add link to [About Creative Management](/help/dsp/campaign-management/creatives/creative-about.md) when it's available-->

Sie können sofort eine Werbeanzeige mit dem hochgeladenen Kreativelement erstellen, oder Sie können später eine Werbeanzeige aus der Creatives-Ansicht oder aus der Anzeigen-Ansicht erstellen.

>[!MORELIKETHIS]
>
>* [Über Campaign Management](/help/dsp/campaign-management/campaigns/campaign-about.md)
>* [Über Package Management](/help/dsp/campaign-management/packages/package-about.md)
>* [Über die Platzierungsverwaltung](/help/dsp/campaign-management/placements/placement-about.md)
>* [Über die Anzeigenverwaltung](/help/dsp/campaign-management/ads/ad-about.md)
>* [Checkliste für den Kampagnenstart](/help/dsp/campaign-management/campaign-launch-checklist.md)
>* [Best Practices zum Einrichten von Leistungskampagnen](/help/dsp/optimization/campaign-best-practices-performance.md)
>* [Über In-Platform-Berichte](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Über Datenansichten in Campaign](/help/dsp/campaign-management/reports/campaign-data-views-about.md)

