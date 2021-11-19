---
title: Von verwendete Advertising Cloud IDs [!DNL Analytics]
description: Von verwendete Advertising Cloud IDs [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ed1aab7b-9bd0-4d42-9bfb-9c6fa6db76bc
source-git-commit: 143e8e756d13597bf923d0b6f5b2510f834e6e0f
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 0%

---

# Von verwendete Advertising Cloud IDs [!DNL Analytics]

*Werbetreibende, die nur über eine Advertising Cloud-Adobe Analytics-Integration verfügen*

*Gilt für Advertising Cloud DSP und Advertising Cloud Search*

Advertising Cloud verwendet zwei IDs für die Leistungsverfolgung vor Ort: die *EF ID* und *AMO-ID*.

Wenn eine Ad-Impression auftritt, erstellt Advertising Cloud die AMO-ID- und EF-ID-Werte und speichert sie. Wenn ein Besucher, der eine Anzeige gesehen hat, auf die Site gelangt, ohne auf eine Anzeige zu klicken, [!DNL Analytics] ruft diese Werte von Advertising Cloud über [!DNL Analytics for Advertising Cloud] JavaScript-Code. Für Durchsichts-Traffic: [!DNL Analytics] generiert eine zusätzliche ID (`SDID`), das zum Zuordnen der EF ID und AMO ID zu verwendet wird [!DNL Analytics]. Für Clickthrough-Traffic werden diese IDs mithilfe der `s_kwcid` und `ef_id` Abfragezeichenfolgenparameter.

Advertising Cloud unterscheidet mithilfe der folgenden Kriterien zwischen einem Clickthrough- oder Durchsichtseintrag auf der Website:

* Ein Durchsichtseintrag wird erfasst, wenn ein Benutzer die Site besucht, nachdem er eine Anzeige angesehen, aber nicht darauf geklickt hat. [!DNL Analytics] erfasst eine Durchsicht, wenn zwei Bedingungen erfüllt sind:
   * Der Besucher hat keine Clickthroughs für eine [!DNL DSP] oder [!DNL Search] Anzeige während der [Klick-Lookback-Fenster](#lookback-a4adc).
   * Der Besucher hat mindestens eine [!DNL DSP] Anzeige während der [Impression-Lookback-Fenster](#lookback-a4adc). Die letzte Impression wird als Durchsicht übergeben.
* Ein Clickthrough-Eintrag wird erfasst, wenn ein Site-Besucher auf eine Anzeige klickt, bevor er die Site betritt. [!DNL Analytics] erfasst einen Clickthrough, wenn eine der folgenden Bedingungen eintritt:
   * Die URL enthält eine EF ID und eine AMO ID, die von Advertising Cloud zur Landingpage-URL hinzugefügt wurden.
   * Die URL enthält keine Trackingcodes, aber der Advertising Cloud-JavaScript-Code erkennt einen Klick innerhalb der letzten zwei Minuten.

![Ansichtsbasierte Advertising Cloud-Ansicht [!DNL Analytics] Integration](/help/integrations/assets/a4adc-view-through-process.png)

*Abbildung 1: Ansichtsbasierte Advertising Cloud-Ansicht [!DNL Analytics] Integration*

![Advertising Cloud klickt auf URL-basiert [!DNL Analytics] Integration](/help/integrations/assets/a4adc-click-through-process.png)

*Abbildung 2: Advertising Cloud klickt auf URL-basiert [!DNL Analytics] Integration*

## Advertising Cloud EF IDs

Die EF ID ist ein eindeutiges Token, mit dem Advertising Cloud Aktivitäten mit einem Online-Klick oder einer Anzeige verknüpft. Die EF ID wird in einer [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) oder die rVar-Dimension (reservierte eVar) (Advertising Cloud EF ID) und verfolgt jeden Anzeigenklick oder jede Anzeige auf der Browser- oder Geräteebene. EF-IDs dienen hauptsächlich als Schlüssel zum Senden [!DNL Analytics] Daten an Advertising Cloud zur Berichterstellung und Angebotsoptimierung in Advertising Cloud.

### EF ID Format

```<Advertising Cloud visitor ID>:<timestamp>:<channel type>```

<!-- <*Advertising Cloud visitor ID*>:<*timestamp*>:<*channel type*> -->

wobei:

* &lt;*Advertising Cloud-Besucher-ID*> ist eine eindeutige ID pro Besucher (z. B. &quot;ÄhKVaAAABCkJ0mDt&quot;). Auch als *Surfer-ID*.

* &lt;*timestamp*> ist die Zeit im Format JJJJMMTDDHHMMSS (z. B. 20190821192533 für Jahr 2019, Monat 08, Tag 21, Zeit 19).:25:33).

* &lt;*Kanaltyp*> ist der Kanaltyp, der für den Klick oder die Belichtung verantwortlich ist:

   * `d` für einen Klick auf eine DSP Display-Anzeige (Display-Clickthrough)
   * `i` für eine Impression einer DSP Display-Anzeige (Durchsicht der Anzeige)
   * `s` für einen Klick auf eine Suchanzeige (Durchsuchen-Clickthrough).

Beispiel `EF `ID: WcmibgAAAHJK1RyY:1551968087687:d

>[!NOTE]
>
>Bei EF IDs wird zwischen Groß- und Kleinschreibung unterschieden. Wenn eine [!DNL Analytics] -Implementierung erzwingt das URL-Tracking in Kleinbuchstaben. Anschließend erkennt Advertising Cloud die EF-ID nicht. Dies wirkt sich auf Gebote und Berichte von Advertising Cloud aus, hat jedoch keine Auswirkungen auf die Berichterstellung von Advertising Cloud innerhalb von [!DNL Analytics].

### Die EF ID-Dimension in [!DNL Analytics]

In [!DNL Analytics] Berichte, können Sie EF ID-Daten finden, indem Sie nach der [!UICONTROL EF ID] Dimension und unter Verwendung der [!UICONTROL EF ID Instance] Metrik.

EF-IDs unterliegen in Analysis Workspace der Grenze von 500.000 eindeutigen Kennungen. Sobald der Wert von 500.000 erreicht ist, werden alle neuen Trackingcodes unter dem einzeiligen Elementtitel gemeldet.[!UICONTROL Low Traffic].&quot; Da die Möglichkeit besteht, dass die Berichtstreue fehlt, werden die EF-IDs nicht klassifiziert und sollten Sie sie nicht für Segmente oder Berichte in [!DNL Analytics].

## Advertising Cloud AMO-IDs

Die AMO-ID verfolgt jede eindeutige Anzeigenkombination auf einer weniger detaillierten Ebene und wird für [!DNL Analytics] Datenklassifizierung und Erfassung von Werbemetriken (wie Impressionen, Klicks und Kosten) aus Advertising Cloud. Die AMO-ID wird in einer [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) oder rVar-Dimension (AMO-ID) und wird ausschließlich für die Berichterstellung in [!DNL Analytics].

Die AMO-ID wird auch als `s_kwcid`, der manchmal als &quot;[!DNL the squid].&quot;

### AMO-ID-Format für [!DNL DSP]

```<Channel ID>!<Ad ID>!<Placement ID>```

wobei:

* &lt;*Kanal-ID*> kann sein:

   * `AC` = Advertising Cloud DSP
   * `AL` für Advertising Cloud Search

* &lt;*Anzeigen-ID*> wird eine von Advertising Cloud generierte eindeutige Kennung für eine Anzeige verwendet. Sie dient als Schlüssel für die Übersetzung von Advertising Cloud-Entitätsmetadaten in lesbare [!DNL Analytics] Dimensionen.

* &lt;*Platzierungs-ID*> ist eine von Advertising Cloud generierte eindeutige Kennung für eine Platzierung. Sie dient als Schlüssel für die Übersetzung von Advertising Cloud-Entitätsmetadaten in lesbare [!DNL Analytics] Dimensionen.

<!-- <*Channel ID*>!<*Ad ID*>!<*Placement ID*>

where:

* <*Channel ID*> may be:

    * `AC` = Advertising Cloud DSP
    * `AL` for Advertising Cloud Search

* <*Ad ID*> is used an Advertising Cloud-generated unique identifier for an ad. It serves as a key for translating Advertising Cloud entity metadata into readable [!DNL Analytics] dimensions.

* <*Placement ID*> is an Advertising Cloud-generated unique identifier for an placement. It serves as a key for translating Advertising Cloud entity metadata into readable [!DNL Analytics] dimensions.
 -->

Beispiel einer AMO-ID: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

### AMO-ID-Format für [!DNL Search]

AMO-IDs für [!DNL Search] für jede Suchmaschine ein bestimmtes Format verwenden. Das Format für alle Suchmaschinen beginnt mit Folgendem:

```AL!{ef_userid}!{ef_sid}```

wobei:

* `AL` ist die Kanal-ID für den Suchkanal.
* `{ef_userid}` ist die eindeutige numerische Benutzer-ID, die Advertising Cloud dem Advertiser zuweist.
* `{ef_sid}` ist die numerische ID, die Advertising Cloud für die angegebene Suchmaschine verwendet, z. B. `3` für [!DNL Google Ads] oder `10` für [!DNL Microsoft Advertising].

Im Folgenden finden Sie die vollständigen AMO ID-Formate für einige Suchmaschinen. Wenden Sie sich bei AMO-ID-Formaten für andere Suchmaschinen an Ihren [!DNL Adobe] Kundenbetreuer.

AMO-ID-Format für [!DNL Google Ads]:

```AL!{ef_userid}!{ef_sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}```

wobei:

* `{creative}` ist die [!DNL Google Ads] eindeutige numerische ID für das Kreativelement.
* `{matchtype}` ist der Übereinstimmungstyp des Suchbegriffs, der die Anzeige ausgelöst hat: `e` exakt, `p` für Wortgruppe oder `b` für einen breiten Bereich.
* `{placement}` ist der Domänenname der Website, auf der auf die Anzeige geklickt wurde. Ein Wert ist für Anzeigen in platzierungszielgerichteten Kampagnen und für Anzeigen in auf Suchbegriffe ausgerichteten Kampagnen verfügbar, die auf Inhalts-Sites angezeigt werden.
* `{network}` gibt das Netzwerk an, aus dem der Klick erfolgte:  `g` für [!DNL Google] Suche (nur für Anzeigen mit Keyword-Targeting), `s` für einen Suchpartner (nur für Anzeigen mit Keyword-Targeting) oder `d` für das Display-Netzwerk (für Anzeigen mit Keyword oder Platzierungszielgruppe).
* `{keyword}` ist entweder der spezifische Suchbegriff, der Ihre Anzeige ausgelöst hat (auf Suchseiten) oder der beste Suchbegriff (auf Inhalts-Sites).

AMO-ID-Format für [!DNL Microsoft Advertising]:

```AL!{ef_userid}!{ef_sid}!{AdId}!{OrderItemId}```

wobei:

* `{AdId}` ist die [!DNL Microsoft Advertising] eindeutige numerische ID für das Kreativelement.
* `{OrderItemId}` ist die [!DNL Microsoft Advertising] numerische ID für den Suchbegriff.

### AMO-ID-Dimension in [!DNL Analytics]

In Analytics-Berichten können Sie AMO-ID-Daten finden, indem Sie nach der [!UICONTROL AMO ID] Dimension und unter Verwendung der [!UICONTROL AMO ID Instance] Metrik. Die [!UICONTROL AMO ID] -Dimension enthält alle erfassten AMO-ID-Werte, während die [!UICONTROL AMO ID Instance] gibt an, wie oft ein AMO-ID-Wert von der Site erfasst wurde. Wenn beispielsweise dieselbe Suchanzeige viermal angeklickt wurde, Analytics jedoch sieben Site-Einträge verfolgt hat, wird [!UICONTROL AMO ID Instance] wäre sieben (7) und [!UICONTROL Clicks] wäre vier (4).

Für alle Berichte oder Prüfungen innerhalb von [!DNL Analytics]Best Practice ist, die AMO-ID zusammen mit der entsprechenden Instanz zu verwenden. Weitere Informationen finden Sie unter &quot;[Datenvalidierung für [!DNL Analytics for Advertising Cloud]](data-variances.md#data-validation)&quot;in &quot;Erwartete Datenabweichungen zwischen [!DNL Analytics] und Advertising Cloud.&quot;

## Informationen zu Analytics Classifications

In [!DNL Analytics], [Classification](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) ist ein Metadatenelement für einen bestimmten Trackingcode, z. B. Konto, Kampagne oder Anzeige. Advertising Cloud kategorisiert Advertising Cloud-Rohdaten mithilfe von Klassifizierungen, damit Sie die Daten beim Generieren von Berichten auf unterschiedliche Weise anzeigen können (z. B. nach Anzeigentyp oder Kampagne). Klassifizierungen bilden die Grundlage für die Advertising Cloud-Berichterstellung in [!DNL Analytics] und kann mit den AMO-Metriken verwendet werden, z. B. [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions]und [!UICONTROL AMO Clicks]sowie mit benutzerspezifischen und standardmäßigen Onsite-Ereignissen wie [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders]und [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Erwartete Datenabweichungen zwischen [!DNL Analytics] und Advertising Cloud](data-variances.md)

