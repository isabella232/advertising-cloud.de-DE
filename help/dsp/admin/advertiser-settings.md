---
title: Advertiser-Kontoeinstellungen
description: Siehe Beschreibungen der verfügbaren Advertiser-Einstellungen.
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '871'
ht-degree: 0%

---

# Advertiser-Kontoeinstellungen

*Nicht für schreibgeschützte Benutzer verfügbar*

## [!UICONTROL General] Einstellungen

**[!UICONTROL Advertiser Name]:** Der Name des Advertisers.

**[!UICONTROL Category]:** Die Kategorie, in der das Unternehmen des Werbetreibenden tätig ist. Die Kategorie wird den Herausgebern mitgeteilt, wenn Sie ein Angebot für den Bestand abgeben. Stellen Sie sicher, dass Sie eine Kategorie auswählen, die Ihren Anzeigen entspricht, oder Herausgeber können Ihre Anzeigen ablehnen.

>[!NOTE]
>
>Wenn Sie *[!UICONTROL Other]*, kann der Advertiser nicht auf DSP zugreifen. [!DNL On Demand Inventory].

**[!UICONTROL Advertiser URL]:** Homepage oder Haupt-Website-URL des Advertisers (beginnend mit `http://` oder `https://`).

**[!UICONTROL Share all private exchange feeds into this advertiser]:** (Nur neue Advertiser-Konten) Stellt alle für das DSP des Unternehmens konfigurierten privaten Exchange-Feeds für den Advertiser zur Verfügung.

### [!UICONTROL Adobe IMS IDs]

Werbetreibende mit zusätzlichen Adobe Experience Cloud-Produkten können Daten mithilfe der eindeutigen ID des Unternehmens zum Experience Cloud über einige Produkte hinweg freigeben. Sie können bestimmte Produktintegrationen im [!UICONTROL Integrations] Abschnitt.

**[!UICONTROL Account IMS org and ID]:** (Advertiser mit zusätzlichen Experience Cloud-Produkten, die über ein Experience Cloud-Konto mit mehreren Advertisern lizenziert sind; optional) Die Experience Cloud-Organisations-ID des Advertisers.

**[!UICONTROL Advertiser IMS org and ID]:** (Advertiser mit Direktlizenzen für zusätzliche Experience Cloud-Produkte; optional) Die Experience Cloud-Organisations-ID des Advertisers.

### [!UICONTROL Integrations]

(Optional) Zusätzliche Experience Cloud-Produkte, die mit dem DSP verknüpft sind. Die Produkte müssen derselben Organisations-ID des Experience Cloud zugeordnet sein, die in der Variablen [!UICONTROL Adobe IMS IDs] Abschnitt.

**[!UICONTROL Attribution services]> [!UICONTROL Adobe Media Optimizer]:** (Werbetreibende mit [!DNL Adobe Advertising Search] oder die Adobe Advertising Conversion-Pixel verwenden) A [!DNL Search] -Konto, mit dem DSP Attributionsdaten austauschen.

**[!UICONTROL Report suites]> [!UICONTROL Adobe Analytics]:** (Werbetreibende mit Adobe Analytics; fakultativ; nur auf Daten anwendbar, die mit Adobe Advertising-Konversions-Tracking-Tags erfasst wurden, die eine [!DNL EF Redirect] und nur Token) Eine oder mehrere [!DNL Analytics] Report Suites, an die DSP Daten sendet, die von Herausgebern und Anbietern erfasst werden. Analytics sendet außerdem die erfassten Daten von der Site des Kunden an DSP.

Damit die Daten in den Report Suites angezeigt werden, muss die Variable [!DNL Search] Einstellung auf Advertiser-Ebene auf &quot;[!UICONTROL Enable tracking for SAINT feeds]&quot; muss aktiviert sein. Darüber hinaus gibt die [!DNL Analytics] -Konto muss für den Empfang von Daten von Adobe Advertising konfiguriert sein.

>[!WARNING]
>
>Wenn Sie eine zuvor verknüpfte Report Suite entfernen, tauschen DSP keine Daten mehr mit dieser Suite aus. Datenfluktuationen werden erwartet.

Weitere Informationen zur Integration mit [!DNL Analytics], siehe[Übersicht über [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md).&quot;

**[!UICONTROL Audiences]> [!UICONTROL Adobe Analytics Cloud]:** (Advertiser mit Adobe Audience Manager oder Adobe Analytics; optional) ein Audience Manager oder [!DNL Analytics] -Konto, aus dem DSP Segmentmetadaten, Hierarchiedaten und eindeutige Zielgruppendaten für alle Adobe-Zielgruppen des Advertisers abruft. Dazu gehören Daten für:

* Audience Manager-Segmente
* [!DNL Analytics] Segmente, die in Adobe Experience Cloud veröffentlicht werden
* Segmente, die in Adobe Experience Cloud mit dem [!DNL People core service]
* Segmente, die in Adobe Experience Platform erstellt und über Audience Manager an Adobe Advertising gesendet werden

Die anfängliche Synchronisation dauert etwa 24 Stunden. Danach werden die Daten in Echtzeit mit einer Verzögerung von einer bis zwei Sekunden synchronisiert.
<!-- I don't think this is true anymore:
Segment membership data is sent to Adobe Advertising only after one of the following:

* The segment is targeted in an Adobe Advertising placement or audience library
* The segment is added to the Adobe Advertising batch and real-time destinations within the Audience Manager user interface
-->

## [!UICONTROL Targeting] Einstellungen

Sie können optional Standardziele für die neuen Platzierungen des Werbetreibenden konfigurieren. Benutzer können die Standardziele für jede neue Platzierung überschreiben.

### [!UICONTROL Geo-targeting]

**[!UICONTROL Countries]:** Das Standardland für das Geotargeting jeder Platzierung. Benutzer können für jede Platzierung das Land ändern und spezifischeres Geotargeting konfigurieren.

### [!UICONTROL Audience Targeting]

**[!UICONTROL Audiences to exclude]:** Alle Zielgruppen oder Segmente, die standardmäßig unterdrückt werden sollen. Benutzer können die Ausschlüsse für jede Platzierung ändern.

### [!UICONTROL Media Quality]

#### [!UICONTROL Contextual Filtering]

Typen [!DNL Comscore], [!DNL DoubleVerify], [!DNL Integral Ad Science]und [!DNL Peer39] anzuwendende Kontextfilter. Sie können die Einstellungen auf Advertiser-Ebene auf der [Platzierungsebene](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-context}

**[!UICONTROL Block sites that are]:** (Optional) Ein oder mehrere Arten von Inventarkontext, der standardmäßig blockiert werden soll. Es können zusätzliche Gebühren erhoben werden.

##### [!UICONTROL Peer 39] {#peer39-context}

**[!UICONTROL Target sites that are]:** (Optional) Ein oder mehrere Arten von Bestandsattributen, die standardmäßig als Ziel dienen sollen. Es können zusätzliche Gebühren erhoben werden.

##### [!UICONTROL ComScore]

**[!UICONTROL Block sites that are]:** (Optional) Ein oder mehrere Arten von Bestandsattributen, die standardmäßig blockiert werden sollen. Es können zusätzliche Gebühren erhoben werden.

##### [!UICONTROL Integral Ad Science] {#ias-context}

**[!UICONTROL Adult Content]:** (Optional) Der Grad des Erwachseneninhalts, für den Anzeigen standardmäßig blockiert werden sollen: *[!UICONTROL Do Not Block]* (Standardeinstellung), *[!UICONTROL Standard]* oder *[!UICONTROL Strict]*. Es können zusätzliche Gebühren erhoben werden.

**[!UICONTROL Alcohol Content]:** (Optional) Der Alkoholgehalt, für den Anzeigen standardmäßig blockiert werden sollen: *[!UICONTROL Do Not Block]* (Standardeinstellung), *[!UICONTROL Standard]* oder *[!UICONTROL Strict]*. Es können zusätzliche Gebühren erhoben werden.

#### [!UICONTROL Pre-Bid Fraud Blocking]

Arten von zu blockierenden Websites auf der Grundlage von betrügerischem Traffic und verdächtigen Aktivitäten, die durch [!DNL DoubleVerify], [!DNL Integral Ad Science]und [!DNL Peer39]. Sie können die Einstellungen auf Advertiser-Ebene auf der [Platzierungsebene](/help/dsp/campaign-management/placements/placement-settings.md).

##### [!UICONTROL DoubleVerify] {#doubleverify-fraud}

**[!UICONTROL Block Fraud Sites (100% Invalid traffic) and User-Based Fraud and IVT Devices]:** Standardmäßig werden alle 100 % ungültigen Traffic, einschließlich Traffic auf entführten Geräten, für neue Platzierungen blockiert. Es können zusätzliche Gebühren erhoben werden.

**[!UICONTROL Also block sites with]:** (Optional) Eine zusätzliche Stufe von Betrug und ungültigem Traffic, die dazu führt, dass DSP Anzeigen standardmäßig blockieren:  *[!UICONTROL None]* (Standardeinstellung, die zusätzlichen Traffic nicht blockiert), *[!UICONTROL >2% Average Fraud/IVT levels (lowest reach)]*, *[!UICONTROL >4% Average Fraud/IVT levels]*, *[!UICONTROL >6% Average Fraud/IVT levels]*, *[!UICONTROL >10% Average Fraud/IVT levels]* oder *[!UICONTROL >25% Average Fraud/IVT levels]*. Es können zusätzliche Gebühren erhoben werden.

##### [!UICONTROL Peer 39] {#peer-39-fraud}

**[!UICONTROL Block sites that are]:** (Optional) Ein oder mehrere Arten von Betrug, durch den Anzeigen standardmäßig blockiert DSP: *[!UICONTROL Fraud]* (die alle betrügerischen Websites blockiert), *[!UICONTROL Fraud: Bot Sites_Non-Human traffic]* und/oder *[!UICONTROL Fraud: Zero Ads]*. Es können zusätzliche Gebühren erhoben werden.

##### [!UICONTROL Integral Ad Science] {#ias-fraud}

**[!UICONTROL Block sites that are]:** (Optional) Ein Typ von verdächtigen Website- oder App-Aktivitäten, der dazu führt, dass DSP Anzeigen standardmäßig blockieren: *[!UICONTROL None]* (die Standardeinstellung, die keine auf verdächtigen Aktivitäten basierenden Anzeigen blockiert), *[!UICONTROL Suspicious Activity - High Risk]* oder *[!UICONTROL Suspicious Activity - High or Moderate Risk]*. Es können zusätzliche Gebühren erhoben werden.

#### [!UICONTROL Ads.text]

**[!UICONTROL Ads.txt Filtering]:** Standardmäßig wird die Ebene von [[!DNL Ads.txt] Filter vor dem Angebot](https://iabtechlab.com/ads-txt-about/) zur Verwendung durch Nutzung der [!DNL Authorized Digital Sellers] list:
* *[!UICONTROL Opt out of ads.txt (default)]*: Inventar von allen Verkäufern zu kaufen.
* *[!UICONTROL Ads.txt sellers + sites without ads.txt]*: Zur Priorisierung des Kaufinventars von autorisierten Direktverkäufern und Wiederverkäufern einer Domain.
* *[!UICONTROL Ads.txt sellers only]*: Um Inventar nur von autorisierten Direktverkäufern und Wiederverkäufern einer Domain zu kaufen.
* *[!UICONTROL Ads.txt sellers only]*: Um Inventar nur von autorisierten Direktverkäufern einer Domain zu kaufen.

Sie können die Einstellung auf Advertiser-Ebene auf der [Platzierungsebene](/help/dsp/campaign-management/placements/placement-settings.md).

#### [!UICONTROL Safe Site Block]

**[!UICONTROL Enable Site Safety Block]:** Standardmäßig ermöglicht einen Filter nach dem Angebot in Echtzeit, um sicherzustellen, dass Anzeigen auf den vom Advertiser angesprochenen Sites bereitgestellt werden. <!-- Can remove this: Users can enable or disable the feature for each placement. I don't see this option, but I should probably verify. If this can't be edited at placement level, then remove "By default." If it can, say that you can override at placement level. -->

#### [!UICONTROL DoubleVerify Authentic Brand Safety]

**[!UICONTROL DoubleVerify Account]:** ([!DNL DoubleVerify] nur Kunden; optional) Die Kennung des Markensicherheitssegments, die der Organisation zugeordnet ist [!DNL DoubleVerify] -Konto.

**[!UICONTROL Enable Authentic Brand Safety]:** (Optional) Standardmäßig aktiviert [!DNL DoubleVerify] Authentische Markensicherheit, die Impressionen nach dem Gebot blockiert, indem die benutzerdefinierten Markensicherheitsregeln verwendet werden, die für die angegebene Segment-ID konfiguriert sind. DSP stellt Ihr Konto für die Verwendung der Segment-ID in Rechnung.

Sie können die Einstellung auf Advertiser-Ebene auf Platzierungsebene überschreiben.

>[!MORELIKETHIS]
>
>* [Werbekonto erstellen](/help/dsp/admin/advertiser-create.md)


<!-- >* [View the Advertiser List for the Account](/help/dsp/admin/advertiser-view.md) -->
