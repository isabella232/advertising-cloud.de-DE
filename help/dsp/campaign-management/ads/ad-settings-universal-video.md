---
title: Universelle Videoanzeigeneinstellungen
description: Siehe Beschreibungen der verfügbaren Anzeigeneinstellungen für universelle Videoanzeigen.
feature: DSP Ads
exl-id: 0be86b84-78f9-4429-a8b7-8195891875ca
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '449'
ht-degree: 0%

---

# Universelle Videoanzeigeneinstellungen

*Open-Beta-Funktion*

## [!UICONTROL Insert Ad Tag]

*Nur neue Anzeigen*

**[!UICONTROL URL]:** Die VAST-Tag-URL.

**[!UICONTROL Title]:** Ein Titel für die Datei, der sich im [!UICONTROL Ads] Anzeigen und Berichten.

>[!TIP]
>
> Um die Gültigkeit eines VAST-Tags zu überprüfen, fügen Sie es in einen Browser ein und drücken Sie die **[!UICONTROL Enter]** Schlüssel. Wenn das Tag gültig ist, wird eine XML-Datei angezeigt, die Folgendes enthält: `<VAST>` oben.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Schreibgeschützt) Der Anzeigentyp, den Sie erstellen. Er entspricht dem Platzierungstyp, an den die Anzeige angehängt werden kann.

**[!UICONTROL Ad Name]:** Der Anzeigenname. Der Asset-Titel wird standardmäßig verwendet, Sie können jedoch den Namen ändern.

>[!TIP]
>
> Verwenden Sie einen Namen, der leicht zu finden ist, wenn Sie die Anzeige an eine Platzierung anhängen, in der [!UICONTROL Ads] und in Berichten anzeigen. Beschreiben Sie beispielsweise den Einheitentyp und einige wichtige Attribute (z. B. die Holiday-Produktvorschau: 30 Sek. Universal Video&quot;).

**[!UICONTROL Show Controls]:** Wo Sie Videosteuerelemente für die Anzeige einbeziehen: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* oder *[!UICONTROL None]* (Standardeinstellung).

**[!UICONTROL Preserve Aspect Ratio]:** Gibt an, ob die Breite und Höhe des Videos (*[!UICONTROL Yes]*) oder um das Video so zu dehnen, dass der verfügbare Platz (*[!UICONTROL No]*).

**[!UICONTROL VAST Tag]:** (Anzeigen, die nur VAST-Tags verwenden; schreibgeschützt) Das VAST-Tag des Drittanbieters, das Sie als Anzeigenquelle eingegeben haben.

**[!UICONTROL Final VAST Tag]:** (Anzeigen, die nur VAST-Tags verwenden; schreibgeschützt) Das VAST-Tag des Drittanbieters, das Sie als Anzeigenquelle mit dem erforderlichen [Anzeigen DSP Tracking-Makros](/help/dsp/campaign-management/macros.md) gegebenenfalls eingefügt.

**[!UICONTROL Wmode]:** Der Fenstermodus: *[!UICONTROL window]*, *[!UICONTROL transparent]* oder *[!UICONTROL opaque]*. Wenn diese Einstellung nicht anwendbar ist, lassen Sie sie leer.

**[!UICONTROL Video Format]:** Das Format des Anzeigen-Players für das potenzielle Inventar: *[!UICONTROL VPAID]*, *[!UICONTROL VPAID & VAST]* oder *[!UICONTROL VAST]*. Die Sichtbarkeit wird immer für [!UICONTROL VPAID], aber [!UICONTROL VPAID & VAST] enthält Inventar, das keine Sichtbarkeitsmessung zulässt. Beachten Sie diese Unterscheidung, wenn Sichtbarkeitsmetriken für Ihre Kampagne wichtig sind.

Verwendung *[!UICONTROL VAST]*, was keine Sichtbarkeitsmessung zulässt, wenn Sie angeschlossene Fernsehgeräte oder Inventare auswählen, für die ausschließlich das VAST-Format erforderlich ist (normalerweise aus Versorgungsquellen wie Google Ad Manager, Appnexus, SpotX und Freewheel).

**[!UICONTROL Clock Number]**: (nur im Vereinigten Königreich verwendet; nur für Benutzer mit Berechtigung verfügbar) Eine eindeutige ID, mit der sichergestellt wird, dass die richtige Anzeige gesendet wird. Wenn diese Einstellung nicht anwendbar ist, lassen Sie sie leer.

### [!UICONTROL Pixel]

Alle vorhandenen Ereignis-Tracking-Pixel für die Platzierung werden automatisch angehängt. Sie können vorhandene Pixel trennen und je nach Ihren Tracking-Anforderungen für die einzelne Anzeige neue Pixel erstellen.

Die folgenden Einstellungen gelten für jedes Pixel, das Sie erstellen oder bearbeiten.

**[!UICONTROL Integration Event]:** Das Ereignis, bei dem das Pixel Trigger wird, um ausgelöst zu werden. Verwenden Sie für diesen Anzeigentyp Pixel, die auf dem *[!UICONTROL Impression]* oder *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Gibt an, ob das Pixel ein *[!UICONTROL IMG URL]* (1x1-Pixel-Bilddatei), *[!UICONTROL HTML]* oder *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** Die URL des Pixelbilds in dem für die [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** Der Pixelname. Verwenden Sie einen Namen, mit dem Sie das Pixel leicht identifizieren können.

**[!UICONTROL Pixel Provider]:** Der Pixelanbieter: *[!UICONTROL None]*, *[!UICONTROL Nielsen]* oder *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Über die Anzeigenverwaltung](ad-about.md)
>* [Einzelne Anzeige erstellen](ad-create.md)
>* [Platzierungen auflisten, die einer Anzeige zugeordnet sind](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Anzeigenspezifikationen](ad-specs.md)
>* [DSP Makros](/help/dsp/campaign-management/macros.md)

