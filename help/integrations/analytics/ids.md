---
title: Von [!DNL Analytics] verwendete Advertising Cloud IDs
description: Von [!DNL Analytics] verwendete Advertising Cloud IDs
feature: Integration with Adobe Analytics
exl-id: ed1aab7b-9bd0-4d42-9bfb-9c6fa6db76bc
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '1157'
ht-degree: 0%

---

# Von [!DNL Analytics] verwendete Advertising Cloud IDs

*Werbetreibende, die nur über eine Advertising Cloud-Adobe Analytics-Integration verfügen*

*Gilt für Advertising Cloud DSP und Advertising Cloud Search*

Advertising Cloud verwendet zwei IDs für die Leistungsverfolgung vor Ort:  die EF ID und die AMO-ID.

Wenn eine Ad-Impression auftritt, erstellt Advertising Cloud die AMO-ID- und EF-ID-Werte und speichert sie. Wenn ein Besucher, der eine Anzeige gesehen hat, auf die Site gelangt, ohne auf eine Anzeige zu klicken, ruft [!DNL Analytics] diese Werte über den JavaScript-Code [!DNL Analytics for Advertising Cloud] aus Advertising Cloud auf. Für Durchsichts-Traffic generiert [!DNL Analytics] eine zusätzliche ID (`SDID`), die zum Zuordnen der EF ID und AMO-ID zu [!DNL Analytics] verwendet wird. Für Clickthrough-Traffic sind diese IDs mithilfe der Abfragezeichenfolgenparameter `s_kwcid` und `ef_id` in der URL der Landingpage enthalten.

Advertising Cloud unterscheidet mithilfe der folgenden Kriterien zwischen einem Clickthrough- oder Durchsichtseintrag auf der Website:

* Ein Durchsichtseintrag wird erfasst, wenn ein Benutzer die Site besucht, nachdem er eine Anzeige angesehen, aber nicht darauf geklickt hat. [!DNL Analytics] erfasst eine Durchsicht, wenn zwei Bedingungen erfüllt sind:
   * Der Besucher hat keine Clickthroughs für eine [!DNL DSP] - oder [!DNL Search] -Anzeige während des [Klick-Lookback-Fensters](#lookback-a4adc).
   * Der Besucher hat mindestens eine [!DNL DSP] Anzeige während des [Impression-Lookback-Fensters](#lookback-a4adc) gesehen. Die letzte Impression wird als Durchsicht übergeben.
* Ein Clickthrough-Eintrag wird erfasst, wenn ein Site-Besucher auf eine Anzeige klickt, bevor er die Site betritt. [!DNL Analytics] erfasst einen Clickthrough, wenn eine der folgenden Bedingungen eintritt:
   * Die URL enthält eine EF ID und eine AMO ID, die von Advertising Cloud zur Landingpage-URL hinzugefügt wurden.
   * Die URL enthält keine Trackingcodes, aber der Advertising Cloud-JavaScript-Code erkennt einen Klick innerhalb der letzten zwei Minuten.

![Sichtbare  [!DNL Analytics] Integration mit Advertising Cloud](/help/integrations/assets/a4adc-view-through-process.png)

*Abbildung 1: Sichtbare  [!DNL Analytics] Integration mit Advertising Cloud*

![Advertising Cloud klickt auf URL-basierte  [!DNL Analytics] Integration](/help/integrations/assets/a4adc-click-through-process.png)

*Abbildung 2: Advertising Cloud klickt auf URL-basierte  [!DNL Analytics] Integration*

## Advertising Cloud EF IDs

Die EF ID ist ein eindeutiges Token, mit dem Advertising Cloud Aktivitäten mit einem Online-Klick oder einer Anzeige verknüpft. Die EF ID wird in einer [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)- oder rVar-Dimension (Advertising Cloud EF ID) gespeichert und verfolgt jeden Anzeigenklick oder jede Anzeige auf der Browser- oder Geräteebene. EF-IDs dienen hauptsächlich als Schlüssel zum Senden von [!DNL Analytics]-Daten an Advertising Cloud für die Berichterstellung und Angebotsoptimierung innerhalb von Advertising Cloud.

### EF ID Format

```<Advertising Cloud visitor ID>:<timestamp>:<channel type>```

<!-- <*Advertising Cloud visitor ID*>:<*timestamp*>:<*channel type*> -->

wobei:

* &lt;>Die Advertising Cloud-Besucher-ID *> ist eine eindeutige ID pro Besucher (z. B. &quot;ÄhKVaAAABCkJ0mDt&quot;).* Auch *Surfer-ID* genannt.

* &lt;>timestamp *> ist die Zeit im Format JJJJMMDDHHMMSS (z. B. 20190821192533 für Jahr 2019, Monat 08, Tag 21, Zeit 19:25:33).*

* &lt;>Kanaltyp *> ist der für den Klick oder die Belichtung verantwortliche Kanaltyp:*

   * `d` für einen Klick auf eine DSP Display-Anzeige (Display-Clickthrough)
   * `i` für eine Impression einer DSP Display-Anzeige (Durchsicht der Anzeige)
   * `s` für einen Klick auf eine Suchanzeige (Durchsuchen-Clickthrough).

Beispiel `EF `ID: WcmibgAAAHJK1RyY:1551968087687:d

>[!NOTE]
>
>Bei EF IDs wird zwischen Groß- und Kleinschreibung unterschieden. Wenn eine [!DNL Analytics] -Implementierung das URL-Tracking in Kleinbuchstaben erzwingt, erkennt Advertising Cloud die EF-ID nicht. Dies wirkt sich auf die Gebote und Berichterstellung von Advertising Cloud aus, hat jedoch keine Auswirkungen auf die Berichterstellung von Advertising Cloud innerhalb von [!DNL Analytics].

### Die EF ID-Dimension in [!DNL Analytics]

In [!DNL Analytics] -Berichten können Sie EF-ID-Daten finden, indem Sie nach der Dimension [!UICONTROL EF ID] suchen und die Metrik [!UICONTROL EF ID Instance] verwenden.

`EF IDs` unterliegen in Analysis Workspace der Grenze von 500.000 eindeutigen Kennungen. Sobald der Wert von 500.000 erreicht ist, werden alle neuen Trackingcodes unter dem einzeiligen Elementtitel &quot;[!UICONTROL Low Traffic]&quot;gemeldet. Da die Berichtstreue möglicherweise fehlt, sind die `EF IDs` nicht klassifiziert und sollten Sie sie nicht für Segmente oder Berichte in [!DNL Analytics] verwenden.

## Advertising Cloud AMO-IDs

Die AMO-ID verfolgt jede eindeutige Anzeigenkombination auf einer weniger detaillierten Ebene und wird für die [!DNL Analytics]-Datenklassifizierung und Erfassung von Werbedetriken (wie Impressionen, Klicks und Kosten) aus Advertising Cloud verwendet. Die AMO-ID wird in einer [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)- oder rVar-Dimension (AMO-ID) gespeichert und ausschließlich für die Berichterstellung in [!DNL Analytics] verwendet.

Die AMO-ID wird auch als `s_kwcid` bezeichnet, was manchmal auch als &quot;Kalmar&quot;bezeichnet wird.

### AMO-ID-Format für [!DNL DSP]

```<Channel ID>!<Ad ID>!<Placement ID>```

wobei:

* &lt;>Die Kanal-ID *> kann lauten:*

   * `AC` = Advertising Cloud DSP
   * `AL` für Advertising Cloud Search

* &lt;>Anzeigen-ID *> wird als eindeutige Kennung verwendet, die von Advertising Cloud für eine Anzeige generiert wurde.* Sie dient als Schlüssel für die Übersetzung von Advertising Cloud-Entitätsmetadaten in lesbare [!DNL Analytics]-Dimensionen.

* &lt;>Platzierungs-ID *> ist eine von Advertising Cloud generierte eindeutige Kennung für eine Platzierung.* Sie dient als Schlüssel für die Übersetzung von Advertising Cloud-Entitätsmetadaten in lesbare [!DNL Analytics]-Dimensionen.

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

AMO-IDs für [!DNL Search] weisen für jede Suchmaschine ein bestimmtes Format auf. Das Format für alle Suchmaschinen beginnt mit Folgendem:

```AL!{ef_userid}!{ef_sid}```

wobei:

* `AL` ist die Kanal-ID für den Suchkanal.
* `{ef_userid}` ist die eindeutige numerische Benutzer-ID, die Advertising Cloud dem Advertiser zuweist.
* `{ef_sid}` ist die numerische ID, die Advertising Cloud für die angegebene Suchmaschine verwendet, z. B.  `3` für  [!DNL Google Ads] oder  `10` für  [!DNL Microsoft Advertising].

Im Folgenden finden Sie die vollständigen AMO ID-Formate für einige Suchmaschinen. Wenden Sie sich bei AMO-ID-Formaten für andere Suchmaschinen an Ihren Adobe-Kundenbetreuer.

AMO-ID-Format für [!DNL Google Ads]:

```AL!{ef_userid}!{ef_sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}```

wobei:

* `{creative}` ist die  [!DNL Google Ads] eindeutige numerische ID für das Kreativelement.
* `{matchtype}` ist der Übereinstimmungstyp des Suchbegriffs, der die Anzeige ausgelöst hat:  `e` für exakt,  `p` für Wortgruppe oder  `b` für breit.
* `{placement}` ist der Domänenname der Website, auf der auf die Anzeige geklickt wurde. Ein Wert ist für Anzeigen in platzierungszielgerichteten Kampagnen und für Anzeigen in auf Suchbegriffe ausgerichteten Kampagnen verfügbar, die auf Inhalts-Sites angezeigt werden.
* `{network}` gibt das Netzwerk an, aus dem der Klick erfolgte:   `g` für die  [!DNL Google] Suche (nur für Anzeigen mit Keyword-Targeting),  `s` für einen Suchpartner (nur für Anzeigen mit Keyword-Targeting) oder  `d` für das Display-Netzwerk (für Anzeigen mit Keyword oder Platzierungszielgruppe).
* `{keyword}` ist entweder der spezifische Suchbegriff, der Ihre Anzeige ausgelöst hat (auf Suchseiten) oder der beste Suchbegriff (auf Inhalts-Sites).

AMO-ID-Format für [!DNL Microsoft Advertising]:

```AL!{ef_userid}!{ef_sid}!{AdId}!{OrderItemId}```

wobei:

* `{AdId}` ist die  [!DNL Microsoft Advertising] eindeutige numerische ID für das Kreativelement.
* `{OrderItemId}` ist die  [!DNL Microsoft Advertising] numerische ID für den Suchbegriff.

### AMO-ID-Dimension in [!DNL Analytics]

In Analytics-Berichten können Sie AMO-ID-Daten finden, indem Sie nach der Dimension [!UICONTROL AMO ID] suchen und die Metrik [!UICONTROL AMO ID Instance] verwenden. Die Dimension [!UICONTROL AMO ID] enthält alle erfassten AMO-ID-Werte, während die Metrik [!UICONTROL AMO ID Instance] angibt, wie oft ein AMO-ID-Wert von der Site erfasst wurde. Wenn beispielsweise dieselbe Suchanzeige viermal angeklickt wurde, Analytics jedoch sieben Site-Einträge verfolgt hat, wäre [!UICONTROL AMO ID Instance] sieben (7) und [!UICONTROL Clicks] vier (4).

Für alle Berichte oder Prüfungen innerhalb von [!DNL Analytics] ist es Best Practice, die AMO-ID zusammen mit der zugehörigen Instanz zu verwenden. Weitere Informationen finden Sie unter &quot;[Datenvalidierung für [!DNL Analytics for Advertising Cloud]](data-variances.md#data-validation)&quot;in &quot;Erwartete Datenabweichungen zwischen [!DNL Analytics] und Advertising Cloud&quot;.

## Informationen zu Analytics Classifications

In [!DNL Analytics] ist eine [Klassifizierung](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) ein Metadatenelement für einen bestimmten Trackingcode, z. B. Konto, Kampagne oder Anzeige. Advertising Cloud kategorisiert Advertising Cloud-Rohdaten mithilfe von Klassifizierungen, damit Sie die Daten beim Generieren von Berichten auf unterschiedliche Weise anzeigen können (z. B. nach Anzeigentyp oder Kampagne). Klassifizierungen bilden die Grundlage der Advertising Cloud-Berichterstellung in [!DNL Analytics] und können mit den AMO-Metriken wie [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions] und [!UICONTROL AMO Clicks] sowie mit benutzerspezifischen und standardmäßigen Onsite-Ereignissen wie [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders] und [!UICONTROL Revenue] verwendet werden.

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Erwartete Datenabweichungen  [!DNL Analytics] zwischen und Advertising Cloud](data-variances.md)

