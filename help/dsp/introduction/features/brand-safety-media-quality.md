---
title: Markensicherheit und Medienqualität
description: Erfahren Sie mehr über Markensicherheit und Medienqualitätsmerkmale.
feature: Introduction
exl-id: df5be5d4-490e-479f-b76d-4fda4acd4201
source-git-commit: e2ee41c7e3e195f062ad1cc67080ed913d6d3d06
workflow-type: tm+mt
source-wordcount: '1266'
ht-degree: 0%

---

# Markensicherheit und Medienqualität

<!-- Check on logo sizes in staging environment -- I made them all 100 pixels high except for DoubleVerify, which is 150 (harder to see at 100), but some instances look larger in VS Code. -->

Advertising Cloud DSP bietet eine Reihe von Markenschutzfunktionen, um sicherzustellen, dass jede Ihrer Kampagnen echte Benutzer in einer markensicheren Umgebung erreicht.

Unser Team von Fraud Surveillance arbeitet eng mit branchenführenden Partnern wie den [!DNL Interactive Advertising Bureau], [!DNL Trust and Accountability Group] [!DNL (TAG)] und [!DNL WhiteOps] zusammen, um den Bestand auf unserer Plattform sorgfältig zu kuratieren. Durch die proaktive Verwaltung unseres Angebots stellt DSP sicher, dass alle Advertiser auf der ganzen Plattform vor unmenschlichem Traffic (Bots, Crawler, Data Center Traffic und Betrug) geschützt sind und nur in markensicheren Kontexten bereitstellen.

Neben dem zentralen Qualitätsmanagement möchten wir Werbetreibende in die Lage versetzen, die ihrer Marke entsprechenden Steuerelemente zu entwerfen. Adobe Advertising Cloud bietet Integrationen mit [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science], [!DNL Oracle Data Cloud] und [!DNL Peer39], um sicherzustellen, dass jeder Advertiser sein gewünschtes Maß an Betrugsschutz, kontextbezogener Filterung und Keyword-Targeting auswählen kann.

## Advertising Cloud DSP-Qualitätsinitiativen

### Lagerbestandsüberprüfung mit [!DNL Ads.txt] Unterstützung

[[!DNL Ads.txt], which stands for [!DNL Authorized Digital Sellers]](https://iabtechlab.com/ads-txt) ist eine Initiative, die von  [!DNL Interactive Advertising Bureau] ([!DNL IAB]) im Juni 2017 eingeleitet wurde, um die ordnungsgemäße Darstellung des Bestands auf dem offenen Markt zu erleichtern und damit illegale Quellen des Verkehrs und der Domain-Spoofing zu bekämpfen. Beteiligte Herausgeber und Distributoren erklären öffentlich die Unternehmen, die zum Verkauf ihres digitalen Bestands berechtigt sind, sowie die Art dieser Beziehungen, indem sie eine `ads.txt` -Seite auf oberster Ebene der Domain verwalten (z. B. `example.com/ads.txt`).

DSP unterstützt [!DNL ads.txt], indem die `ads.txt`-Datei jedes Herausgebers gelesen wird und Sie die Möglichkeit erhalten, nur bei verifizierten [!DNL ads.txt]-Verkäufern zu kaufen. Wenn wir beispielsweise die Verkäufer, auf die wir zugreifen können, mit der Datei `nytimes.com` der New York Times `ads.txt` abgleichen, können wir feststellen, welche rechtmäßig sind und welche nicht, und wir blockieren die Täter, wenn die Platzierung so konfiguriert ist, dass sie nur bei verifizierten Verkäufern gekauft wird. <!-- can we actually mention NY Times? -->

Sie können die standardmäßigen [!DNL ads.txt]-Steuerelemente für jeden Advertiser<!-- [default ads.txt controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> festlegen und dann optional [die Einstellungen für jede Platzierung](/help/dsp/campaign-management/placements/placement-settings.md) anpassen, um:

* Inventar nur von autorisierten Direktverkäufern einer Domain kaufen

* Inventar nur von autorisierten Direktverkäufern und Wiederverkäufern einer Domain kaufen

* Kaufbestand von autorisierten Direktverkäufern und Wiederverkäufern einer Domain priorisieren

* Inventar von allen Verkäufern kaufen

### Überwachung von Platform-Betrug

DSP hat leistungsstarke interne Tools und Systeme zur Verwaltung von Betrug auf unserer Plattform entwickelt, die mit führenden Branchenanbietern wie [!DNL Whiteops] und [!DNL Integral Ad Science] zusammenarbeiten.

Darüber hinaus arbeitet Adobe eng mit [!DNL IAB] und [!DNL TAG] zusammen, um eine robuste und branchenübliche Betrugsblockierung zu gewährleisten, um unsere Advertiser zu schützen, indem Tools wie [!DNL ads.txt] genutzt werden (siehe vorherigen Abschnitt), die [!DNL IAB] Liste &quot;Bots und Spiders&quot;und die [!DNL TAG] Datacenter IP-Liste.

Durch unseren mehrdimensionalen Qualitätsansatz überwacht unser Team Anomalien und ungültige Traffic-Muster und sorgt so für weniger als 3 % ungültigen Traffic im geschützten Inventar. Alle Bestände, die verdächtig sind - einschließlich Inventar auf bestimmten Domänen oder von bestimmten Herausgebern oder Verkäufern - werden sofort auf der gesamten Plattform blockiert.

### Inventarzuordnung, -unterteilung und -kategorisierung

Die Bestandszuordnung ist der detaillierte Überprüfungs- und Onboarding-Prozess, der für alle neuen Bestände erforderlich ist, bevor er zu unserer Plattform hinzugefügt wird. Dieser Prozess soll die Sicherheit und Qualität des gesamten Bestands auf DSP gewährleisten.

* **Zuordnung:** Unser Inventarteam überprüft jede Domäne sorgfältig und bewertet Aspekte wie:

   * Markensicherheit

   * Verifizierung des Anzeigentyps

   * Allgemeine Inhalte, doppelte Domänen und gefälschte Adserving

* **Tiering:** Wir untersuchen ganzheitlich die Markenpräsenz im gesamten Ökosystem, um Inventare über verschiedene Ebenen hinweg zu klassifizieren. Sie können [Ihre Platzierungen](/help/dsp/campaign-management/placements/placement-settings.md) für die gewünschte Reichweite auf diese Ebenen ausrichten:

   * **[!UICONTROL T1]** - Markennamen, international anerkannte Sites

   * **[!UICONTROL T2]** - Optimale Sites, die aktuell und aktuell sind, ohne benutzergenerierten Inhalt und in der Regel nicht global erkannt werden

   * **[!UICONTROL T3]** - Benutzergenerierte Inhalte und Nischeninhalte

* **Site-Kategorisierung:** Um einfaches Content-Targeting und -Blockieren sicherzustellen, taggen wir jede Eigenschaft mit einer Advertising Cloud-definierten Site-Kategorie, die auf dem Eigenschaftsinhalt basiert. Sie können [diese Site-Kategorien je nach Platzierungszielen für jede Platzierung](/help/dsp/campaign-management/placements/placement-settings.md) als Ziel auswählen oder ausschließen.

### Umfassende Unterstützung für Site-Blocking

Advertising Cloud DSP bietet sowohl eine global gesperrte Siteliste als auch die Möglichkeit, benutzerdefinierte Blockierungslisten für Advertiser und Konten zu erstellen.

#### Advertising Cloud DSP - Liste global blockierter Sites

Advertising Cloud DSP verwaltet eine global gesperrte Site-Liste von Sites, die für unsicher erachtet werden, um Anzeigen auf diesen zu starten. Diese Liste enthält Websites mit verwerflichen Inhalten (z. B. Hass oder Terror) und von Bots infizierten Websites, gefälschten Pre-Roll-Dateien, nicht übereinstimmenden Domänen und anderen betrügerischen Aktivitäten.

Im Rahmen unserer Initiative zur Markensicherheit, um Aktivitäten auszurotten, die Werbetreibende betrügen, werden alle Sites anhand der in der Liste der blockierten Sites der Grafik aufgeführten Maßnahmen überprüft. Alle Sites, die die Markensicherheitsprüfungen nicht bestehen, werden der Liste der global blockierten Sites hinzugefügt. Da Advertising Cloud DSP diese Liste dynamisch verwaltet, können Sites auf der Grundlage der neuesten Analyse der Markensicherheit jederzeit aus der Liste wechseln.

Wenn Sie eine Site in die Liste der global blockierten Sites als Platzierungsziel einschließen, wird die Site mit einem roten Ausrufezeichen (!) gekennzeichnet. Dies bedeutet, dass Anzeigen nicht auf der gekennzeichneten Site ausgeführt werden.

#### Blockierte Sites auf Kontoebene und Advertiser-Ebene

Benutzer können auch Blockierungslisten auf Kontoebene und auf Advertiser-Ebene verwalten<!-- [account-level and advertiser-level blocked sites lists](/help/dsp/admin/blocked-sites-list-edit.md) -->, die automatisch für alle Platzierungen verwendet werden. Die Liste der blockierten Sites der unteren Ebene wird zusätzlich zur Liste der global blockierten Sites angewendet.

## Drittanbieterintegrationen

### Kontextuelle Filterung

Mit kontextuellen Filtern können Sie Anzeigenangebote basierend auf dem Kontext der Seite, auf der die Anzeige bereitgestellt wird, gezielt ausrichten oder blockieren. Adobe bietet kontextbezogene Filterung über Integrationen mit führenden Anbietern in der Branche: [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] und [!DNL Peer39]. Beispiele für aktuelle Filter sind [!UICONTROL Adult Content], [!UICONTROL Natural Disasters], [!UICONTROL Legal Drinking Age], [!UICONTROL MANGA], [!UICONTROL Epidemics] und [!UICONTROL G-rated Sites].

Sie können für jeden Advertiser Standardkontrollen für kontextbezogene Filter festlegen<!-- [default contextual filter controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> und dann optional [die Einstellungen für jede Platzierung](/help/dsp/campaign-management/placements/placement-settings.md) anpassen. Wenn Sie diese Funktion verwenden, fallen möglicherweise zusätzliche Gebühren an.

![Comscore-](/help/dsp/assets/comscore-logo.png) ![LogoDoubleVerify-](/help/dsp/assets/doubleverify-logo.png) ![LogoIntegral Ad Science-](/help/dsp/assets/ias-logo.png) ![LogoPeer39-Logo](/help/dsp/assets/peer39-logo.png)

### Blockierung von Betrugsvorgängen

Nutzen Sie unsere Drittanbieterintegrationen mit [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science] und [!DNL Peer39], um nicht menschlichen Traffic aus Ihren Kampagnen zu blockieren. Diese Integrationen bieten branchenführende Pre-Bid-Blockierungsfunktionen, mit denen Sie den allgemeinen und komplexen ungültigen Traffic (GIVT und SIVT) in Ihren Kampagnen minimieren können.

Sie können für jeden Advertiser<!-- [default pre-bid fraud blocking controls for each advertiser](/help/dsp/admin/advertiser-settings.md) --> Standardsteuerungen zum Blockieren von Pre-Bid-Betrug festlegen und dann optional [die Einstellungen für jede Platzierung](/help/dsp/campaign-management/placements/placement-settings.md) anpassen. Wenn Sie diese Funktion verwenden, fallen möglicherweise zusätzliche Gebühren an.

Weitere Informationen zur Funktionalität erhalten Sie von Ihrem bevorzugten Anbieter direkt oder von Ihrem Adobe-Kundenbetreuer.

![Comscore-](/help/dsp/assets/comscore-logo.png) ![LogoDoubleVerify-](/help/dsp/assets/doubleverify-logo.png) ![LogoIntegral Ad Science-](/help/dsp/assets/ias-logo.png) ![LogoPeer39-Logo](/help/dsp/assets/peer39-logo.png)

### Pre-Bid-Sichtbarkeit {#pre-bid-viewability}

Vorab-Targeting-Filter, die von unseren branchenführenden Partnern [!DNL DoubleVerify], [!DNL Oracle Advertising] ([!DNL Moat]) und [!DNL Integral Ad Science] unterstützt werden, ermöglichen es Werbetreibenden, sicherzustellen, dass ihre Kampagnen ihre gewünschten Sichtbarkeitsleistungsziele über Video- und Display-Inventar hinweg erfüllen.

Sie können standardmäßige Sichtbarkeitsfilter für jeden Advertiser<!-- [default pre-viewability filters for each advertiser](/help/dsp/admin/advertiser-settings.md) --> festlegen und dann optional [die Einstellungen für jede Platzierung](/help/dsp/campaign-management/placements/placement-settings.md) anpassen. Wenn Sie diese Funktion verwenden, fallen möglicherweise zusätzliche Gebühren an.

![DoubleVerify ](/help/dsp/assets/doubleverify-logo.png) ![logoOracle Advertising-](/help/dsp/assets/oracle-advertising-logo.png) ![LogoIntegral Ad Science-Logo](/help/dsp/assets/ias-logo.png)

### Themen-Targeting

DSP Thema-Targeting ermöglicht es Ihnen, Suchbegrifflisten durch Nutzung unserer branchenführenden kontextbezogenen Partner [!DNL Comscore] und [!DNL Oracle Data Cloud] ([!DNL Grapeshot]) als Ziel festzulegen oder zu blockieren.

Das Thema-Targeting hilft Ihnen dabei sicherzustellen, dass Ihre Anzeigen immer in einer mit Ihrer Marke abgestimmten Umgebung bereitgestellt werden, unabhängig davon, ob dies das Blockieren schädlicher Inhalte oder die Sicherstellung von Ausgaben in einem Kontext umfasst, der ein höheres Ergebnis gewährleistet.

Für das Themenziel müssen Sie Themensegmente direkt mit [!DNL Comscore] oder [!DNL Grapeshot] erstellen (unter Verwendung von [!DNL Oracle Data Cloud]). Sobald diese in der Partnerplattform erstellt wurden, können Sie für jede Platzierung](/help/dsp/campaign-management/placements/placement-settings.md) im Abschnitt [!UICONTROL  Audience Targeting] eine Segment-ID als Ziel angeben oder ausschließen. [ Für diese Funktion können zusätzliche Gebühren anfallen.

Wenden Sie sich zunächst an Ihren bevorzugten Anbieter oder Ihren Adobe-Kundenbetreuer.

![Comscore-](/help/dsp/assets/comscore-logo.png) ![LogoGrapeshot-Logo](/help/dsp/assets/oracle-grapeshot-logo.png)

### [!DNL DoubleVerify Authentic Brand Safety]

DSP hat sich mit [!DNL DoubleVerify] zusammengeschlossen, um die Targeting-Lösung [!DNL Authentic Brand Safety] anzubieten, mit der Sie ein zentralisiertes Set von Anforderungen an die Markensicherheit erstellen können, um auf all Ihren Einkaufsplattformen für Konsistenz zu sorgen.

Nachdem Sie ein Markensegment [!DNL DoubleVerify] mit dem erforderlichen Targeting erstellt haben, können Sie es in DSP verwenden, um Ihre Regeln für Bausteine nach dem Gebot in allen Webumgebungen mit dem Pre-Gebot zu replizieren.

Sie können für jeden Advertiser <!-- [specify a DoubleVerify segment ID for each advertiser](/help/dsp/admin/advertiser-settings.md) --> eine [!DNL DoubleVerify] Segment-ID angeben und dann optional [[!UICONTROL Authentic Brand Safety] für jede Platzierung ](/help/dsp/campaign-management/placements/placement-settings.md) aktivieren oder deaktivieren. DSP stellt Ihr Konto für die Verwendung der Segment-ID in Rechnung.

Weitere Informationen zur Funktion erhalten Sie direkt bei [!DNL DoubleVerify] oder bei Ihrem Adobe Account Manager.

![DoubleVerify-Logo](/help/dsp/assets/doubleverify-logo.png)

>[!MORELIKETHIS]
>
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)

<!-- >* [Advertiser Account Settings](/help/dsp/admin/advertiser-settings.md) -->
