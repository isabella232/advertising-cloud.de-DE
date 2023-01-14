---
title: Anzeigenspezifikationen
description: Verweisen Sie auf allgemeine und Publisher-spezifische Anzeigenspezifikationen.
feature: DSP Ads
exl-id: 905dfd9b-e7a3-4eb6-988f-b49d4b282dd2
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# Spezifikationen für unterstützte Anzeigentypen

## Videoanzeigen (Pre-Roll, CTV und universelle Videos)

### Unterstützte Bildschirme

Anzeigen werden standardmäßig auf Desktop-, Mobil- und vernetzten TV-Geräten bereitgestellt. Die Zielgruppenbestimmung für Geräte ist verfügbar, um die Bereitstellung anzupassen.

### Unterstützte Drittanbieter-Anzeigenserver

Sie können Tag-Arbeitsblätter aus [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid]und [!DNL Sizmek]. Eine vollständige Liste der unterstützten Anbieter finden Sie unter[Zertifizierte Ad Serving-Partner](certified-ad-servers.md).&quot;

### Anforderungen für hochauflösende Video-Assets (erforderlich)

**Video-Tag-Typ:** VPAID 2.0 JavaScript oder VAST (CTV). Alle VPAID-Anzeigeneinheiten müssen der [VPAID 2.0-Spezifikation](https://iabtechlab.com/wp-content/uploads/2016/04/VPAID_2_0_Final_04-10-2012.pdf) wie vom Interactive Advertising Bureau (IAB) definiert.

**Video-Codec:** MP4/H.264

**Auflösung:** 1280x720 für 720p, 1920x1080 für 1080p

**Bitrate:** 1500-2500 kBit/s für 720p, 2500-3500 kBit/s für 1080p

**H.264 Profil/Ebene:** hohes Profil, Stufe 3.1 für 720p; Hohes Profil, Stufe 4.0 für 1080p

**Video-Framerate:** 29.970 fps (allgemein als 30 fps bezeichnet) für NTSC-Länder, 25 fps für PAL-Länder, 23.976 fps (allgemein als 24 fps bezeichnet) für Film-Look-Inhalte

**Videofarbraum:** 4:2:0 YUV-Chroma-Subsampling

**Video Interlacing:** Progressives Scannen, d. h. nicht-interlaced. Keine Bewegung innerhalb des Felds (Mischrahmen) oder Zwischenzeilenanzeige.

**Führungskräfte (Split):** Unerlaubt

**Audio-Codec:** AAC-LC oder HE-AACv1

**Audio-Bitrate:** 128-192 kBit/s für AAC-LC, 64-128 kBit/s für HE-AACv1

**Audiokanal:** 2-Kanal-Stereo-Mix

**Audio-Beispielrate:** 44.1 kHz oder 48 kHz, bezogen auf das Ausgangsmaterial

**Audio-Ebenen:** 24 LKFS (+/- 2,0 dB) in den USA gemäß ATSC A/85; 23 LUFS (+/- 1,0) in der EU gemäß EBU R128

#### Zusätzliche Anforderungen an Publisher für vernetzte TV-Anzeigen

* **A+E-Netzwerk:** Siehe A+E-Netzwerke [Anzeigenspezifikationen](/help/dsp/assets/a-e-networks-tve-video-ad-specs.pdf)

* **Erkennung:** Siehe Erkennung [Anzeigenspezifikationen](/help/dsp/assets/discovery-networks-ad-specs.pdf).

* **Disney (einschl. Hulu):** Siehe Disney&#39;s [Anzeigenspezifikationen](https://hulu.disneyadsales.com/ad-products/video-commercial/).

* **HBO Max.:** Siehe HBO Max&#39;s [Anzeigenspezifikationen](/help/dsp/assets/hbo-max-ad-specs-2022.xlsx).

* **NBCUniversal:**

   * [Digitales Video](https://together.nbcuni.com/nbcu-creative-guidelines/digital-video/)

   * [Livestream](https://together.nbcuni.com/nbcu-creative-guidelines/livestream/)

   * [Pfau](https://together.nbcuni.com/nbcu-creative-guidelines/peacock/)

* **Paramount:** Siehe Paramount [Anzeigenspezifikationen](https://www.paramount.com/digital-ads).

## Display-Anzeigen

### Unterstützte Bildschirme

Anzeigen werden standardmäßig auf Desktop- und Mobilgeräten bereitgestellt. Die Zielgruppenbestimmung für Geräte ist verfügbar, um die Bereitstellung anzupassen.

### Unterstützte Dateitypen

**Bild:** GIF, JPG/JPEG, PNG

**HTML5:** Bilddateitypen: GIF, JPG/JPEG, PNG, SVG

### Anforderungen für Bild-Assets (erforderlich)

Universelle Anzeige wird unterstützt.

**Empfohlene Anzeigengrößen:** 120x60, 160x600, 180x150, 300x50, 300x100, 300x1050, 300x250, 300x60 0, 320x50, 320x480, 480x60, 640x480, 88x31, 728x90, 970x250, 970x90

**Unterstützte Drittanbieter-Anzeigenserver:** Sie können Tag-Arbeitsblätter aus [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid]und [!DNL Sizmek]. Eine vollständige Liste der unterstützten Anbieter finden Sie unter[Zertifizierte Ad Serving-Partner](certified-ad-servers.md).&quot;

## Audioanzeigen

### Unterstützte Bildschirme

Desktop, Mobilgerät, Tablet, Smart-Lautsprecher und vernetztes TV

### Unterstützte Drittanbieter-Anzeigenserver

Sie können Tag-Arbeitsblätter aus [!DNL DCM], [!DNL Flashtalking], [!DNL Innovid]und [!DNL Sizmek]. Eine vollständige Liste der unterstützten Anbieter finden Sie unter[Zertifizierte Ad Serving-Partner](certified-ad-servers.md).&quot;

### Anforderungen für Audio-Assets (erforderlich)

**Dateityp:** MP3, OGG, AAC

**Führungskräfte (Tonschiefer):**  Unerlaubt

**Maximale Dateigröße:** 2 MB

**Bitrate:** 128

**Dateilänge:** 0-60 s

#### Zusätzliche Anforderungen an Publisher

* **[!DNL iHeartRadio]**
   * Länge: 5, 15, 30 oder 60 Sekunden
   * Dateityp: MP3
   * Maximale Dateigröße: 320 kBit/s
   * Volumen: 44.1 kHz

* **[!DNL Pandora]**
   * Länge: 15 oder 30 Sekunden
   * Dateityp: MP4 (in-App), MP3 (Desktop)
   * Maximale Dateigröße: 2,2 MB

* **[!DNL SoundCloud]**
   * Länge: 6, 15 oder 30 Sekunden
   * Dateityp: MP3
   * Maximale Dateigröße: 5 MB

* **[!DNL Spotify]**
   * Länge: Bis zu 30 Sekunden
   * Dateityp: OGG
   * Maximale Dateigröße: 500 MB
   * Volumen: RMS normalisiert auf -14; dBFS-Spitzenwert normalisiert auf -0,2 dBFS

* **[!DNL TargetSpot]**
   * Länge: 15, 30 oder 60 Sekunden
   * Dateityp: MP3

* **[!DNL TuneIn]**
   * Länge: 10, 15 oder 30 Sekunden
   * Dateityp: MP3, OGG
   * Volumen: 44.1 kHz

### Anforderungen für begleitende Banneranzeigen (optional)

**Unterstützte Größen:** 300x250, 500x500, 640x640, 1024x1024

#### Zusätzliche Anforderungen an Publisher

* **[!DNL iHeartRadio]:**
   * Dateityp: JPEG, JPG, PNG, GIF, SWF, HTML
   * Maximale Dateigröße: 2,2 MB
   * Dimensionen: 300 x 250

* **[!DNL Pandora]:**
   * Dateityp: JPEG, GIF
   * Maximale Dateigröße: Größe: 100 KB
   * Dimensionen: 300 x 250 (Mobil oder Desktop) oder 500 x 500 (Desktop)

* **[!DNL SoundCloud]:**
   * Dateityp: Statische JPG, PNG
   * Maximale Dateigröße: Unter 400 KB
   * Dimensionen: 1024 x 1024

* **[!DNL Spotify]:**
   * Dateityp: Statische JPG, PNG
   * Maximale Dateigröße: 200 KB
   * Dimensionen: 300 x 250

* **[!DNL TuneIn]:**
   * Dateityp: JPEG, JPG, PNG, GIF, HTML
   * Maximale Dateigröße: 2 MB
   * Dimensionen: 300 x 250
 

## Native Display-Anzeigen

Jede Anzeige kann entweder ein Standbild oder ein bewegliches GIF (Kinemagramm) enthalten.

### Unterstützte Bildschirme

Anzeigen werden standardmäßig auf Desktop- und Mobilgeräten bereitgestellt. Die Zielgruppenbestimmung für Geräte ist verfügbar, um die Bereitstellung anzupassen.

### Erforderliche Assets für alle nativen In-Feed-Formate

#### Bild-Asset

**Auflösung:** Mindestens 600 x 600 px; Empfohlenes Minimum von 1200x627px

**Dateityp:** JPEG (Bild- oder Videoanzeigenabbild), GIF (Cinemograph)

**Dateigröße:** Weniger als 1 MB (Bild sollte frei von Text sein.)

#### Advertiser-Logo

**Auflösung:** Mindestens 80 x 80 px; Empfohlenes Minimum von 300x300px

**Dateityp:** JPEG oder PNG.

**Seitenverhältnis:**  1x1 Verhältnis

>[!NOTE]
>
>Je nachdem, über welchem Bild es überlagert wird, können Sie zwischen hellen oder dunklen Logoelementen wählen.

#### Text/Kopieren

**Überschrift:** Maximal 200 Zeichen; 25 Zeichen empfohlen

**Beschriftung:** Maximal 200 Zeichen; 100 Zeichen empfohlen

**Sponsored by:** Maximal 200 Zeichen; 30 Zeichen empfohlen

**Aktionsaufruf (nur MoPub):** Maximal 15 Zeichen

>[!NOTE]
>
>Das endgültige Layout wird vom Publisher zur Laufzeit definiert. Wenn eine Anzeige die empfohlene Zeichenanzahl überschreitet, dürfen einige Inventaranbieter die Anzeige möglicherweise nicht bereitstellen, oder der Herausgeber oder SSP kann den Text abschneiden.

#### Landingpage-URL

Die Clickthrough-URL mit optionalen Klicktrackern.

Anforderungen an Klick-Tracker:

* Impression-Tracking-Pixel von Drittanbietern: Nur 1x1-Bild-URL-Format

* JavaScript-Tracking zur Sichtbarkeit: Nur für IAS unterstützt; Nur 1x1-Bilder im JS.append-Format

* Clicktracking-Pixel von Drittanbietern: Muss zu der in die URL eingebetteten Landingpage weiterleiten (HTTP 302-Umleitung)

* Klick-Tracker mit Data Management Platform (DMP) mit 200 oder mehr Antworten werden nicht unterstützt.

>[!MORELIKETHIS]
>
>* [Über die Anzeigenverwaltung](ad-about.md)
>* [Einzelne Anzeige erstellen](ad-create.md)
>* [Erstellen mehrerer Drittanbieteranzeigen](ad-create-multiple.md)
>* [Eine Anzeige bearbeiten](ad-edit.md)

