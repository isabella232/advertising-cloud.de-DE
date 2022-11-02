---
title: Erfassen von Klick- und Impressionsdaten aus Advertising Cloud DSP-Kampagnen
description: Erfahren Sie, wie Sie Cookie-basierte Impressions- und Klickereignisse aus Advertising Cloud DSP-Anzeigen mit Audience Manager-Pixeln erfassen.
feature: Integration with Adobe Audience Manager
exl-id: eb717148-00ab-428a-97b9-e8396a5c47b0
source-git-commit: 8de057df8bf2b67f20a915e6e711902f11176747
workflow-type: tm+mt
source-wordcount: '1062'
ht-degree: 0%

---

# Erfassen von Medienbelichtungsdaten aus Advertising Cloud DSP-Kampagnen

*Advertiser nur mit Advertising Cloud DSP*

*Werbetreibende, die nur über eine Advertising Cloud-Adobe Audience Manager-Integration verfügen*

In diesem Dokument wird beschrieben, wie Sie Advertising Cloud DSP-Anzeigen mit Tags versehen, um Cookie-basierte Impressions- und Klickereignisse mithilfe von Audience Manager-Pixeln zu erfassen, sowie zusätzliche Aufgaben, die zur Verwendung der Daten erforderlich sind.

Die Ereignispixel erfassen keine Ereignisse, die in Cookie-losen Umgebungen wie mobilen Apps und vernetztem TV (CTV) auftreten.

## Schritt 1: Datenquelle in Audience Manager einrichten {#set-up-data-source}

Erstellen Sie in Audience Manager eine [Datenquelle](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html) für die DSP Impressions- und Klickdaten. Datenquellen-ID einschließen [in jedem Ereignis-Tag](#implement-dsp-pixels) damit alle verfolgten Ereignisse der Datenquelle zugeordnet werden.

>[!NOTE]
> Es ist möglich, alle Impressions- und Klickdaten für Werbekampagnen zu erfassen, die auf mehreren DSP in einer Datenquelle ausgeführt werden.

## Schritt 2: Implementieren von Impression- und Klickereignis-Pixeln auf Webseiten {#implement-dsp-pixels}

Advertiser können Ereignis-Tags für ihre eigenen Marken erstellen und implementieren. Wenden Sie sich bei Bedarf an Ihren Adobe Audience Manager-Berater oder an Ihren [!DNL Adobe] Kundenbetreuer für Support.

>[!NOTE]
>
>Wenn Ihr Unternehmen [!DNL Analytics] -Tracking verwenden, ist möglicherweise kein Klick-Tracking für Audience Manager erforderlich. Adobe Analytics erfasst Klicksignale und kann sie an den Audience Manager senden, indem [serverseitige Weiterleitung](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

### Pixel-Syntax

Die Ereignispixel müssen die folgenden Parameter enthalten.

**Impression-Tracking-Pixel:**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

mit [optionale zusätzliche Parameter](#parameters) Präfix mit `&`

**Clicktracking-Pixel:**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

mit [optionale zusätzliche Parameter](#parameters) Präfix mit `&`

Dabei gilt:

* `[Audience Manager customer domain]` ist der Domänenname, der Impressions- oder Klickereignisse an sendet. [!DNL Adobe].

* `[source id]` ist die ID für die [Datenquelle](#set-up-data-source) in der Sie DSP Impressions- und Klickdaten verfolgen.

* `[redirect URL]` ist die doppelt kodierte Umleitungs-URL. Wenn Sie ein Online-Kodierungs-Tool wie www.urlencoder.org verwenden, führen Sie die Zeichenfolge über den Kodierer aus und kodieren Sie das Ergebnis neu.

* `${TM_CAMPAIGN_ID_NUM}` ist die numerische Kampagnen-ID in DSP. Wenn Sie eine einzelne Kampagnen-ID hartcodieren möchten, anstatt das DSP-Makro zu verwenden, suchen Sie die ID in den Kampagneneinstellungen.

* Jeder [parameter](#key-value-pairs) mit dem Präfix `&` und im Format `d_parameter=parameter_id`, wobei `parameter` wird durch das Schlüssel-Wert-Paar für das neue Feld ersetzt. Beispiel: `&d_placement=${TM_PLACEMENT_ID_NUM}`

### Parameter als Schlüssel-Wert-Paare {#parameters}

**Format:**  `d_parameter=parameter_id`

    wobei:
    
    * Der Parameter wird durch &quot;&amp;&quot;vorangestellt.
    
    * &quot;Parameter&quot;wird durch das Schlüssel-Wert-Paar für das neue Feld ersetzt.
    
    Beispiel: `&amp;d_placement=${TM_PLACEMENT_ID_NUM}

Beide Pixeltypen können zusätzliche Parameter enthalten, da *Schlüssel-Wert-Paare* , um Eigenschaften zu erfassen oder Kampagnen-Metadaten (z. B. einen Platzierungsnamen oder einen Kampagnennamen) für andere Berichte bereitzustellen. Ein Schlüssel-Wert-Paar besteht aus zwei verwandten Elementen: a *key*, eine Konstante, die den Datensatz definiert, und eine *value*, eine Variable, die zum Satz gehört.

Im Schlüssel-Wert-Paar kann die Wertvariable entweder eine fest codierte ID oder eine *macro*: Hierbei handelt es sich um eine kleine Einheit von eigenständigem Code, der dynamisch durch die entsprechenden Werte ersetzt wird, wenn das Anzeigen-Tag zum Kampagnen- und Benutzertracking geladen wird. Für kampagnenbezogene Parameter können Sie [DSP Makros](/help/dsp/campaign-management/macros.md) anstelle von Audience Manager-Makros verwenden, um Kampagnenattribute zusammen mit den entsprechenden Impressions- oder Klickdaten an den Audience Manager zu senden, wobei ein einzelnes Pixel für alle Anzeigen verwendet wird. Die DSP Makros, die Sie in Ihre Ereignispixel einfügen, müssen geeignete Werte für die Schlüssel-Wert-Paare sein, die Sie in die Pixel einschließen. Beispiel: für die `d_placement` Schlüssel verwenden, würden Sie das DSP Makro `${TM_PLACEMENT_ID_NUM}` als Wert zum Erfassen von Platzierungs-IDs, die vom Advertising Cloud-Makro generiert wurden.

Eine Liste der Makros, die von Audience Manager für Impressionsereignis-Pixel unterstützt werden, finden Sie unter &quot;[Erfassen von Kampagnenimpressionsdaten über Pixelaufrufe](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html#supported-key-value-pairs).&quot;

Eine Liste der Makros, die von Audience Manager für Klickereignis-Pixel unterstützt werden, finden Sie unter &quot;[Erfassen von Kampagnen-Klickdaten über Pixelaufrufe](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html).&quot;

>[!TIP]
>
>* Die Best Practice besteht darin, die Kampagnen-, Platzierungs-, Kreativ- (Anzeigen) und Site-IDs einzubeziehen, damit Sie die Kampagnenattribute verwenden können, um Audience Manager-Eigenschaften zu erstellen.
>* Zur Erstellung von Audience Optimization-Berichten sind zusätzliche Parameter erforderlich.
>* Ersetzen Sie in den Schlüssel-Wert-Paaren die Werte durch die entsprechenden [DSP Makros](/help/dsp/campaign-management/macros.md) sodass Sie ein einzelnes Pixel für alle Anzeigen in allen Kampagnen verwenden können. Ändern Sie beispielsweise `d_campaign=[%campaignID%]`nach `d_campaign=${TM_CAMPAIGN_ID_NUM}` zum Erfassen von Kampagnen-IDs, die vom Advertising Cloud-Makro generiert wurden.
>* Sie können bei Bedarf eigene Parameter mit fest programmierten Werten erstellen. Beispiel: `d_DSP=AdCloud`


Beispiel eines Impressionsereignis-Pixels:

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### Hinzufügen der Pixel

#### Impression-Tracking-Pixel

Fügen Sie allen Anzeigen in Ihrer [!DNL DSP] Kampagnen. Sie können dies an einer der folgenden Stellen tun:

* Auf Platzierungsebene, die das Pixel standardmäßig auf alle Anzeigen in der Platzierung anwendet. Fügen Sie im Abschnitt Tracking der Platzierungseinstellungen das Pixel im [[!UICONTROL Event pixels] field](/help/dsp/campaign-management/placements/placement-settings.md).

* Auf Anzeigenebene, wodurch alle Ereignispixel auf Platzierungsebene außer Kraft gesetzt werden. In den Anzeigeneinstellungen [Erstellen Sie ein Ereignispixel auf der [!UICONTROL Pixel] tab](/help/dsp/campaign-management/ads/ad-edit.md).

* (Für Anzeigen auf einem Drittanbieter-Anzeigenserver) Auf Anzeigenebene innerhalb des Werbeservers.

#### Klick-Tracking-Pixel

Fügen Sie innerhalb des Anzeigen-Servers das Clickevent-Pixel (mit angehängter kodierter URL) an der Stelle ein, an der Sie normalerweise die Clickthrough-URL der Anzeige einfügen.

## Schritt 3: Aufgaben nach der Implementierung

Sobald die Ereignis-Tags implementiert sind, fließen die Daten in die Datenerfassungsserver des Audience Managers. Führen Sie die folgenden Aufgaben aus, bevor Sie die Daten in Berichten verwenden können.

### Erstellen Sie eine [!DNL Amazon S3] Bucket und Datenquelle

Sobald sich Ihre Daten auf den Audience Manager-Servern befinden, müssen Sie eine [!DNL Amazon Simple Storage Service] ([!DNL Amazon S3]) und dann einer Datenquelle, an die alle Pixeldaten gesendet werden. Wenden Sie sich an Ihren Audience Manager-Berater oder [Kundenunterstützung](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html) wenn Sie Unterstützung benötigen.

### Erstellen von Audience Manager-Eigenschaften und -Segmenten

Ihre Ereignisdaten fließen in Audience Manager als [unbenutzte Signale](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html). Manuelles Erstellen [regelbasierte Eigenschaften](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) aus den erfassten Daten und erstellen Sie dann [Segmente](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html) Verwendung dieser Eigenschaften, bevor Sie die Daten in Berichten verwenden können.

Beispieleigenschaft, mit der Benutzerdaten für Benutzer gefüllt werden, die einem bestimmten kreativen Element in DSP ausgesetzt sind:

1. Identifizieren Sie das Ereignis als `d_event = imp`.
1. Identifizieren Sie die kreative ID innerhalb der DSP Kampagne und ordnen Sie sie dann der Eigenschaft als `d_creative=[Creative ID]`.

![Bildschirm zur Erstellung von Eigenschaften](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [Advertising Cloud DSP Makros](/help/dsp/campaign-management/macros.md)
>* [Übersicht über das Senden von DSP-Exposure-Daten an Adobe Audience Manager](overview.md)
>* [Nutzungsszenarios](use-cases.md)

