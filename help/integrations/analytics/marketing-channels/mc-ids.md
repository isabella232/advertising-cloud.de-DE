---
title: Verwenden von Advertising Cloud IDs zum Erstellen [!DNL Marketing Channels] Regeln
description: Erfahren Sie, wie Sie mit Advertising Cloud IDs Verarbeitungsregeln für  [!DNL Analytics Marketing Channels] erstellen.
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 5224d891d665b901d076ff6a203e9ff3bab80f85
workflow-type: tm+mt
source-wordcount: '766'
ht-degree: 0%

---

# Verwenden von Advertising Cloud IDs zum Erstellen von [!DNL Marketing Channels] Verarbeitungsregeln

*Werbetreibende, die nur über eine Advertising Cloud-Adobe Analytics-Integration verfügen*

Sie können Advertising Cloud IDs ([AMO ID und EF ID](../ids.md)) verwenden, um [!DNL Marketing Channels] Verarbeitungsregeln in Adobe Analytics zu konfigurieren. Verwenden Sie Advertising Cloud IDs für Regeln, die für Ihre Advertising Cloud-Kampagnen spezifisch sind.

## AMO-ID in Verarbeitungsregeln

Die AMO-ID ist der primäre Trackingcode für die Meldung von Advertising Cloud-Daten innerhalb von [!DNL Analytics]. Die AMO-ID ist eine Verkettung von dynamischen Werten, die von Adobe verwaltet werden, um innerhalb von [!DNL Analytics] granulare Berichte bereitzustellen. Sie wird in einer [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html)- oder rVar-Dimension (AMO-ID) gespeichert. Die AMO-ID kann auf zwei Arten in [!DNL Analytics] festgelegt werden:

* Clickthrough-Tracking: Advertising Cloud legt den Abfragezeichenfolgenparameter `s_kwcid` in einem Link fest und [!DNL Analytics] übernimmt den Parameter aus der Landingpage-URL, wenn ein Clickthrough erfolgt.
* Durchsichtsverfolgung ([!DNL DSP] nur): Der letzte Ereignisdienst erkennt eine Durchsicht auf der Serverseite und sendet die AMO-ID an [!DNL Analytics]. In diesem Fall enthält die URL keinen Parameter `s_kwcid`.

Die dynamischen Werte in AMO-IDs geben den verfolgten Marketing-Kanal an:

* Das Präfix in der AMO-ID kann verwendet werden, um den Kanal der obersten Ebene innerhalb von [!DNL Marketing Channels] zu identifizieren.

* Zeichensätze im Hauptteil der AMO-ID weisen auf einen spezifischeren Kampagnentyp hin.

* Das Suffix &quot;vt&quot;ist für [!DNL DSP] Durchsichts-Traffic vorhanden und kann zum Erstellen separater Clickthrough- und Durchsichtskanäle [!DNL DSP] verwendet werden.

Der Rest der AMO-ID kann ignoriert werden.

| AMO-ID | Kanal | Regellogik |
|--------|---------|--------------------|
| AL! (Präfix) | [!UICONTROL Paid Search] | Beginnt mit |
| AC! (Präfix) | [!UICONTROL DSP] | Beginnt mit |
| !g! (body) | [!UICONTROL Google Search] | Enthält |
| !s! (body) | [!UICONTROL Search Partner] | Enthält |
| !d! (body) | [!UICONTROL Display Network] | Enthält |
| !u! (body) | [!UICONTROL Smart Shopping Campaign] | Enthält |
| !ytv! (body) | [!UICONTROL YouTube Video Ad] | Enthält |
| !yts! (body) | [!UICONTROL YouTube Search Ad] | Enthält |
| !vp! (body) | [!UICONTROL Google Video Partners] | Enthält |
| !vt (Suffix) | [!UICONTROL DSP View-through] | Endet in |

### Beispiele für Verarbeitungsregeln, die die AMO-ID verwenden

Die [!DNL Marketing Channels]-Verarbeitungsregel für den Kanal [!UICONTROL Paid Search] könnte wie folgt aussehen:

![Beispiel einer  [!UICONTROL Paid Search] Regel](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

Die [!DNL Marketing Channels]-Verarbeitungsregel für den Kanal [!UICONTROL YouTube Video Ads] könnte wie folgt aussehen:

![Beispiel einer  [!UICONTROL YouTube Video Ads] Regel](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Stellen Sie sicher, dass Sie Ihre Regeln in der richtigen Reihenfolge ausführen. Wenn die beiden oben genannten Regeln in der richtigen Reihenfolge ausgeführt werden, würde der [!DNL YouTube]-Videoanzeigen-Traffic alle unter den Kanal [!UICONTROL Paid Search] fallen, da die AMO-ID beide mit &quot;AL!&quot;beginnt. und enthalten &quot;!ytv!&quot;.

## Die EF ID in den Verarbeitungsregeln

Die AMO EF ID (EF ID) ist der zweite Trackingcode, der in der [!DNL Analytics for Advertising Cloud] -Integration verwendet wird. Ihr Hauptzweck besteht darin, [!DNL Analytics]-Ereignisdaten zu verfolgen und an Advertising Cloud weiterzugeben. Jedes Mal, wenn ein Clickthrough oder eine Durchsicht erfolgt, wird eine eindeutige EF-ID generiert, auch wenn es sich um genau dieselbe Anzeige für denselben Besucher handelt. Die EF ID wird in der [!DNL Analytics] -Berichterstellungsbenutzeroberfläche nicht verwendet, da sie in der Regel die 500.000 individuellen Werte pro Variablenbegrenzung in [!DNL Analytics] überschreitet, wodurch sie für die Berichterstellung unbrauchbar wird. Die Advertising Cloud-Metriken und -Metadaten werden nicht auf die EF ID angewendet. werden nur auf die AMO-ID angewendet. Die zusätzliche Granularität des Trackings ist für die Kampagnenoptimierung in Advertising Cloud erforderlich, sodass beide IDs erforderlich sind.

Obwohl die EF ID-Dimension nicht direkt in [!DNL Analytics] -Berichten verwendet wird, kann die EF ID bei der Erstellung von Marketing-Kanälen hilfreich sein. Das EF ID-Suffix zeigt den Kanal (Anzeige oder Suche) an und ob der Besuch durch einen Clickthrough oder eine Durchsicht gesteuert wurde. Das Trennzeichen in der EF ID ist ein Doppelpunkt und nicht der Ausrufezeichen in der AMO-ID.

| EF ID Suffix | Kanal |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Beispiele für Verarbeitungsregeln, die die EF ID verwenden

#### Clickthrough-Regel anzeigen

Erstellen Sie einen Display-Clickthrough-Marketing-Kanal, indem Sie nur Clickthroughs erfassen. Da die AMO-ID für Clickthroughs und Durchsichten gleich ist, verwendet diese Regel die EF ID-Variable und den `ef_id`-Abfragezeichenfolgenparameter.

Manchmal werden Clickthroughs über die URL verfolgt (Standard). In anderen Fällen werden Clickthroughs über den letzten Ereignisdienst auf der Serverseite verfolgt, weshalb die URL den Parameter `ef_id` nicht enthält. Die Regel sucht daher nach Bedingungen, in denen die EF ID-Variable oder der `ef_id`-Abfragezeichenfolgenparameter mit &quot;:d&quot;endet. Verwenden Sie den Operator &quot;`Any`&quot;, da diese Regel für beide Bedingungen ausgelöst werden soll.

![Beispiel einer Display-Clickthrough-Regel](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Durchsichtsregel anzeigen

Um einen Durchsichtskanal für die Anzeige zu erstellen, erstellen Sie eine Regel, in der die EF-ID mit &quot;:i&quot;endet. Da der Besucher nicht auf die Anzeige geklickt hat, enthält das Durchsichts-Tracking nicht die Zeichen `ef_id` oder `s_kwcid` in der URL. Daher ist nur eine Bedingung erforderlich.

![Beispiel einer Durchsichtsregel für die Anzeige](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [Grundlagen [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Warum Kanaldaten zwischen Advertising Cloud und variieren können [!DNL Marketing Channels]](mc-data-variances.md)
>* [ [!DNL Analytics Marketing Channels] Verwenden mit Advertising Cloud-Daten](mc-ac-data.md)
>* [Video: Reporting mit Advertising Cloud [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Von verwendete Advertising Cloud IDs [!DNL Analytics]](/help/integrations/analytics/ids.md)

