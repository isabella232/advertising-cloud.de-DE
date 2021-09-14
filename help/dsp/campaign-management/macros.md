---
title: Advertising Cloud DSP Makros
description: Referenzieren Sie die verfügbaren Makros für das allgemeine Tracking und zur Verfolgung von Klicks auf Display-Anzeigen von Drittanbietern.
feature: Ads
exl-id: e31cc2e5-ad1f-4555-a87b-0e4c3731fe5f
source-git-commit: e0166dbad4fec41fdc64a65cb3a8ac97496c681f
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 0%

---

# Advertising Cloud DSP Makros

Ein Makro ist ein kurzer Befehl oder Kurzbefehl für eine Anweisung und folgt normalerweise dem Format `${MACRO_NAME}`. Der Advertising Cloud DSP-Anzeigenserver führt Makros aus, wenn die Anzeige bereitgestellt oder angeklickt wird.

Makros werden am häufigsten während des Handels mit kreativem Drittanbieter- und benutzerdefiniertem Code oder Metadaten (z. B. Pixeln von Drittanbietern) verwendet.

## Allgemeine Tracking-Makros

Verwenden Sie allgemeine Tracking-Makros für alle Anzeigen- und Tag-Typen, um bei Bedarf bestimmte Daten zurückzugeben.

| Makro | Beschreibung |
| --------------- | ---------------------- |
| `${USER_ID}` | Benutzer-ID für alle Gerätetypen. |
| `${TM_RANDOM}` | Cachebuster: eine Zufallszahl zwischen 1 und 100000 |
| `${TM_PLACEMENT_ID_NUM}` | Die Platzierungs-ID |
| `${TM_SITE_URL_URLENC}` | Die in der Angebotsanfrage übergebene URL; URL-kodiert |
| `${TM_SITE_DOMAIN_URLENC}` | Die von der URL in der Angebotsanforderung analysierte Seiten-Subdomäne; URL-kodiert |

{style=&quot;table-layout:auto&quot;}

## Klicken Sie auf Makros für Display-Anzeigen von Drittanbietern

Um Klicks für Anzeigen mithilfe von Display-Tags von Drittanbietern genau zu verfolgen, DSP ein Klick-Makro für die Anzeige erforderlich. Es ist nur eine Version des Makros erforderlich. das relevante Makro hängt vom Tag-Typ ab.

| Makro | Beschreibung |
| --------------- | ---------------------- |
| `${TM_CLICK_URL}` | Umleitungs-URL, die es Adservern ermöglicht, Anzeigenklicks in der Plattform zu verfolgen und zu zählen |
| `${TM_CLICK_URL_URLENC}` | Umleitungs-URL, die Adservern, die URL-Codierung benötigen, die Verfolgung und Zählung von Anzeigenklicks in der Plattform ermöglicht |

{style=&quot;table-layout:auto&quot;}

DSP fügt automatisch Klick-Makros in einem Display-Tag ein, wenn Sie:

* Exportieren von Anzeigen-Tags von einem Advertising Cloud-Adserver-Partner <!-- [Needs PM confirmation.] -->
* Massen-Upload von [!DNL Flashtalking]- oder [!DNL Google DoubleClick for Advertisers]-Anzeigen-Tags direkt in DSP

Wenn beim Erstellen einer Display-Anzeige ein Klickmakro fehlt, zeigt DSP eine Warnmeldung an, in der Sie aufgefordert werden, das entsprechende Display-Klickmakro manuell in den richtigen Bereich des Tags einzufügen.

>[!MORELIKETHIS]
>
>* [Audio-Anzeigeneinstellungen](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [Einstellungen für Connected TV-Anzeigen](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [Anzeigeeinstellungen](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [Einstellungen für mobile Anzeigen](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [Native Anzeigeneinstellungen](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [Pre-Roll-Anzeigeneinstellungen](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)

