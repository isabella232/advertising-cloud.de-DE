---
title: Markensicherheit und Medienqualität
description: Erfahren Sie mehr über Markensicherheit und Medienqualitätsmerkmale.
feature: DSP Introduction
exl-id: df5be5d4-490e-479f-b76d-4fda4acd4201
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '1315'
ht-degree: 0%

---

# Markensicherheit und Medienqualität

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising Cloud DSP bietet eine Reihe von Markenschutzfunktionen, um sicherzustellen, dass jede Ihrer Kampagnen echte Benutzer in einer markensicheren Umgebung erreicht.

Unser Team zur Überwachung von Betrugsfällen arbeitet eng mit branchenführenden Partnern wie dem [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)]und [!DNL WhiteOps], um den Bestand auf unserer Plattform sorgfältig zu kuratieren. Durch die proaktive Verwaltung unseres Angebots stellt DSP sicher, dass alle Advertiser auf der ganzen Plattform vor unmenschlichem Traffic (Bots, Crawler, Data Center Traffic und Betrug) geschützt sind und nur in markensicheren Kontexten bereitstellen.

Neben dem zentralen Qualitätsmanagement möchten wir Werbetreibende in die Lage versetzen, die ihrer Marke entsprechenden Steuerelemente zu entwerfen. Adobe Advertising Cloud bietet Integrationen mit [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], [!DNL Oracle Data Cloud]und [!DNL Peer39], sodass jeder Werbetreibende sein gewünschtes Maß an Betrugsschutz, kontextbezogener Filterung und Keyword-Targeting wählen kann.

## Advertising Cloud DSP-Qualitätsinitiativen

### Inventarüberprüfung mit [!DNL Ads.txt] Support

[[!DNL Ads.txt], der für [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) ist eine Initiative, die von der [!DNL Interactive Advertising Bureau] ([!DNL IAB]) im Juni 2017, um die ordnungsgemäße Darstellung des Bestands auf dem offenen Markt zu erleichtern und damit illegale Quellen des Datenverkehrs und der Domain-Spoofing zu bekämpfen. Beteiligte Verlage und Händler erklären öffentlich die Unternehmen, die zum Verkauf ihres digitalen Bestands zugelassen sind, und die Art dieser Beziehungen, indem sie eine `ads.txt` auf der obersten Ebene der Domäne (z. B. `example.com/ads.txt`).

DSP unterstützt [!DNL ads.txt] durch Lesen der `ads.txt` -Datei erstellen und Ihnen die Möglichkeit geben, nur bei verifizierter Person zu kaufen [!DNL ads.txt] Verkäufer. Wenn wir beispielsweise die Verkäufer abgleichen, können wir auf `nytimes.com` an die New York Times&#39; `ads.txt` -Datei, können wir identifizieren, welche legitim sind und welche nicht, und wir blockieren die Täter, wenn die Platzierung so konfiguriert ist, dass sie nur bei verifizierten Verkäufern kaufen. <!-- can we actually mention NY Times? -->

Sie können die Standardeinstellung [!DNL ads.txt] Steuerelemente für jeden Advertiser<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->und dann optional [Anpassen der Einstellungen für jede Platzierung](/help/dsp/campaign-management/placements/placement-settings.md) an:

* Inventar nur von autorisierten Direktverkäufern einer Domain kaufen

* Inventar nur von autorisierten Direktverkäufern und Wiederverkäufern einer Domain kaufen

* Kaufbestand von autorisierten Direktverkäufern und Wiederverkäufern einer Domain priorisieren

* Inventar von allen Verkäufern kaufen

### Überwachung von Platform-Betrug

DSP verfügt über leistungsstarke interne Tools und Systeme, mit denen Betrug auf unserer gesamten Plattform in Zusammenarbeit mit führenden Branchenanbietern wie [!DNL Whiteops] und [!DNL Integral Ad Science].

Darüber hinaus arbeitet Adobe eng mit [!DNL IAB] und [!DNL TAG] Sicherstellung einer robusten und branchenüblichen Betrugsblockierung zum Schutz unserer Werbetreibende durch Nutzung von Tools wie [!DNL ads.txt] (siehe vorherigen Abschnitt), wird die [!DNL IAB] Liste &quot;Bots and Spiders&quot;und die [!DNL TAG] IP-Liste des Datenzentrums.

Durch unseren mehrdimensionalen Qualitätsansatz überwacht unser Team Anomalien und ungültige Traffic-Muster und sorgt so für weniger als 3 % ungültigen Traffic im geschützten Inventar. Alle Bestände, die verdächtig sind - einschließlich Inventar auf bestimmten Domänen oder von bestimmten Herausgebern oder Verkäufern - werden sofort auf der gesamten Plattform blockiert.

### Inventarzuordnung, -unterteilung und -kategorisierung

Die Bestandszuordnung ist der detaillierte Überprüfungs- und Onboarding-Prozess, der für alle neuen Bestände erforderlich ist, bevor er zu unserer Plattform hinzugefügt wird. Dieser Prozess soll die Sicherheit und Qualität des gesamten Bestands auf DSP gewährleisten.

* **Zuordnung:** Unser Inventarteam überprüft jede Domäne sorgfältig, wobei Aspekte wie:

   * Markensicherheit

   * Verifizierung des Anzeigentyps

   * Allgemeine Inhalte, doppelte Domänen und gefälschte Adserving

* **Tiering:** Wir untersuchen ganzheitlich die Markenpräsenz im gesamten Ökosystem, um Inventare über verschiedene Ebenen hinweg zu klassifizieren. Sie können [Targeting Ihrer Platzierungen](/help/dsp/campaign-management/placements/placement-settings.md) auf diese Ebenen für die gewünschte Reichweite:

   * **[!UICONTROL T1]** - Markennamen, international anerkannte Sites

   * **[!UICONTROL T2]** - Optimale Sites, die aktuell und aktuell sind, ohne benutzergenerierten Inhalt und in der Regel nicht global erkannt werden

   * **[!UICONTROL T3]** - Benutzergenerierte Inhalte und Nischeninhalte

* **Site-Kategorisierung:** Um einfaches Content-Targeting und -Blockieren zu gewährleisten, taggen wir jede Eigenschaft mit einer Advertising Cloud-definierten Site-Kategorie, die auf dem Eigenschaftsinhalt basiert. Sie können [diese Site-Kategorien für jede Platzierung als Ziel auswählen oder ausschließen](/help/dsp/campaign-management/placements/placement-settings.md) basierend auf den Platzierungszielen.

### Umfassende Unterstützung für Site-Blocking

Advertising Cloud DSP bietet sowohl eine global gesperrte Siteliste als auch die Möglichkeit, benutzerdefinierte Blockierungslisten für Advertiser und Konten zu erstellen.

#### Advertising Cloud DSP - Liste global blockierter Sites {#global-blocked-sites}

Advertising Cloud DSP verwaltet eine global gesperrte Site-Liste von Sites, die für unsicher erachtet werden, um Anzeigen auf diesen zu starten. Diese Liste enthält Websites mit verwerflichen Inhalten (z. B. Hass oder Terror) und von Bots infizierten Websites, gefälschten Pre-Roll-Dateien, nicht übereinstimmenden Domänen und anderen betrügerischen Aktivitäten.

Im Rahmen unserer Initiative zur Markensicherheit, um Aktivitäten auszurotten, die Werbetreibende betrügen, werden alle Sites anhand der in der Liste der blockierten Sites der Grafik aufgeführten Maßnahmen überprüft. Alle Sites, die die Markensicherheitsprüfungen nicht bestehen, werden der Liste der global blockierten Sites hinzugefügt. Da Advertising Cloud DSP diese Liste dynamisch verwaltet, können Sites auf der Grundlage der neuesten Analyse der Markensicherheit jederzeit aus der Liste wechseln.

Wenn Sie eine Site in die Liste der global blockierten Sites als Platzierungsziel einschließen, wird die Site mit einem roten Ausrufezeichen (!) gekennzeichnet. Dies bedeutet, dass Anzeigen nicht auf der gekennzeichneten Site ausgeführt werden.

#### Blockierte Sites auf Kontoebene und Advertiser-Ebene

Benutzer können auch Listen auf Kontoebene und auf Advertiser-Ebene blockierte Sites verwalten<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->, die automatisch für alle Platzierungen verwendet werden. Die Liste der blockierten Sites der unteren Ebene wird zusätzlich zur Liste der global blockierten Sites angewendet.

## Drittanbieterintegrationen

### Kontextuelle Filterung

Mit kontextuellen Filtern können Sie Anzeigenangebote basierend auf dem Kontext der Seite, auf der die Anzeige bereitgestellt wird, gezielt ausrichten oder blockieren. Adobe bietet kontextbezogene Filterung über Integrationen mit führenden Anbietern in der Branche: [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]und [!DNL Peer39]. Beispiele für aktuelle Filter sind [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics]und [!UICONTROL G-rated Sites].

Sie können für jeden Advertiser standardmäßige Steuerelemente für kontextbezogene Filter festlegen<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->und dann optional [Anpassen der Einstellungen für jede Platzierung](/help/dsp/campaign-management/placements/placement-settings.md). Wenn Sie diese Funktion verwenden, fallen möglicherweise zusätzliche Gebühren an.

![Comscore-Logo](/help/dsp/assets/comscore-logo.png) ![DoubleVerify-Logo](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science-Logo](/help/dsp/assets/ias-logo.png) ![Peer39-Logo](/help/dsp/assets/peer39-logo.png)

### Blockierung von Betrugsvorgängen

Nutzen Sie unsere Drittanbieterintegrationen mit [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]und [!DNL Peer39] , um nicht-menschlichen Traffic in Ihren Kampagnen zu blockieren. Diese Integrationen bieten branchenführende Pre-Bid-Blockierungsfunktionen, mit denen Sie den allgemeinen und komplexen ungültigen Traffic (GIVT und SIVT) in Ihren Kampagnen minimieren können.

Sie können für jeden Advertiser standardmäßige Pre-Bid-Betrug-Kontrollen einrichten<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) -->und dann optional [Anpassen der Einstellungen für jede Platzierung](/help/dsp/campaign-management/placements/placement-settings.md). Wenn Sie diese Funktion verwenden, fallen möglicherweise zusätzliche Gebühren an.

Weitere Informationen zur Funktionalität erhalten Sie von Ihrem bevorzugten Anbieter direkt oder bei Ihrem [!DNL Adobe] Account-Team.

![Comscore-Logo](/help/dsp/assets/comscore-logo.png) ![DoubleVerify-Logo](/help/dsp/assets/doubleverify-logo.png) ![Integral Ad Science-Logo](/help/dsp/assets/ias-logo.png) ![Peer39-Logo](/help/dsp/assets/peer39-logo.png)

### Pre-Bid-Sichtbarkeit {#pre-bid-viewability}

Vorab-Sichtbarkeitsfilter, die von unseren branchenführenden Partnern unterstützt werden [!DNL DoubleVerify], [!DNL Oracle Advertising] ([!DNL Moat]) und [!DNL Integral Ad Science] Werbetreibenden die Möglichkeit zu bieten, sicherzustellen, dass ihre Kampagnen die gewünschten Ziele der Sichtbarkeit der Leistung im Video- und Display-Inventar erreichen.

Sie können für jeden Advertiser standardmäßige Sichtbarkeitsfilter festlegen<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) -->und dann optional [Anpassen der Einstellungen für jede Platzierung](/help/dsp/campaign-management/placements/placement-settings.md). Wenn Sie diese Funktion verwenden, fallen möglicherweise zusätzliche Gebühren an.

![DoubleVerify-Logo](/help/dsp/assets/doubleverify-logo.png) ![Oracle Advertising-Logo](/help/dsp/assets/oracle-advertising-logo.png) ![Integral Ad Science-Logo](/help/dsp/assets/ias-logo.png)

### Themen-Targeting

DSP Thema-Targeting ermöglicht es Ihnen, mithilfe unserer branchenführenden kontextbezogenen Partner Suchbegrifflisten als Ziel festzulegen oder zu blockieren. [!DNL Comscore] und [!DNL Oracle Data Cloud] ([!DNL Grapeshot]). Das Thema-Targeting hilft Ihnen dabei sicherzustellen, dass Ihre Anzeigen immer in einer mit Ihrer Marke abgestimmten Umgebung bereitgestellt werden, unabhängig davon, ob dies das Blockieren schädlicher Inhalte oder die Sicherstellung von Ausgaben in einem Kontext umfasst, der ein höheres Ergebnis gewährleistet.

Für das Thema-Targeting müssen Sie benutzerdefinierte Themensegmente direkt mit [!DNL Comscore] oder [!DNL Grapeshot] (mithilfe von [!DNL Oracle Data Cloud]). Sobald diese in der Partnerplattform erstellt wurden, können Sie [Segment-ID in der [!UICONTROL Audience Targeting] für jede Platzierung](/help/dsp/campaign-management/placements/placement-settings.md). Für diese Funktion können zusätzliche Gebühren anfallen.

So erstellen Sie benutzerdefinierte Themensegmente:

* So erstellen Sie eine [!DNL Comscore] Konto erstellen und benutzerdefinierte Segmente erstellen, können Sie eine Anmeldung für [!DNL Activation Segment Manager] at [https://agents.comscore.com](https://agents.comscore.com). Siehe [[!DNL Comscore] Hilfezentrum](https://comscoreactivation.zendesk.com/hc/) für vollständige Anweisungen zum Einrichten benutzerdefinierter Segmente. Gebühren für benutzerdefinierte Segmente sind in [!DNL Segment Manager] während der Erstellung.

* Erste Schritte mit [!DNL Oracle Data Cloud], Kontakt [!DNL Oracle Data Cloud] oder [!DNL Adobe] Account-Team.

![Comscore-Logo](/help/dsp/assets/comscore-logo.png) ![Graustufen-Logo](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP hat eine Partnerschaft mit [!DNL DoubleVerify] um [!DNL Authentic Brand Safety] Targeting-Lösung, mit der Sie eine zentrale Gruppe von Anforderungen an die Markensicherheit erstellen können, um auf all Ihren Bestellplattformen Konsistenz zu erreichen.

Sobald Sie eine [!DNL DoubleVerify] Markensegment Sicherheit mit dem erforderlichen Targeting verwenden, können Sie es in DSP verwenden, um Ihre Blockregeln nach dem Gebot in allen Webumgebungen mit dem Pre-Gebot zu replizieren.

Sie können eine [!DNL DoubleVerify] Segment-ID für jeden Advertiser<!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) -->und dann optional [aktivieren oder deaktivieren [!UICONTROL Authentic Brand Safety] für jede Platzierung](/help/dsp/campaign-management/placements/placement-settings.md). DSP stellt Ihr Konto für die Verwendung der Segment-ID in Rechnung.

Weitere Informationen zur Funktion erhalten Sie bei [!DNL DoubleVerify] direkt oder kontaktieren Sie Ihre [!DNL Adobe] Account-Team.

![DoubleVerify-Logo](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)

<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
