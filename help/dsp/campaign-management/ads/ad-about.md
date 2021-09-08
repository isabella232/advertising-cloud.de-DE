---
title: Über die Anzeigenverwaltung in Advertising Cloud DSP
description: Erfahren Sie mehr über die Anzeigenverwaltung.
feature: Ads
exl-id: 72c8bbef-d09c-4cf4-994d-99578d043d39
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 0%

---

# Über die Anzeigenverwaltung in Advertising Cloud DSP

<!-- add "The Ads View (Dashboard?)" section -->

Advertising Cloud DSP bietet zwei Möglichkeiten, Ihre Anzeigen zu bedienen:

* Advertising Cloud DSP stellt Ihre Anzeigen kostenlos bereit, wenn Sie Ihre eigenen Assets (z. B. Display-Banner, Video-Assets, Audiodateien oder URLs) direkt in DSP hochladen. Bei DSP bereitgestellten Assets haben Sie Zugriff auf zusätzliche Funktionen wie Überlagerungen.

* Wenn Sie einen Drittanbieter-Werbeserver verwenden (z. B. Google, Flashspeak oder Sizmek), können Sie Ihre Drittanbieter-Werbe-Tags für einzelne DSP oder in großen Mengen hochladen. Für die Funktion zum Massen-Upload müssen Sie entweder a) DoubleClick- und Flashspeak-Tag-Tabellen hochladen oder b) eine Vorlage herunterladen, Ihre Tags in die Vorlage eingeben und dann die Vorlage erneut hochladen.<!-- need a list of all supported third-party ad servers; see file in future-tbd folder -->

Nachdem Sie Ihre Anzeigen eingerichtet haben, müssen Sie jede Anzeige an eine Platzierung anhängen, die die Targeting-Parameter (Geo, Zielgruppe, Gerät und Inventar-Targeting) enthält, die steuern, wie Ihre Kampagne bereitgestellt wird. Sie können eine einzelne Anzeige an eine oder mehrere Platzierungen anhängen.

## Verfügbare Anzeigentypen

* Audio
* Angeschlossener Fernseher
* Anzeige
* Mobile
* Nativ
* Pre-Roll

Weitere Informationen zu diesen Anzeigentypen finden Sie unter [Verfügbare Anzeigentypen](ad-types.md) und die vollständigen [Anzeigenspezifikationen](/help/dsp/assets/ad-specs.pdf).

## Spezielle Anzeigenfunktionen

Die folgenden Funktionen sind nur für DSP-bereitgestellte Anzeigen verfügbar.

### Companion Banner

Companion Banner werden zusammen mit [Pre-Roll-Anzeigen](ad-settings-pre-roll.md) oder (mit einigen Herausgebern) [Audio-Anzeigen](ad-settings-audio.md) bereitgestellt und können zur Stärkung der Marken- und Nachrichtenzuordnung beitragen.

>[!NOTE]
>
>* Nicht alle Herausgeber lassen begleitende Banner zu. Die Herausgeber, die begleitende Banner zulassen, garantieren keine begleitenden Bannerimpressionen.
>* Begleitbanner von Anzeigen-Tags von Drittanbietern stehen möglicherweise nicht immer für die Vorschau zur Verfügung.


Sie können Ihr eigenes begleitendes Banner-Asset hochladen oder ein iFrame- oder Skriptbanner-Tag eines Drittanbieters von einem zertifizierten Drittanbieter-Anzeigenbereitstellungspartner hochladen.

### Überlagerungen

Überlagerungen unterstützen das persistente Branding im gesamten Video und können zusätzliche Klicks bewirken. Die Überlagerungsfunktion ist für [interaktive Pre-Roll-Anzeigen](ad-settings-pre-roll.md) und für [mobile Anzeigen in interaktiven und Wiedergabe-Tippen](ad-settings-mobile.md)-Formaten verfügbar.

Siehe [Best Practices zum Erstellen von Überlagerungen](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)

### Teaser

Ein Teaser ist ein auffälliges Bild, das den Betrachter dazu bringt, eine Anzeige wiederzugeben. Teaser gelten nur für mobile Anzeigenformate mit &quot;Tippen auf Wiedergabe&quot;.

## Advertising Cloud DSP-Anzeigengenehmigungen

Wenn Sie eine Anzeige erstellen, prüft Advertising Cloud DSP sie auf sensible Kategorien, klickt auf URL-Funktionalität und zeigt die Vorschau an.

Zunächst wird in der Spalte [!UICONTROL Status] ein roter Punkt angezeigt. Der Überprüfungsprozess dauert normalerweise 24 bis 48 Stunden. Eine fehlerhafte Anzeige kann jedoch länger als 48 Stunden den Status &quot;Ausstehend&quot;aufweisen, sodass Sie Zeit haben, Fehler zu beheben, bevor die Anzeige abgelehnt wird. Abgelehnte Anzeigen enthalten einen Grund für die Ablehnung.

Wenn DSP eine Anzeige genehmigt, wird in der Spalte Status ein grüner Punkt angezeigt.

![Validierungsanzeiger in der  [!UICONTROL Status] Spalte](/help/dsp/assets/ad-approval-status.png)

>[!NOTE]
>
>Ihre Werbeanzeige wird nur bereitgestellt, wenn sowohl DSP als auch die SSP die Kreativinhalte genehmigt haben. Jeder SSP hat seine eigenen Genehmigungsanforderungen und -prozesse.

>[!MORELIKETHIS]
>
>* [Erstellen einer Anzeige](ad-create.md)
>* [Erstellen mehrerer Drittanbieteranzeigen](ad-create-third-party.md)
>* [Verfügbare Anzeigentypen](ad-types.md)
>* [Anzeigenspezifikationen](/help/dsp/assets/ad-specs.pdf)

