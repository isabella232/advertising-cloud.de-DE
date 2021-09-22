---
title: Anzeigeeinstellungen
description: Siehe Beschreibungen der verfügbaren Anzeigeneinstellungen für Display-Anzeigen.
feature: DSP Ads
exl-id: ae88dfab-0b0c-42ab-9135-422b20a4b6cd
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# Anzeigeeinstellungen

Die folgenden Einstellungen gelten für standardmäßige Display-Anzeigen. Sie können auch Clickthrough-Videoanzeigen für Display-Anzeigen bereitstellen. Wir empfehlen jedoch nicht, dies zu tun, da diese von nicht vielen Herausgebern unterstützt werden.

## [!UICONTROL Ad Options]

### Allgemein

**[!UICONTROL Ad Type]:**  (Schreibgeschützt) Der Anzeigentyp, den Sie erstellen, der dem Platzierungstyp entspricht, an den die Anzeige angehängt werden kann. Der Standardwert ist *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** Der Anzeigenname. Der Asset-Titel wird standardmäßig verwendet, Sie können jedoch den Namen ändern.

>[!TIP]
>
> Verwenden Sie einen Namen, der leicht zu finden ist, wenn Sie die Anzeige an eine Platzierung, in der [!UICONTROL Ads]-Ansicht und in Berichten anhängen. Beschreiben Sie beispielsweise den Einheitentyp und einige wichtige Attribute (z. B. die Holiday-Produktvorschau: 300x250 Gamer&quot;).

**\[Anzeigenquelle\]**: Ob Advertising Cloud DSP die Anzeige bereitstellt (*[!UICONTROL Adobe served]*) oder einen Werbeserver eines Drittanbieters (*[!UICONTROL 3rd party]*) verwendet.

**[!UICONTROL This is an expandable Banner]:**  (Nur Werbeanzeigen von Drittanbietern) Gibt an, dass es sich bei der Anzeige um eine erweiterbare Banneranzeige handelt. Die zugehörigen Erweiterungsparameter bestimmen, welcher Bestand gekauft werden soll. Stellen Sie daher sicher, dass er das Anzeigenverhalten widerspiegelt.

**[!UICONTROL Expansion Method]:**  (Nur erweiterbare Banneranzeigen von Drittanbietern) Gibt an, ob das Banner bei  *[!UICONTROL Click]* oder  *[!UICONTROL Rollover]* erweitert wird.

**[!UICONTROL Expansion Directions]:**  (Nur erweiterbare Banner-Anzeigen von Drittanbietern) Die Richtung, in der sich die Anzeige erweitert:  *[!UICONTROL Up]*,  *[!UICONTROL Down]*,  *[!UICONTROL Left]* oder  *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:**  (Nur erweiterbare Banneranzeigen von Drittanbietern) Der zertifizierte Anbieter, für den die Anzeige verfügbar ist:  *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]),  *[!UICONTROL Flashtalking]*,  *[!UICONTROL Sizmek]* oder  *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:**  (Nur Werbeanzeigen von Drittanbietern) Die URL des kreativen Drittanbieter-Assets. Alle Parameter [timestamp] und [[timestamp]] werden durch tatsächliche Werte ersetzt.

**[!UICONTROL Final Display Code]:**  (Nur Werbeanzeigen von Drittanbietern) Die URL für das kreative Asset von Drittanbietern mit den erforderlichen  [Advertising Cloud DSP-Tracking-](/help/dsp/campaign-management/macros.md) Makros, sofern zutreffend.

**[!UICONTROL Creative type]:**  (Nur von Adobe bereitgestellte Anzeigen) Gibt an, ob es sich bei dem Asset um ein  *[!UICONTROL Image]* oder ein  *[!UICONTROL HTML5]* Asset handelt.

**[!UICONTROL Asset]|  [!UICONTROL HTML5 Asset]:**  (Nur für Adobe bereitgestellte Anzeigen) Eine Bilddatei oder ein komprimiertes HTML5-Asset, das hochgeladen werden soll, je nach kreativem Typ. Klicken Sie auf **[!UICONTROL Browse]** und suchen Sie die Datei auf Ihrem Gerät oder Netzwerk und klicken Sie dann auf **[!UICONTROL Upload]** oder **[!UICONTROL Upload Image]**.

**[!UICONTROL Ad Size]:** Die Breite und Höhe der Anzeige. Dabei muss es sich um eine [unterstützte standardmäßige Anzeigegröße](/help/dsp/assets/ad-specs.pdf) handeln. Sie können die Anzeigengröße manuell eingeben, bevor Sie die Anzeige hochladen, oder einen [!UICONTROL Display Code] eingeben. Wenn Sie die Anzeigengröße nicht eingeben, werden die Dimensionen der hochgeladenen Anzeige oder des Anzeigen-Tags automatisch als schreibgeschützt eingegeben. Beachten Sie, dass die Display-Anzeige nicht gespeichert wird, wenn die Abmessungen nicht der Standardanzeige in der Größe entsprechen - z. B. 301x250 anstelle der Anzeigengröße 300x250.

>[!IMPORTANT]
>
> Die in den Feldern Breite und Höhe deklarierte Anzeigengröße wird mit den eingehenden Angebotsanfragen abgeglichen. Möglicherweise treten Versandprobleme auf, wenn die Dimensionen der Anzeige nicht mit der deklarierten Anzeigengröße übereinstimmen.

**[!UICONTROL Click URL]:**  (Nur von Adobe bereitgestellte Anzeigen) Die URL, auf die der Viewer landet, wenn er auf die Anzeige klickt.

**[!UICONTROL Final Click URL]:**  (nur von der Adobe bereitgestellte Anzeigen; schreibgeschützt) Die  [!UICONTROL Click URL] mit den erforderlichen  [Advertising Cloud DSP-Tracking-](/help/dsp/campaign-management/macros.md) Makros, sofern zutreffend.

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
>* [Platzierungen auflisten, die einer Anzeige zugeordnet sind](ad-list-placements.md)
>* [Verfügbare Anzeigentypen](ad-types.md)
>* [Anzeigenspezifikationen](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSP Makros](/help/dsp/campaign-management/macros.md)

