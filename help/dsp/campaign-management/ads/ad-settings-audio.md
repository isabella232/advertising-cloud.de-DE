---
title: Audio-Anzeigeneinstellungen
description: Siehe Beschreibungen der verfügbaren Anzeigeneinstellungen für Audioanzeigen.
feature: DSP Ads
exl-id: 746b6f40-ff59-4bbe-bfc0-3579d4461e4a
source-git-commit: e0713f3717a684fb5ef2808d7de769424b8972d2
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 0%

---

# Audio-Anzeigeneinstellungen

## [!UICONTROL Upload or Select Creative]

*Nur neue Anzeigen*

**[!UICONTROL Upload Audio]:** So laden Sie ein unverarbeitetes Asset in DSP hoch. Gehen Sie bei Auswahl dieser Option wie folgt vor:

1. Klicken **[!UICONTROL Choose File]** und suchen Sie die Datei auf Ihrem Gerät oder Netzwerk.
1. Geben Sie einen Titel für die Datei ein, der im [!UICONTROL Ads] Anzeigen und Berichten.
1. Klicken **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** So wählen Sie alle zuvor hochgeladenen Kreativelemente im richtigen Format innerhalb des Kontos aus.

**[!UICONTROL Advanced: VAST Tag URL]:** So geben Sie ein VAST-Tag eines Drittanbieters ein, das kreative Assets und Tracking-Pixel enthält:

1. Klicken ![Pfeil](/help/dsp/assets/compressed.png) neben **[!UICONTROL Advanced: VAST Tag URL]**.
1. Im **[!UICONTROL URL]** Geben Sie die VAST-Tag-URL ein.
1. Geben Sie einen **[!UICONTROL Title]** für die Datei, die in der [!UICONTROL Ads] Anzeigen und Berichten.

>[!TIP]
>
> Um die Gültigkeit eines VAST-Tags zu überprüfen, fügen Sie es in einen Browser ein und drücken Sie die **[!UICONTROL Enter]** Schlüssel. Wenn das Tag gültig ist, wird eine XML-Datei angezeigt, die Folgendes enthält: `<VAST>` oben.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:** (Schreibgeschützt) Der Anzeigentyp, den Sie erstellen. Er entspricht dem Platzierungstyp, an den die Anzeige angehängt werden kann. Die Standardeinstellung ist *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** Der Anzeigenname. Der Asset-Titel wird standardmäßig verwendet, Sie können jedoch den Namen ändern.

>[!TIP]
>
> Verwenden Sie einen Namen, der leicht zu finden ist, wenn Sie die Anzeige an eine Platzierung anhängen, in der [!UICONTROL Ads] und in Berichten anzeigen. Beschreiben Sie beispielsweise den Einheitentyp und einige wichtige Attribute (z. B. die Holiday-Produktvorschau: 30 Sek. Audio&quot;).

**[!UICONTROL Ad Duration]:** Die Länge der Audiodatei. Sie wird automatisch als [!UICONTROL 15] oder [!UICONTROL 30], abhängig von der ausgewählten Anzeigeneinheit.

Je nach den Kontoberechtigungen kann dieses Feld angezeigt werden.

**[!UICONTROL Click URL]:** (Anzeigen, die Rohdaten und Anzeigen verwenden, die nur Anzeigebanner enthalten; optional) Die URL, auf die der Viewer gelangt, wenn er auf ein Anzeigenbanner klickt, das Ihre Anzeige begleitet.

**[!UICONTROL Final Click URL]:** (Anzeigen, die Rohdaten und Anzeigen verwenden, die nur Anzeigebanner enthalten; schreibgeschützt) Die [!UICONTROL Click URL] mit den erforderlichen [Advertising Cloud DSP-Tracking-Makros](/help/dsp/campaign-management/macros.md) gegebenenfalls eingefügt.

**[!UICONTROL VAST Tag]:** (Anzeigen, die nur VAST-Tags verwenden) Eine URL für eine Anzeigenquelle eines Drittanbieters. Stellen Sie sicher, dass das VAST-Tag nur Audiomediendateien enthält.

**[!UICONTROL Final VAST Tag]:** (Anzeigen, die nur VAST-Tags verwenden) Die URL für die Anzeigenquelle eines Drittanbieters mit den erforderlichen [Advertising Cloud DSP-Tracking-Makros](/help/dsp/campaign-management/macros.md) gegebenenfalls eingefügt.

**[!UICONTROL Select Rate]:** (Nur Benutzer mit Berechtigung) Ein vorab ausgehandelter Preis, der über die Adobe in Rechnung gestellt wird, oder einer der Tarife, die Sie ausgehandelt haben und für die Sie vom Anbieter in Rechnung gestellt werden. Wenden Sie sich an Ihren [!DNL Adobe] Kundenbetreuer.

### [!UICONTROL Companion]

*Nur DSP-Anzeigen*

Sie können optional bis zu drei begleitende Banner mit einer Anzeige anhängen. Die Best Practice besteht darin, nach Möglichkeit begleitende Banner anzuhängen.

>[!NOTE]
>
>* Nicht alle Herausgeber lassen begleitende Banner zu. Die Herausgeber, die begleitende Banner zulassen, garantieren keine begleitenden Bannerimpressionen.
>* Begleitbanner von Anzeigen-Tags von Drittanbietern stehen möglicherweise nicht immer für die Vorschau zur Verfügung.


**\[Kontrollkästchen\]:** Enthält das angegebene begleitende Banner in die Anzeige. Wenn das Kontrollkästchen deaktiviert ist, ist das begleitende Banner nicht enthalten.

**\[Bannergröße\]:** Die Größe des begleitenden Banners: *[!UICONTROL 300x250]* (verwendet für [!DNL iHeartRadio], [!DNL Spotify], [!DNL SoundCloud]und [!DNL TuneIn]), *[!UICONTROL 640x640]* (verwendet für [!DNL Spotify), or *1024x1024]* (verwendet für [!DNL SoundCloud]).

**\[Quelle\]:** Die Quelle des begleitenden Banner-Assets:

* *[!UICONTROL Upload My Own Asset]:* Hochladen Ihres eigenen Assets.
* *[!UICONTROL Use a Third Party Tag]:* So geben Sie ein iFrame- oder Skript-Tag von einem zertifizierten Drittanbieter-Adserving-Partner ein.

Verwenden Sie ein Drittanbieter-Tag, wenn Sie begleitende Bannerimpressionen von Drittanbietern verfolgen möchten.

**[!UICONTROL Asset]:** (Nur Rohdaten) Das begleitende Banner-Asset im Format GIF, JPG oder PNG. Klicken **[!UICONTROL Browse]** und suchen Sie die Datei auf Ihrem Gerät oder Netzwerk und klicken Sie auf **[!UICONTROL Upload]**.

**[!UICONTROL Click URL]:** (Nur Rohdaten) Die URL, auf die der Viewer landet, wenn er auf das begleitende Banner für die Anzeige klickt. Sie kann eine Klick-Umleitung mit einem Klick-Tracking-Pixel eines Drittanbieters enthalten.

**[!UICONTROL Final Click URL]:** (Nur Rohstoffe; schreibgeschützt) Die Klick-URL mit der erforderlichen [Advertising Cloud DSP-Tracking-Makros](/help/dsp/campaign-management/macros.md) gegebenenfalls eingefügt.

**[!UICONTROL Ad Tag]:** (Anzeigen, die nur Werbe-Tags von Drittanbietern verwenden) Ein iFrame- oder Skriptbanner-Tag für eine Drittanbieter-Bannerquelle. Sie muss von einem zertifizierten Drittanbieter-Adserving-Partner stammen.

**[!UICONTROL Final Ad Tag]:** (Anzeigen, die nur Werbe-Tags von Drittanbietern verwenden) Das Anzeigen-Tag mit den erforderlichen [Advertising Cloud DSP-Tracking-Makros](/help/dsp/campaign-management/macros.md) gegebenenfalls eingefügt.

### Pixel

Alle vorhandenen Ereignis-Tracking-Pixel für die Platzierung werden automatisch angehängt. Sie können vorhandene Pixel trennen und je nach Ihren Tracking-Anforderungen bei Bedarf neue Pixel erstellen.

Die folgenden Einstellungen gelten für jedes Pixel, das Sie erstellen oder bearbeiten.

**[!UICONTROL Integration Event]:** Das Ereignis, bei dem das Pixel Trigger wird, um ausgelöst zu werden. Verwenden Sie für diesen Anzeigentyp Pixel, die auf dem *[!UICONTROL Impression]* oder *[!UICONTROL Click-through]*.

**[!UICONTROL Pixel Type]:** Gibt an, ob das Pixel ein *[!UICONTROL IMG UR]L* (1x1-Pixel-Bilddatei), *[!UICONTROL HTML]* oder *[!UICONTROL JavaScript URL]*.

**[!UICONTROL Pixel URL or Code]:** Die URL des Pixelbilds im entsprechenden Format für den angegebenen Pixeltyp.

**[!UICONTROL Pixel Name]:** Der Pixelname. Verwenden Sie einen Namen, mit dem Sie das Pixel leicht identifizieren können.

**[!UICONTROL Pixel Provider]:** Der Pixelanbieter: *[!UICONTROL None]*, *[!UICONTROL Nielsen]* oder *[!UICONTROL Comscore]*.

>[!MORELIKETHIS]
>
>* [Über die Anzeigenverwaltung](ad-about.md)
>* [Erstellen einer Anzeige](ad-create.md)
>* [Platzierungen auflisten, die einer Anzeige zugeordnet sind](/help/dsp/campaign-management/ads/ad-list-placements.md)
>* [Verfügbare Anzeigentypen](ad-types.md)
>* [Anzeigenspezifikationen](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSP Makros](/help/dsp/campaign-management/macros.md)

