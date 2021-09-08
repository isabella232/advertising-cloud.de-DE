---
title: Audio-Anzeigeneinstellungen
description: Siehe Beschreibungen der verfügbaren Anzeigeneinstellungen für Audioanzeigen.
feature: Ads
exl-id: 746b6f40-ff59-4bbe-bfc0-3579d4461e4a
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 0%

---

# Audio-Anzeigeneinstellungen

## [!UICONTROL Upload or Select Creative]

*Nur neue Anzeigen*

**[!UICONTROL Upload Audio]:** Um ein Rohdaten-Asset in DSP hochzuladen. Gehen Sie bei Auswahl dieser Option wie folgt vor:

1. Klicken Sie auf **[!UICONTROL Choose File]** und suchen Sie die Datei auf Ihrem Gerät oder Netzwerk.
1. Geben Sie einen Titel für die Datei ein, der in der [!UICONTROL Ads]-Ansicht und den Berichten verwendet wird.
1. Klicken **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** So wählen Sie alle zuvor hochgeladenen Kreativelemente im richtigen Format innerhalb des Kontos aus.

**[!UICONTROL Advanced: VAST Tag URL]:** So geben Sie ein VAST-Tag eines Drittanbieters ein, das kreative Assets und Tracking-Pixel enthält:

1. Klicken Sie auf ![Pfeil](/help/dsp/assets/compressed.png) neben **[!UICONTROL Advanced: VAST Tag URL]**.
1. Geben Sie im Feld **[!UICONTROL URL]** die VAST-Tag-URL ein.
1. Geben Sie einen **[!UICONTROL Title]** für die Datei ein, der in der [!UICONTROL Ads]-Ansicht und den Berichten verwendet wird.

>[!TIP]
>
> Um die Gültigkeit eines VAST-Tags zu überprüfen, fügen Sie es in einen Browser ein und drücken Sie die Taste **[!UICONTROL Enter]** . Wenn das Tag gültig ist, wird oben eine XML-Datei mit `<VAST>` angezeigt.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:**  (Schreibgeschützt) Der Anzeigentyp, den Sie erstellen, der dem Platzierungstyp entspricht, an den die Anzeige angehängt werden kann. Der Standardwert ist *[!UICONTROL Audio]*.

**[!UICONTROL Ad Name]:** Der Anzeigenname. Der Asset-Titel wird standardmäßig verwendet, Sie können jedoch den Namen ändern.

>[!TIP]
>
> Verwenden Sie einen Namen, der leicht zu finden ist, wenn Sie die Anzeige an eine Platzierung, in der [!UICONTROL Ads]-Ansicht und in Berichten anhängen. Beschreiben Sie beispielsweise den Einheitentyp und einige wichtige Attribute (z. B. die Holiday-Produktvorschau: 30 Sek. Audio&quot;).

**[!UICONTROL Ad Duration]:** Die Länge der Audiodatei. Er wird je nach ausgewählter Anzeigeneinheit automatisch entweder auf [!UICONTROL 15] oder auf [!UICONTROL 30] gesetzt.

Je nach den Kontoberechtigungen kann dieses Feld angezeigt werden.

**[!UICONTROL Click URL]:**  (Anzeigen, die Rohdaten und nur Anzeigebanner verwenden; optional) Die URL, auf die der Viewer gelangt, wenn er auf ein Anzeigenbanner klickt, das Ihre Anzeige begleitet.

**[!UICONTROL Final Click URL]:**  (Anzeigen, die Rohdaten und nur Anzeigebanner verwenden; schreibgeschützt) Die  [!UICONTROL Click URL] mit den erforderlichen  [Advertising Cloud DSP-Tracking-](/help/dsp/campaign-management/macros.md) Makros, sofern zutreffend.

**[!UICONTROL VAST Tag]:**  (Anzeigen, die nur VAST-Tags verwenden) Eine URL für eine Anzeigenquelle eines Drittanbieters. Stellen Sie sicher, dass das VAST-Tag nur Audiomediendateien enthält.

**[!UICONTROL Final VAST Tag]:**  (Anzeigen, die nur VAST-Tags verwenden) Die URL für die Drittanbieter-Anzeigenquelle mit den erforderlichen  [Advertising Cloud DSP-Tracking-](/help/dsp/campaign-management/macros.md) Makros, sofern zutreffend.

**[!UICONTROL Select Rate]:** (Nur Benutzer mit Berechtigung) Ein vorab ausgehandelter Preis, der über die Adobe in Rechnung gestellt wird, oder einer der Tarife, die Sie ausgehandelt haben und für die vom Anbieter in Rechnung gestellt wird. Wenden Sie sich zum Hinzufügen einer Adobe an Ihren Kundenbetreuer.

### [!UICONTROL Companion]

*Nur DSP-Anzeigen*

Sie können optional bis zu drei begleitende Banner mit einer Anzeige anhängen. Die Best Practice besteht darin, nach Möglichkeit begleitende Banner anzuhängen.

>[!NOTE]
>
>* Nicht alle Herausgeber lassen begleitende Banner zu. Die Herausgeber, die begleitende Banner zulassen, garantieren keine begleitenden Bannerimpressionen.
>* Begleitbanner von Anzeigen-Tags von Drittanbietern stehen möglicherweise nicht immer für die Vorschau zur Verfügung.


**\[Kontrollkästchen\]:** Enthält das angegebene begleitende Banner mit der Anzeige. Wenn das Kontrollkästchen deaktiviert ist, ist das begleitende Banner nicht enthalten.

**\[Bannergröße\]:**  Die Größe des begleitenden Banners:  *[!UICONTROL 300x250]* (verwendet für  [!DNL iHeartRadio],  [!DNL Spotify],  [!DNL SoundCloud] und  [!DNL TuneIn]),  *[!UICONTROL 640x640]* (verwendet für  [!DNL Spotify), or *1024x1024]* (verwendet für  [!DNL SoundCloud]).

**\[Quelle\]:** Die Quelle des begleitenden Banner-Assets:

* *[!UICONTROL Upload My Own Asset]:* Um Ihr eigenes Asset hochzuladen.
* *[!UICONTROL Use a Third Party Tag]:* Um ein iFrame- oder Skript-Tag von einem zertifizierten Drittanbieter-Adserving-Partner einzugeben.

Verwenden Sie ein Drittanbieter-Tag, wenn Sie begleitende Bannerimpressionen von Drittanbietern verfolgen möchten.

**[!UICONTROL Asset]:**  (Nur Rohdaten) Das begleitende Banner-Asset im Format GIF, JPG oder PNG. Klicken Sie auf **[!UICONTROL Browse]**, suchen Sie die Datei auf Ihrem Gerät oder Netzwerk und klicken Sie dann auf **[!UICONTROL Upload]**.

**[!UICONTROL Click URL]:**  (Nur Rohdaten) Die URL, auf die der Viewer landet, wenn er auf das begleitende Banner für die Anzeige klickt. Sie kann eine Klick-Umleitung mit einem Klick-Tracking-Pixel eines Drittanbieters enthalten.

**[!UICONTROL Final Click URL]:**  (Nur Rohwerte; schreibgeschützt) Die Klick-URL mit den erforderlichen  [Advertising Cloud DSP-Tracking-](/help/dsp/campaign-management/macros.md) Makros, falls zutreffend.

**[!UICONTROL Ad Tag]:**  (Anzeigen, die nur Werbe-Tags von Drittanbietern verwenden) Ein iFrame- oder Skriptbanner-Tag für eine Drittanbieter-Bannerquelle. Sie muss von einem zertifizierten Drittanbieter-Adserving-Partner stammen.

**[!UICONTROL Final Ad Tag]:**  (Anzeigen, die nur Werbe-Tags von Drittanbietern verwenden) Das Anzeigen-Tag mit den erforderlichen  [Advertising Cloud DSP-Tracking-](/help/dsp/campaign-management/macros.md) Makros, sofern zutreffend.

### Pixel

Alle vorhandenen Ereignis-Tracking-Pixel für die Platzierung werden automatisch angehängt. Sie können vorhandene Pixel trennen und je nach Ihren Tracking-Anforderungen bei Bedarf neue Pixel erstellen.

Die folgenden Einstellungen gelten für jedes Pixel, das Sie erstellen oder bearbeiten.

**[!UICONTROL Integration Event]:** Das Ereignis, bei dem das Pixel Trigger wird, um ausgelöst zu werden. Verwenden Sie für diesen Anzeigentyp Pixel, die auf *[!UICONTROL Impression]* oder *[!UICONTROL Click-through]* ausgelöst werden.

**[!UICONTROL Pixel Type]:** Gibt an, ob das Pixel eine  *[!UICONTROL IMG UR]L* -Bilddatei (1x1-Pixelbilddatei),  *[!UICONTROL HTML]* oder  *[!UICONTROL JavaScript URL]* ist.

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

