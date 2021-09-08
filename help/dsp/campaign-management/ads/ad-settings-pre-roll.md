---
title: Pre-Roll-Anzeigeneinstellungen
description: Siehe Beschreibungen der verfügbaren Anzeigeneinstellungen für Pre-Roll-Anzeigen.
feature: Ads
exl-id: 638d5a3d-3dff-40b6-a3ba-7ab3f08282b9
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '1211'
ht-degree: 0%

---

# Pre-Roll-Anzeigeneinstellungen

## [!UICONTROL Upload or Select Creative]

*Nur neue Anzeigen*

**[!UICONTROL Transcode to]:** (Einige Benutzer, abhängig von den Berechtigungen; (optional) Die Formate, die Sie in Ihr VAST-Tag aufnehmen möchten, wenn der Herausgeber bestimmte Anforderungen an kreative Dateien hat. Von den meisten Herausgebern akzeptierte Formate sind standardmäßig ausgewählt.

**[!UICONTROL Custom Transcode]:**  (nur Beta-Benutzer; nicht verfügbar, wenn Vertikales Video ausgewählt ist) Gibt an, dass das Video benutzerdefinierte Transkodierung verwendet. Wenn Sie diese Option auswählen, geben Sie das Dateiformat, die Video-Bitrate, den Zoom und die Abmessungen für bis zu drei benutzerdefinierte Transkodierungsversionen an.

**[!UICONTROL XTrader]:**  (Einige Benutzer, je nach Berechtigungen) Gibt an, dass das Video einen oder mehrere  [!DNL X_TRADER] Feeds verwendet.

**[!UICONTROL Upload Video]:** Um ein Rohdaten-Asset in DSP hochzuladen. Gehen Sie bei Auswahl dieser Option wie folgt vor:

1. Klicken Sie auf **[!UICONTROL Choose File]** und suchen Sie die Datei auf Ihrem Gerät oder Netzwerk.
1. Geben Sie einen Titel für die Datei ein, der in der [!UICONTROL Ads]-Ansicht und den Berichten verwendet wird.
1. Klicken **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Video]:** So wählen Sie alle zuvor hochgeladenen Kreativelemente im richtigen Format innerhalb des Kontos aus.

**[!UICONTROL Advanced: VAST Tag URL]:**  (Einige Anzeigentypen) So geben Sie ein VAST-Tag eines Drittanbieters ein, das kreative Assets und Tracking-Pixel enthält:

1. Klicken Sie auf ![Pfeil](/help/dsp/assets/compressed.png) neben **[!UICONTROL Advanced: VAST Tag URL]**.
1. Geben Sie im Feld **[!UICONTROL URL]** die VAST-Tag-URL ein.
1. Geben Sie einen **[!UICONTROL Title]** für die Datei ein, der in der [!UICONTROL Ads]-Ansicht und den Berichten verwendet wird.

>[!TIP]
>
> Um die Gültigkeit eines VAST-Tags zu überprüfen, fügen Sie es in einen Browser ein und drücken Sie die Taste **[!UICONTROL Enter]** . Wenn das Tag gültig ist, wird oben eine XML-Datei mit `<VAST>` angezeigt.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:**  (Schreibgeschützt) Der Anzeigentyp, den Sie erstellen, der dem Platzierungstyp entspricht, an den die Anzeige angehängt werden kann.

**[!UICONTROL Ad Name]:** Der Anzeigenname. Der Asset-Titel wird standardmäßig verwendet, Sie können jedoch den Namen ändern.

>[!TIP]
>
> Verwenden Sie einen Namen, der leicht zu finden ist, wenn Sie die Anzeige an eine Platzierung, in der [!UICONTROL Ads]-Ansicht und in Berichten anhängen. Beschreiben Sie beispielsweise den Einheitentyp und einige wichtige Attribute (z. B. die Holiday-Produktvorschau: 30 Sek. Preroll&quot;).

**[!UICONTROL Width]|  [!UICONTROL Ad Unit Width]:**  (Nur Standard- und übersprungene Pre-Roll-Anzeigen) Die Breite der gesamten Anzeigeneinheit. Diese Option kann je nach ausgewähltem Anzeigentyp gesperrt werden.

**[!UICONTROL Height]|  [!UICONTROL Ad Unit Height]:**  (Nur standardmäßige und übersprungene Pre-Roll-Anzeigen) Die Höhe der gesamten Anzeigeneinheit. Diese Option kann je nach ausgewähltem Anzeigentyp gesperrt werden.

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

**[!UICONTROL Wmode]:**  (Nur interaktive Pre-Roll) Der Fenstermodus:  *[!UICONTROL window]*,  *[!UICONTROL transparent]* oder  *[!UICONTROL opaque]*.

**[!UICONTROL Video Format]:**  (Nur interaktive Pre-Roll) Das Format des Anzeigen-Players für potenziellen Bestand:  *[!UICONTROL VPAID]* oder  *[!UICONTROL VPAID & VAST]*. Die Sichtbarkeit wird immer für VPAID gemessen, VPAID und VAST enthalten jedoch Bestände, die keine Sichtbarkeitsmessung zulassen. Beachten Sie dies, wenn Sichtbarkeitsmetriken für Ihre Kampagne wichtig sind.

**[!UICONTROL Clock Number]**: (Nur interaktive Pre-Roll-Daten; nur im Vereinigten Königreich verwendet werden; nur für Benutzer mit Berechtigung verfügbar) Eine eindeutige ID, mit der sichergestellt wird, dass die richtige Anzeige gesendet wird. Wenn diese Einstellung nicht anwendbar ist, lassen Sie sie leer.

### [!UICONTROL Companion]

*Nur DSP-Anzeigen*

Sie können optional bis zu drei begleitende Banner mit einer Anzeige anhängen. Die Best Practice besteht darin, nach Möglichkeit begleitende Banner anzuhängen.

>[!NOTE]
>
> Nicht alle Herausgeber lassen begleitende Banner zu. Die Herausgeber, die begleitende Banner zulassen, garantieren keine begleitenden Bannerimpressionen.
> Begleitbanner von Anzeigen-Tags von Drittanbietern stehen möglicherweise nicht immer für die Vorschau zur Verfügung.

**\[Kontrollkästchen\]:** Enthält das angegebene begleitende Banner mit der Anzeige. Wenn das Kontrollkästchen deaktiviert ist, ist das begleitende Banner nicht enthalten.

**\[Bannergröße\]:**  Die Größe des begleitenden Banners:  *[!UICONTROL 300x600 (Skyscraper)]*;  *[!UICONTROL 300x250 (Medium Rectangle)]*, was die häufigste Anzeigengröße ist und für alle Anzeigen empfohlen wird;  *[!UICONTROL 300x60 (Small Banner)]*; oder  *[!UICONTROL 728x90 (Leaderboard)]*, was eine weniger häufig verwendete Anzeigengröße ist.

**\[Quelle\]:** Gibt an, ob Sie Ihr eigenes begleitendes Banner-Asset hochladen oder ein Drittanbieter-Tag verwenden.

**Asset:**  (Nur Rohdaten) Das begleitende Banner-Asset. Klicken Sie auf **[!UICONTROL Browse]**, suchen Sie die Datei auf Ihrem Gerät oder Netzwerk und klicken Sie dann auf **[!UICONTROL Upload]**.

**Anzeigen-Tag]:[!UICONTROL ** (Anzeigen, die nur VAST-Tags verwenden) Eine URL zu einer Drittanbieter-Bannerquelle.

**[!UICONTROL Final Ad Tag]:**  (Anzeigen, die nur VAST-Tags verwenden) Eine URL zu einer Drittanbieter-Bannerquelle mit den erforderlichen  [Advertising Cloud DSP-Tracking-](/help/dsp/campaign-management/macros.md) Makros, sofern zutreffend.

### [!UICONTROL Overlays]

*Interaktive Formate für Pre-Roll und mobile interaktive und &quot;Tippen-zu-Wiedergabe&quot;für DSP Anzeigen*

Die folgenden Einstellungen gelten für jede Überlagerung, die Sie erstellen oder bearbeiten.

**[!UICONTROL Asset]:**  (Nur Rohdaten) Das Bild-Asset der Überlagerung. Die Datei muss im Einzelbild-GIF-, JPG- oder PNG-Format vorliegen und die maximale Bildgröße beträgt weniger als 2 MB. Um das Asset hochzuladen, klicken Sie auf **[!UICONTROL Browse]**, suchen Sie die Datei auf Ihrem Gerät oder Netzwerk und klicken Sie dann auf **[!UICONTROL Upload]**.

>[!TIP]
>
>Siehe [Best Practices zum Erstellen von Überlagerungen](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)

**[!UICONTROL Click URL]:**  Die URL, auf die der Viewer gelangt, wenn er auf eine Überlagerung für Ihre Anzeige klickt.

**[!UICONTROL X]:** Die X-Koordinate für die Überlagerung. Wählen Sie die Startposition der Überlagerung aus und geben Sie dann die Anzahl der Pixel von der Startposition ein (z. B. 10 Pixel von der Mitte). Die Best Practice ist, *From Center* zu verwenden, wodurch verhindert wird, dass sich die Überlagerung mit verschiedenen Player-Größen auf Publisher-Sites bewegt.

**[!UICONTROL Y]:** Die Y-Koordinate für die Überlagerung. Wählen Sie die Startposition der Überlagerung aus und geben Sie dann die Anzahl der Pixel von der Startposition ein (z. B. 10 Pixel von oben). Als Best Practice wird empfohlen, je nach Position, an der die Überlagerung auf der Anzeige angezeigt werden soll, eine Koordinate *[!UICONTROL From Bottom]* oder *[!UICONTROL From Top],* anzugeben.

**[!UICONTROL Layer]:** Die Ebene, in der die Überlagerung angezeigt wird. Das Video und jede Überlagerung werden in separaten Ebenen dargestellt.

* *[!UICONTROL 2 through 5]:* Vor dem Video, aber hinter anderen Überlagerungen.

* *[!UICONTROL 1]:* Vor dem Video.

* *[!UICONTROL 0]:* Auf derselben Ebene wie das Video. Das Video wird verkleinert, um den verbleibenden Platz auszufüllen. Für interaktive Vorbereitung nicht empfohlen.

* *[!UICONTROL -1]:* Hinter dem Video.

* *[!UICONTROL -2 through -5]:* Hinter dem Video, aber vor anderen Überlagerungen.

* *[!UICONTROL Background]:* Hinter dem Video und anderen Überlagerungen. Die Überlagerung skaliert auf die volle Breite und Höhe des Videos, und das Seitenverhältnis wird nicht beibehalten.

### [!UICONTROL Pixel]

Alle vorhandenen Ereignis-Tracking-Pixel für die Platzierung werden automatisch angehängt. Sie können vorhandene Pixel trennen und je nach Ihren Tracking-Anforderungen bei Bedarf neue Pixel erstellen.

Die folgenden Einstellungen gelten für jedes Pixel, das Sie erstellen oder bearbeiten.

**[!UICONTROL Integration Event]:** Das Ereignis, bei dem das Pixel Trigger wird, um ausgelöst zu werden. Verwenden Sie für diesen Anzeigentyp Pixel, die auf *[!UICONTROL Impression]* oder *[!UICONTROL Click-through]* ausgelöst werden.

**[!UICONTROL Pixel Type]:** Gibt an, ob das Pixel eine  *[!UICONTROL IMG URL]* (1x1-Pixelbilddatei),  *[!UICONTROL HTML]* oder  *[!UICONTROL JavaScript URL]* ist.

**[!UICONTROL Pixel URL or Code]:** Die URL des Pixelbilds im entsprechenden Format für das angegebene  [!UICONTROL Pixel Type].

**[!UICONTROL Pixel Name]:** Der Pixelname. Verwenden Sie einen Namen, mit dem Sie das Pixel leicht identifizieren können.

**[!UICONTROL Pixel Provider]:** Der Pixelanbieter:  *[!UICONTROL None]*,  *[!UICONTROL Nielsen]* oder  *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Über die Anzeigenverwaltung](ad-about.md)
>* [Erstellen einer Anzeige](ad-create.md)
>* [Platzierungen auflisten, die einer Anzeige zugeordnet sind](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Verfügbare Anzeigentypen](ad-types.md)
>* [Anzeigenspezifikationen](/help/dsp/assets/ad-specs.pdf)
>* [Best Practices zum Entwerfen von Überlagerungen](/help/dsp/campaign-management/ads/ad-best-practices-overlays.md)
>* [Advertising Cloud DSP Makros](/help/dsp/campaign-management/macros.md)

