---
title: Einstellungen für Connected TV-Anzeigen
description: Siehe Beschreibungen der verfügbaren Anzeigeneinstellungen für verbundene TV-Anzeigen.
feature: Ads
exl-id: 4daae9e4-27eb-4496-9186-f33aebd8daae
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '605'
ht-degree: 0%

---

# Einstellungen für Connected TV-Anzeigen

## [!UICONTROL Upload or Select Creative]

*Nur neue Anzeigen*

**[!UICONTROL Upload Audio]:** Um ein Rohdaten-Asset in DSP hochzuladen. Gehen Sie bei Auswahl dieser Option wie folgt vor:

1. Klicken Sie auf **[!UICONTROL Choose File]** und suchen Sie die Datei auf Ihrem Gerät oder Netzwerk.
1. Geben Sie einen Titel für die Datei ein, der in der [!UICONTROL Ads]-Ansicht und den Berichten verwendet wird.
1. Klicken **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** So wählen Sie alle zuvor hochgeladenen Kreativelemente im richtigen Format innerhalb des Kontos aus.

**[!UICONTROL Advanced: VAST Tag URL]:**  (Einige Anzeigentypen) So geben Sie ein VAST-Tag eines Drittanbieters ein, das kreative Assets und Tracking-Pixel enthält:

1. Klicken Sie auf ![Pfeil](/help/dsp/assets/compressed.png) neben **[!UICONTROL Advanced: VAST Tag URL]**.
1. Geben Sie im Feld **[!UICONTROL URL]** die VAST-Tag-URL ein.
1. Geben Sie **[!UICONTROL Title]** für die Datei ein, die in der Anzeigen-Ansicht und in den Berichten verwendet wird.

>[!TIP]
>
> Um die Gültigkeit eines VAST-Tags zu überprüfen, fügen Sie es in einen Browser ein und drücken Sie die Taste **[!UICONTROL Enter]** . Wenn das Tag gültig ist, wird oben eine XML-Datei mit `<VAST>` angezeigt.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:**  (Schreibgeschützt) Der Anzeigentyp, den Sie erstellen, der dem Platzierungstyp entspricht, an den die Anzeige angehängt werden kann.

**[!UICONTROL Ad Name]:** Der Anzeigenname. Der Asset-Titel wird standardmäßig verwendet, Sie können jedoch den Namen ändern.

>[!TIP]
>
> Verwenden Sie einen Namen, der leicht zu finden ist, wenn Sie die Anzeige an eine Platzierung, in der [!UICONTROL Ads]-Ansicht und in Berichten anhängen. Beschreiben Sie beispielsweise den Einheitentyp und einige wichtige Attribute (z. B. die Holiday-Produktvorschau: 30 Sek. CTV&quot;).

**[!UICONTROL Width | Ad Unit Width]:** Die Breite der gesamten Werbeeinheit. Diese Option kann je nach ausgewähltem Anzeigentyp gesperrt werden.

**[!UICONTROL Height | Ad Unit Height]:** Die Höhe der gesamten Anzeigeneinheit. Diese Option kann je nach ausgewähltem Anzeigentyp gesperrt werden.

**[!UICONTROL Player X]:** Die X-Koordinate für die Anzeigeneinheit. Behalten Sie die Standardeinstellung bei.

**[!UICONTROL Player Y]:** Die Y-Koordinate für die Anzeigeneinheit. Behalten Sie die Standardeinstellung bei.

**[!UICONTROL Player Width]:** Die Breite der gesamten Werbeeinheit. Diese Option kann je nach ausgewähltem Anzeigentyp gesperrt werden.

Dies entspricht dem Feld **[!UICONTROL Width]** .

**[!UICONTROL Player Height]:** Die Höhe der gesamten Anzeigeneinheit. Diese Option kann je nach ausgewähltem Anzeigentyp gesperrt werden.

Dies entspricht dem Feld **[!UICONTROL Height]** .

**[!UICONTROL Show Controls]:** So fügen Sie Videosteuerelemente für die Anzeige hinzu:  *[!UICONTROL Under]*,  *[!UICONTROL Over]*,  *[!UICONTROL Bottom]* oder  *[!UICONTROL None]* (Standardeinstellung).

**[!UICONTROL Preserve Aspect Ratio]:** Gibt an, ob die Breite und Höhe des Videos beibehalten (*[!UICONTROL Yes]*) oder das Video gestreckt werden soll, um den verfügbaren Platz zu füllen (*[!UICONTROL No]*).

**[!UICONTROL Click URL]:**  (Nur von Adobe bereitgestellte Anzeigen) Die URL, auf die der Viewer landet, wenn er auf die Anzeige klickt.

**[!UICONTROL Final Click URL]:**  (nur von der Adobe bereitgestellte Anzeigen; schreibgeschützt) Die  [!UICONTROL Click URL] mit den erforderlichen  [Advertising Cloud DSP-Tracking-](/help/dsp/campaign-management/macros.md) Makros, sofern zutreffend.

**[!UICONTROL VAST Tag]:**  (Anzeigen, die nur VAST-Tags verwenden; schreibgeschützt) Das VAST-Tag des Drittanbieters, das Sie als Anzeigenquelle eingegeben haben.

**[!UICONTROL Final VAST Tag]:**  (Anzeigen, die nur VAST-Tags verwenden; schreibgeschützt) Das VAST-Tag des Drittanbieters, das Sie als Anzeigenquelle mit den erforderlichen  [Advertising Cloud DSP-Tracking-](/help/dsp/campaign-management/macros.md) Makros eingegeben haben, sofern zutreffend.

**[!UICONTROL Clock Number]**: (nur im Vereinigten Königreich verwendet; nur für Benutzer mit Berechtigung verfügbar) Eine eindeutige ID, mit der sichergestellt wird, dass die richtige Anzeige gesendet wird. Wenn diese Einstellung nicht anwendbar ist, lassen Sie sie leer.

### [!UICONTROL Pixel]

Alle vorhandenen Ereignis-Tracking-Pixel für die Platzierung werden automatisch angehängt. Sie können vorhandene Pixel trennen und je nach Ihren Tracking-Anforderungen bei Bedarf neue Pixel erstellen.

Die folgenden Einstellungen gelten für jedes Pixel, das Sie erstellen oder bearbeiten.

**[!UICONTROL Integration Event]:** Das Ereignis, bei dem das Pixel Trigger wird, um ausgelöst zu werden. Verwenden Sie für diesen Anzeigentyp Pixel, die auf *[!UICONTROL Impression]* oder *[!UICONTROL Click-through]* ausgelöst werden.

**[!UICONTROL Pixel Type]:** Gibt an, ob das Pixel eine  *[!UICONTROL IMG URL]* (1x1-Pixelbilddatei),  *[!UICONTROL HTML]* oder  *[!UICONTROL JavaScript URL]* ist.

**[!UICONTROL Pixel URL or Code]:** Die URL des Pixelbilds im entsprechenden Format für den angegebenen Pixeltyp.

**[!UICONTROL Pixel Name]:** Der Pixelname. Verwenden Sie einen Namen, mit dem Sie das Pixel leicht identifizieren können.

**[!UICONTROL Pixel Provider]:** Der Pixelanbieter:  *[!UICONTROL None]*,  *[!UICONTROL Nielsen]* oder  *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Über die Anzeigenverwaltung](ad-about.md)
>* [Erstellen einer Anzeige](ad-create.md)
>* [Platzierungen auflisten, die einer Anzeige zugeordnet sind](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Verfügbare Anzeigentypen](ad-types.md)
>* [Anzeigenspezifikationen](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSP Makros](/help/dsp/campaign-management/macros.md)

