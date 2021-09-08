---
title: Native Anzeigeneinstellungen
description: Siehe Beschreibungen der verfügbaren Anzeigeneinstellungen für native Anzeigen.
feature: Ads
exl-id: 3ae59e63-ae64-41b2-8734-3df2da020c7c
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Native Anzeigeneinstellungen

## [!UICONTROL Upload or Select Creative]

*Nur neue Videoanzeigen (aber keine Anzeigen)*

**[!UICONTROL Upload Audio]:** Um ein Rohdaten-Asset in DSP hochzuladen. Gehen Sie bei Auswahl dieser Option wie folgt vor:

1. Klicken Sie auf **[!UICONTROL Choose File]** und suchen Sie die Datei auf Ihrem Gerät oder Netzwerk.
1. Geben Sie einen Titel für die Datei ein, der in der [!UICONTROL Ads]-Ansicht und den Berichten verwendet wird.
1. Klicken **[!UICONTROL Upload]**.

**[!UICONTROL Use Existing Audio]:** So wählen Sie alle zuvor hochgeladenen Kreativelemente im richtigen Format innerhalb des Kontos aus.

## [!UICONTROL Ad Options]

### [!UICONTROL Basic]

**[!UICONTROL Ad Type]:**  (Schreibgeschützt) Der Anzeigentyp, den Sie erstellen, der dem Platzierungstyp entspricht, an den die Anzeige angehängt werden kann.

**[!UICONTROL Ad Name]:** Der Anzeigenname. Der Anzeigentyp (nativ anzeigen) oder Videotitel (Videoformate) wird standardmäßig verwendet, Sie können den Namen jedoch ändern.

>[!TIP]
>
> Verwenden Sie einen Namen, der leicht zu finden ist, wenn Sie die Anzeige an eine Platzierung, in der [!UICONTROL Ads]-Ansicht und in Berichten anhängen. Beschreiben Sie beispielsweise den Einheitentyp und einige wichtige Attribute (z. B. die Holiday-Produktvorschau: 15sec Native&quot;).

**[!UICONTROL Native Creative]:** Ein Bild mit 1200 x 627 Pixel, um die Bereitstellung auf mobilen Beständen zu maximieren. Bei Videoanzeigen ist dies das Bild, das vor der Wiedergabe des nativen Videos angezeigt wird. Klicken Sie auf **[!UICONTROL Browse]**, suchen Sie die Datei auf Ihrem Gerät oder Netzwerk und klicken Sie dann auf **[!UICONTROL Upload]**.

**[!UICONTROL Title]:** Ein auffälliger Titel, der Zuschauer anspricht.

**[!UICONTROL Description]:** Bei Videoanzeigen ist dies eine kurze Zusammenfassung der Anzeige. Bei Display-Anzeigen ist dies der Hauptteil der Anzeige. Die maximale Länge beträgt 100 Zeichen.

**[!UICONTROL Landing Page]:** Die URL, auf die der Viewer gelangt, wenn er auf die Anzeige klickt.

**[!UICONTROL Final Landing Page]:** Die  [!UICONTROL Landing Page] URL mit den erforderlichen  [Advertising Cloud DSP-Tracking-](/help/dsp/campaign-management/macros.md) Makros, falls zutreffend.

**[!UICONTROL Sponsored By (Advertiser Name)]:** Der Advertiser für die Anzeige.

**[!UICONTROL Call to Action]:** (Optional) Der Schritt, den Viewer ausführen sollen, sobald sie diese Anzeige sehen.

**[!UICONTROL Advertiser Logo]:**  (Optional) Ein 1:1-Ratio-Logo, das in die Anzeige aufgenommen wird, um die Markenerkennung zu verbessern. Klicken Sie auf **[!UICONTROL Browse]**, suchen Sie die Datei auf Ihrem Gerät oder Netzwerk und klicken Sie dann auf **[!UICONTROL Upload]**.

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
>* [Advertising Cloud DSP Makros](/help/dsp/campaign-management/macros.md)

