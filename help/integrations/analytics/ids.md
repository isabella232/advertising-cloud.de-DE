---
title: Von [!DNL Analytics]
description: Von [!DNL Analytics]
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '1186'
ht-degree: 0%

---

# Von [!DNL Analytics]

*Werbetreibende mit nur einer Adobe Advertising-Adobe Analytics-Integration*

*Anwendbar auf Advertising DSP und[!DNL Advertising Search]*

Adobe Advertising verwendet zwei IDs für das On-site-Performance-Tracking: die *EF ID* und *AMO-ID*.

Wenn eine Ad-Impression auftritt, erstellt Adobe Advertising die AMO-ID- und EF-ID-Werte und speichert sie. Wenn ein Besucher, der eine Anzeige gesehen hat, auf die Site gelangt, ohne auf eine Anzeige zu klicken, [!DNL Analytics] ruft diese Werte aus der Adobe Advertising über die [!DNL Analytics for Advertising] JavaScript-Code. Für Durchsichts-Traffic: [!DNL Analytics] generiert eine zusätzliche ID (`SDID`), das zum Zuordnen der EF ID und AMO ID zu verwendet wird [!DNL Analytics]. Für Clickthrough-Traffic werden diese IDs mithilfe der `s_kwcid` und `ef_id` Abfragezeichenfolgenparameter.

Adobe Advertising unterscheidet mithilfe der folgenden Kriterien zwischen einem Clickthrough- oder Durchsichtseintrag auf der Website:

* Ein Durchsichtseintrag wird erfasst, wenn ein Benutzer die Site besucht, nachdem er eine Anzeige angesehen, aber nicht darauf geklickt hat. [!DNL Analytics] erfasst eine Durchsicht, wenn zwei Bedingungen erfüllt sind:
   * Der Besucher hat keine Clickthroughs für eine [!DNL DSP] oder [!DNL Search] Anzeige während der [Klick-Lookback-Fenster](#lookback-a4adc).
   * Der Besucher hat mindestens eine [!DNL DSP] Anzeige während der [Impression-Lookback-Fenster](#lookback-a4adc). Die letzte Impression wird als Durchsicht übergeben.
* Ein Clickthrough-Eintrag wird erfasst, wenn ein Site-Besucher auf eine Anzeige klickt, bevor er die Site betritt. [!DNL Analytics] erfasst einen Clickthrough, wenn eine der folgenden Bedingungen eintritt:
   * Die URL enthält eine EF ID und eine AMO ID, die von Adobe Advertising zur Landingpage-URL hinzugefügt wurden.
   * Die URL enthält keine Trackingcodes, aber der JavaScript-Code für Adobe Advertising erkennt einen Klick innerhalb der letzten zwei Minuten.

![Adobe Advertising-Ansicht-basiert [!DNL Analytics] Integration](/help/integrations/assets/a4adc-view-through-process.png)

*Abbildung 1: Adobe Advertising-Ansicht-basiert [!DNL Analytics] Integration*

![Adobe Advertising-Klick-URL-basiert [!DNL Analytics] Integration](/help/integrations/assets/a4adc-click-through-process.png)

*Abbildung 2: Adobe Advertising-Klick-URL-basiert [!DNL Analytics] Integration*

## Adobe Advertising EF IDs

Die EF ID ist ein eindeutiges Token, mit dem Adobe Advertising Aktivitäten mit einem Online-Klick oder einer Anzeige in Verbindung setzt. Die EF ID wird in einer [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) oder die rVar-Dimension (reservierte eVar) (Adobe Advertising EF ID) und verfolgt jeden Anzeigenklick oder jede Anzeige auf der Browser- oder Geräteebene. EF-IDs dienen hauptsächlich als Schlüssel zum Senden [!DNL Analytics] Daten an Adobe Advertising zur Berichterstellung und Angebotsoptimierung in Adobe Advertising.

### EF ID Format

>[!NOTE]
>
>Bei EF IDs wird zwischen Groß- und Kleinschreibung unterschieden. Wenn eine [!DNL Analytics] -Implementierung erzwingt das URL-Tracking in Kleinbuchstaben. Dann erkennt Adobe Advertising die EF-ID nicht. Dies wirkt sich auf das Gebot und die Berichterstellung für Adobe Advertising aus, hat jedoch keine Auswirkungen auf die Berichterstellung für Adobe Advertising innerhalb von [!DNL Analytics].

#### [!DNL Google Ads] Suchanzeigen

```{gclid}:G:s```

wobei:

* `gclid` ist die [!DNL Google Click ID] (GCLID).
* `s` ist der Netzwerktyp (&quot;s&quot; für die Suche).

#### Microsoft Advertising-Suchanzeigen

```{msclkid}:G:s```

wobei:

* `msclkid` ist die [!DNL Microsoft Click ID] (MSCLKID).
* `s` ist der Netzwerktyp (&quot;s&quot; für die Suche).

#### Anzeigen und Suchanzeigen in anderen Suchmaschinen

```<Adobe Advertising visitor ID>:<timestamp>:<channel type>```

wobei:

* &lt;*Adobe Advertising-Besucher-ID*> ist eine eindeutige ID pro Besucher (z. B. &quot;ÄhKVaAAABCkJ0mDt&quot;). Auch als *Surfer-ID*.

* &lt;*timestamp*> ist die Zeit im Format JJJJMMTDDHHMMSS (z. B. 20190821192533 für Jahr 2019, Monat 08, Tag 21, Zeit 19).:25:33).

* &lt;*Kanaltyp*> ist der Kanaltyp, der für den Klick oder die Belichtung verantwortlich ist:

   * `d` für einen Klick auf eine DSP Display-Anzeige (Display-Clickthrough)
   * `i` für eine Impression einer DSP Display-Anzeige (Durchsicht der Anzeige)
   * `s` für einen Klick auf eine Suchanzeige (Durchsuchen-Clickthrough).

Beispiel `EF `ID: WcmibgAAAHJK1RyY:1551968087687:d

### Die EF ID-Dimension in [!DNL Analytics]

In [!DNL Analytics] Berichte, können Sie EF ID-Daten finden, indem Sie nach der [!UICONTROL EF ID] Dimension und unter Verwendung der [!UICONTROL EF ID Instance] Metrik.

EF-IDs unterliegen in Analysis Workspace der Grenze von 500.000 eindeutigen Kennungen. Sobald der Wert von 500.000 erreicht ist, werden alle neuen Trackingcodes unter dem einzeiligen Elementtitel gemeldet.[!UICONTROL Low Traffic].&quot; Da die Möglichkeit besteht, dass die Berichtstreue fehlt, werden die EF-IDs nicht klassifiziert und sollten Sie sie nicht für Segmente oder Berichte in [!DNL Analytics].

## Adobe Advertising AMO-IDs

Die AMO-ID verfolgt jede eindeutige Anzeigenkombination auf einer weniger detaillierten Ebene und wird für [!DNL Analytics] Datenklassifizierung und Erfassung von Werbemetriken (wie Impressionen, Klicks und Kosten) aus Adobe Advertising. Die AMO-ID wird in einer [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) oder rVar-Dimension (AMO-ID) und wird ausschließlich für die Berichterstellung in [!DNL Analytics].

Die AMO-ID wird auch als `s_kwcid`, der manchmal als &quot;[!DNL the squid].&quot;

### AMO-ID-Format für [!DNL DSP]

```<Channel ID>!<Ad ID>!<Placement ID>```

wobei:

* &lt;*Kanal-ID*> kann sein:

   * `AC` = DSP
   * `AL` für [!DNL Advertising Search]

* &lt;*Anzeigen-ID*> wird eine durch Werbung generierte eindeutige Adobe für eine Anzeige verwendet. Sie dient als Schlüssel für die Übersetzung von Adobe Advertising-Entitätsmetadaten in lesbare [!DNL Analytics] Dimensionen.

* &lt;*Platzierungs-ID*> ist eine Adobe Advertising-generierte eindeutige Kennung für eine Platzierung. Sie dient als Schlüssel für die Übersetzung von Adobe Advertising-Entitätsmetadaten in lesbare [!DNL Analytics] Dimensionen.

Beispiel einer AMO-ID: AC!iIMvXqlOa6Nia2lDvtgw!GrVv6o2oV2qQLjQiXLC7

### AMO-ID-Format für [!DNL Search]

AMO-IDs für [!DNL Search] für jede Suchmaschine ein bestimmtes Format verwenden. Das Format für alle Suchmaschinen beginnt mit Folgendem:

```AL!{userid}!{sid}```

wobei:

* `AL` ist die Kanal-ID für das Anzeigennetzwerk.
* `{userid}` ist die eindeutige numerische Benutzer-ID, die Adobe Advertising dem Advertiser zuweist.
* `{sid}` ist die numerische ID, die Adobe Advertising für das angegebene Werbenetzwerk verwendet, z. B. `3` für [!DNL Google Ads] oder `10` für [!DNL Microsoft Advertising].

Im Folgenden finden Sie die vollständigen AMO ID-Formate für einige Werbenetzwerke. Wenden Sie sich bei AMO-ID-Formaten für andere Werbenetzwerke an Ihren [!DNL Adobe] Account-Team.

AMO-ID-Format für [!DNL Google Ads]:

```AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}```

wobei:

* `{creative}` ist die [!DNL Google Ads] eindeutige numerische ID für das Kreativelement.
* `{matchtype}` ist der Übereinstimmungstyp des Suchbegriffs, der die Anzeige ausgelöst hat: `e` exakt, `p` für Wortgruppe oder `b` für einen breiten Bereich.
* `{placement}` ist der Domänenname der Website, auf der auf die Anzeige geklickt wurde. Ein Wert ist für Anzeigen in platzierungszielgerichteten Kampagnen und für Anzeigen in auf Suchbegriffe ausgerichteten Kampagnen verfügbar, die auf Inhalts-Sites angezeigt werden.
* `{network}` gibt das Netzwerk an, aus dem der Klick erfolgte:  `g` für [!DNL Google] Suche (nur für Anzeigen mit Keyword-Targeting), `s` für einen Suchpartner (nur für Anzeigen mit Keyword-Targeting) oder `d` für das Display-Netzwerk (für Anzeigen mit Keyword oder Platzierungszielgruppe).
* `{keyword}` ist entweder der spezifische Suchbegriff, der Ihre Anzeige ausgelöst hat (auf Suchseiten) oder der beste Suchbegriff (auf Inhalts-Sites).

AMO-ID-Format für [!DNL Microsoft Advertising]:

```AL!{userid}!{sid}!{AdId}!{OrderItemId}```

wobei:

* `{AdId}` ist die [!DNL Microsoft Advertising] eindeutige numerische ID für das Kreativelement.
* `{OrderItemId}` ist die [!DNL Microsoft Advertising] numerische ID für den Suchbegriff.

### AMO-ID-Dimension in [!DNL Analytics]

In Analytics-Berichten können Sie AMO-ID-Daten finden, indem Sie nach der [!UICONTROL AMO ID] Dimension und unter Verwendung der [!UICONTROL AMO ID Instance] Metrik. Die [!UICONTROL AMO ID] -Dimension enthält alle erfassten AMO-ID-Werte, während die [!UICONTROL AMO ID Instance] gibt an, wie oft ein AMO-ID-Wert von der Site erfasst wurde. Wenn beispielsweise dieselbe Suchanzeige viermal angeklickt wurde, Analytics jedoch sieben Site-Einträge verfolgt hat, wird [!UICONTROL AMO ID Instance] wäre sieben (7) und [!UICONTROL Clicks] wäre vier (4).

Für alle Berichte oder Prüfungen innerhalb von [!DNL Analytics]Best Practice ist, die AMO-ID zusammen mit der entsprechenden Instanz zu verwenden. Weitere Informationen finden Sie unter &quot;[Datenvalidierung für [!DNL Analytics for Advertising]](data-variances.md#data-validation)&quot;in &quot;Erwartete Datenabweichungen zwischen [!DNL Analytics] und Adobe Advertising.&quot;

## Informationen zu Analytics Classifications

In [!DNL Analytics], [Classification](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) ist ein Metadatenelement für einen bestimmten Trackingcode, z. B. Konto, Kampagne oder Anzeige. Adobe Advertising kategorisiert Werbedaten zu Rohdaten für Adoben mithilfe von Klassifizierungen, damit Sie die Daten beim Generieren von Berichten auf unterschiedliche Weise anzeigen können (z. B. nach Anzeigentyp oder Kampagnen). Klassifizierungen bilden die Grundlage für Adobe Advertising Reporting in [!DNL Analytics] und kann mit den AMO-Metriken verwendet werden, z. B. [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions]und [!UICONTROL AMO Clicks]sowie mit benutzerspezifischen und standardmäßigen On-site-Ereignissen wie [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders]und [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising]](overview.md)
>* [Erwartete Datenabweichungen zwischen [!DNL Analytics] und Adobe Advertising](data-variances.md)

