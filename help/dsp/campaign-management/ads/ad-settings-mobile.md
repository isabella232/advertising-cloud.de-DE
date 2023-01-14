---
title: Einstellungen für mobile Anzeigen
description: Siehe Beschreibungen der verfügbaren Anzeigeneinstellungen für mobile Anzeigen.
feature: DSP Ads
exl-id: f67c4ba0-1011-4ad6-bd36-98c312b81b67
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 0%

---

# Einstellungen für mobile Anzeigen

## [!UICONTROL Insert Ad Tag]

*Nur die neuen Anzeigenformate für mobile Videos*

**[!UICONTROL URL]** oder **[!UICONTROL Ad Tag]**: Ein VAST-Anzeigen-Tag oder Anzeigen-Tag eines Drittanbieters, das kreative Assets und Tracking-Pixel enthält

**[!UICONTROL Ad Title]** oder **[!UICONTROL Title]**: Ein Name für die Anzeige, die in der [!UICONTROL Ads] Anzeigen und Berichten.

>[!TIP]
>
> Um die Gültigkeit eines VAST-Tags zu überprüfen, fügen Sie es in einen Browser ein und drücken Sie die **[!UICONTROL Enter]** Schlüssel. Wenn das Tag gültig ist, wird eine XML-Datei angezeigt, die Folgendes enthält: `<VAST>` oben.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]: Display-Anzeigen für Mobilgeräte

**[!UICONTROL Ad Type]:** (Schreibgeschützt) Der Anzeigentyp, den Sie erstellen. Er entspricht dem Platzierungstyp, an den die Anzeige angehängt werden kann.

**[!UICONTROL Ad Name]:** Der Anzeigenname. Der Asset-Titel wird standardmäßig verwendet, Sie können jedoch den Namen ändern.

>[!TIP]
>
> Verwenden Sie einen Namen, der leicht zu finden ist, wenn Sie die Anzeige an eine Platzierung, in der Anzeigen-Ansicht und in Berichten anhängen. Beschreiben Sie beispielsweise den Einheitentyp und einige wichtige Attribute (z. B. die Holiday-Produktvorschau: 300x250 Gamer&quot;).

**\[Anzeigenquelle\]**: (schreibgeschützt) *[!UICONTROL 3rd party]*.

**[!UICONTROL Display Code]:** Die URL des kreativen Drittanbieter-Assets. Alle [timestamp] und [[timestamp]] -Parameter durch tatsächliche Werte ersetzt.

**[!UICONTROL Final Display Code]:** Die URL für das kreative Asset eines Drittanbieters mit den erforderlichen [Anzeigen DSP Tracking-Makros](/help/dsp/campaign-management/macros.md) gegebenenfalls eingefügt.

### [!UICONTROL Basic]: Videoanzeigen

**[!UICONTROL Ad Type]:** (Schreibgeschützt) Der Anzeigentyp, den Sie erstellen. Er entspricht dem Platzierungstyp, an den die Anzeige angehängt werden kann.

**[!UICONTROL Ad Name]:** Der Anzeigenname. Der Asset-Titel wird standardmäßig verwendet, Sie können jedoch den Namen ändern.

>[!TIP]
>
> Verwenden Sie einen Namen, der leicht zu finden ist, wenn Sie die Anzeige an eine Platzierung, in der Anzeigen-Ansicht und in Berichten anhängen. Beschreiben Sie beispielsweise den Einheitentyp und einige wichtige Attribute (z. B. die Holiday-Produktvorschau: 30 Sek. Telefonvorwahl&quot;).

**[!UICONTROL Width]| [!UICONTROL Ad Unit Width]:** Die Breite der gesamten Anzeigeneinheit. Diese Option kann je nach ausgewähltem Anzeigentyp gesperrt werden.

**[!UICONTROL Height]| [!UICONTROL Ad Unit Height]:** Die Höhe der gesamten Anzeigeneinheit. Diese Option kann je nach ausgewähltem Anzeigentyp gesperrt werden.

**[!UICONTROL Player X]:** Die X-Koordinate für die Anzeigeneinheit. Behalten Sie die Standardeinstellung bei.

**[!UICONTROL Player Y]:** Die Y-Koordinate für die Anzeigeneinheit. Behalten Sie die Standardeinstellung bei.

**[!UICONTROL Player Width]:** Die Breite der gesamten Anzeigeneinheit. Diese Option kann je nach ausgewähltem Anzeigentyp gesperrt werden.

Dies entspricht dem **[!UICONTROL Width]** -Feld.

**[!UICONTROL Player Height]:** Die Höhe der gesamten Anzeigeneinheit. Diese Option kann je nach ausgewähltem Anzeigentyp gesperrt werden.

Dies entspricht dem **[!UICONTROL Height]** -Feld.

**[!UICONTROL Show Controls]:** Wo Sie Videosteuerelemente für die Anzeige einbeziehen: *[!UICONTROL Under]*, *[!UICONTROL Over]*, *[!UICONTROL Bottom]* oder *[!UICONTROL None]* (Standardeinstellung).

**[!UICONTROL Preserve Aspect Ratio]:** Gibt an, ob die Breite und Höhe des Videos beibehalten werden sollen (*[!UICONTROL Yes]*) oder um das Video so zu dehnen, dass der verfügbare Platz (*[!UICONTROL No]*).

**[!UICONTROL Close Button Delay]:** (Einige Anzeigentypen) Die Anzahl der Sekunden, um die Anzeige der Schließen-Schaltfläche zu verzögern.

**[!UICONTROL VAST Tag]:** (Anzeigen, die nur VAST-Tags verwenden; schreibgeschützt) Das VAST-Tag des Drittanbieters, das Sie als kreatives Asset eingegeben haben.

**[!UICONTROL Final VAST Tag]:** (Anzeigen, die nur VAST-Tags verwenden; schreibgeschützt) Das VAST-Tag des Drittanbieters, das Sie als kreatives Asset mit den erforderlichen [Anzeigen DSP Tracking-Makros](/help/dsp/campaign-management/macros.md) gegebenenfalls eingefügt.

**[!UICONTROL Wmode]:** (Einige Anzeigentypen) Der Fenstermodus: *[!UICONTROL window]*, *[!UICONTROL transparent]* oder *[!UICONTROL opaque]*.

### [!UICONTROL Pixel]

Alle vorhandenen Ereignis-Tracking-Pixel für die Platzierung werden automatisch angehängt. Sie können vorhandene Pixel trennen und je nach Ihren Tracking-Anforderungen für die einzelne Anzeige neue Pixel erstellen.

Die folgenden Einstellungen gelten für jedes Pixel, das Sie erstellen oder bearbeiten.

**[!UICONTROL Integration Event]:** Das Ereignis, bei dem das Pixel Trigger wird, um ausgelöst zu werden. Verwenden Sie für diesen Anzeigentyp Pixel, die auf dem *[!UICONTROL Impression]* oder *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Gibt an, ob das Pixel ein *[!UICONTROL IMG URL]* (1x1-Pixel-Bilddatei), *[!UICONTROL HTML]* oder *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** Die URL des Pixelbilds in dem für die [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** Der Pixelname. Verwenden Sie einen Namen, mit dem Sie das Pixel leicht identifizieren können.

**[!UICONTROL Pixel Provider]:** Der Pixelanbieter: *[!UICONTROL None]*, *[!UICONTROL Nielsen]* oder *[!UICONTROL Comscore]*.

### [!UICONTROL Sharing]

Veraltet

>[!MORELIKETHIS]
>
>* [Über die Anzeigenverwaltung](ad-about.md)
>* [Einzelne Anzeige erstellen](ad-create.md)
>* [Platzierungen auflisten, die einer Anzeige zugeordnet sind](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Anzeigenspezifikationen](ad-specs.md)
>* [DSP Makros](/help/dsp/campaign-management/macros.md)

