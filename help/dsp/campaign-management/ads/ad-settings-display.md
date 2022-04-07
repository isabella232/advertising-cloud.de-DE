---
title: Anzeigeeinstellungen
description: Siehe Beschreibungen der verfügbaren Anzeigeneinstellungen für Display-Anzeigen.
feature: DSP Ads
exl-id: ae88dfab-0b0c-42ab-9135-422b20a4b6cd
source-git-commit: 68af6b1846a37689dce0ca13a05cc1611b1f35a9
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---

# Anzeigeeinstellungen

Die folgenden Einstellungen gelten für standardmäßige Display-Anzeigen.

## [!UICONTROL Ad Options]

### Allgemein

**[!UICONTROL Ad Type]:** (Schreibgeschützt) Der Anzeigentyp, den Sie erstellen. Er entspricht dem Platzierungstyp, an den die Anzeige angehängt werden kann. Die Standardeinstellung ist *[!UICONTROL Display]*.

**[!UICONTROL Ad Name]:** Der Anzeigenname. Der Asset-Titel wird standardmäßig verwendet, Sie können jedoch den Namen ändern.

>[!TIP]
>
> Verwenden Sie einen Namen, der leicht zu finden ist, wenn Sie die Anzeige an eine Platzierung anhängen, in der [!UICONTROL Ads] und in Berichten anzeigen. Beschreiben Sie beispielsweise den Einheitentyp und einige wichtige Attribute (z. B. die Holiday-Produktvorschau: 300x250 Gamer&quot;).

**\[Anzeigenquelle\]**: (schreibgeschützt) *[!UICONTROL 3rd party]*.

**[!UICONTROL This is an expandable Banner]:** (Nur Werbeanzeigen von Drittanbietern) Gibt an, dass es sich bei der Anzeige um eine erweiterbare Banneranzeige handelt. Die zugehörigen Erweiterungsparameter bestimmen, welcher Bestand gekauft werden soll. Stellen Sie daher sicher, dass er das Anzeigenverhalten widerspiegelt.

**[!UICONTROL Expansion Method]:** (Nur erweiterbare Banneranzeigen von Drittanbietern) Gibt an, ob das Banner sich um *[!UICONTROL Click]* oder *[!UICONTROL Rollover]*.

**[!UICONTROL Expansion Directions]:** (Nur erweiterbare Banneranzeigen von Drittanbietern) Die Richtung, in der die Anzeige erweitert: *[!UICONTROL Up]*, *[!UICONTROL Down]*, *[!UICONTROL Left]* oder *[!UICONTROL Right]*.

**[!UICONTROL Certified Vendors]:** (Nur erweiterbare Banneranzeigen von Drittanbietern) Der zertifizierte Anbieter, für den die Anzeige verfügbar ist: *[!UICONTROL DCM]* ([!DNL Google DoubleClick for Advertisers]), *[!UICONTROL Flashtalking]*, *[!UICONTROL Sizmek]* oder *[!UICONTROL Jivox]*.

**[!UICONTROL Display Code]:** (Nur Werbeanzeigen von Drittanbietern) Die URL des kreativen Drittanbieter-Assets. Alle [timestamp] und [[timestamp]] -Parameter durch tatsächliche Werte ersetzt.

**[!UICONTROL Final Display Code]:** (Nur Werbeanzeigen von Drittanbietern) Die URL für das kreative Asset von Drittanbietern mit den erforderlichen [Advertising Cloud DSP-Tracking-Makros](/help/dsp/campaign-management/macros.md) gegebenenfalls eingefügt.

**[!UICONTROL Ad Size]:** Die Breite und Höhe der Anzeige. Es muss ein [Unterstützte standardmäßige Anzeigeanzeigengröße](/help/dsp/assets/ad-specs.pdf). Sie können die Anzeigengröße manuell eingeben, bevor Sie die Anzeige hochladen, oder eine [!UICONTROL Display Code]. Wenn Sie die Anzeigengröße nicht eingeben, werden die Dimensionen der hochgeladenen Anzeige oder des Anzeigen-Tags automatisch als schreibgeschützt eingegeben. Beachten Sie, dass die Display-Anzeige nicht gespeichert wird, wenn die Abmessungen nicht der Standardanzeige in der Größe entsprechen - z. B. 301x250 anstelle der Anzeigengröße 300x250.

>[!IMPORTANT]
>
> Die in den Feldern Breite und Höhe deklarierte Anzeigengröße wird mit den eingehenden Angebotsanfragen abgeglichen. Möglicherweise treten Versandprobleme auf, wenn die Dimensionen der Anzeige nicht mit der deklarierten Anzeigengröße übereinstimmen.

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
>* [Platzierungen auflisten, die einer Anzeige zugeordnet sind](ad-list-placements.md)
>* [Anzeigenspezifikationen](/help/dsp/assets/ad-specs.pdf)
>* [Advertising Cloud DSP Makros](/help/dsp/campaign-management/macros.md)

