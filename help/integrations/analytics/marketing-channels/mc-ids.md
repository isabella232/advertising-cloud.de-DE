---
title: Erstellen von Adobe Advertising-IDs mit [!DNL Marketing Channels] Regeln
description: Erfahren Sie, wie Sie mit Adobe Advertising IDs Verarbeitungsregeln für [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 0%

---

# Erstellen von Adobe Advertising-IDs mit [!DNL Marketing Channels] Verarbeitungsregeln

*Werbetreibende mit nur einer Adobe Advertising-Adobe Analytics-Integration*

Sie können Adobe Advertising IDs ([AMO-ID und EF ID](../ids.md)) zum Konfigurieren [!DNL Marketing Channels] Verarbeitungsregeln in Adobe Analytics. Verwenden Sie Adobe Advertising IDs für Regeln, die für Ihre Adobe Advertising-Kampagnen spezifisch sind.

## AMO-ID in Verarbeitungsregeln

Die AMO-ID ist der primäre Trackingcode, mit dem Adobe Advertising-Daten in [!DNL Analytics]. Die AMO-ID ist eine Verkettung von dynamischen Werten, die von Adobe verwaltet werden, um eine detaillierte Berichterstellung innerhalb von [!DNL Analytics]. Sie wird in einer [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) oder rVar-Dimension (AMO-ID). Die AMO-ID kann in [!DNL Analytics] auf zwei Arten:

* Clickthrough-Tracking: Adobe Advertising setzt die `s_kwcid` Abfragezeichenfolgenparameter in einem Link und [!DNL Analytics] Ruft den Parameter aus der Landingpage-URL ab, wenn ein Clickthrough erfolgt.
* Durchsichts-Tracking ([!DNL DSP] Nur): Der letzte Ereignisdienst erkennt eine Durchsicht auf der Serverseite und sendet die AMO-ID an [!DNL Analytics]. In diesem Fall enthält die URL keine `s_kwcid` Parameter.

Die dynamischen Werte in AMO-IDs geben den verfolgten Marketing-Kanal an:

* Das Präfix in der AMO-ID kann verwendet werden, um den Kanal der obersten Ebene innerhalb von [!DNL Marketing Channels].

* Zeichensätze im Hauptteil der AMO-ID weisen auf einen spezifischeren Kampagnentyp hin.

* Das Suffix &quot;vt&quot;ist vorhanden für [!DNL DSP] Durchsichts-Traffic und kann verwendet werden, um separate Clickthrough- und Durchsichtsaktionen zu erstellen. [!DNL DSP] Kanäle.

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

Die [!DNL Marketing Channels] Verarbeitungsregel für [!UICONTROL Paid Search] -Kanal könnte wie folgt aussehen:

![Beispiel einer [!UICONTROL Paid Search] Regel](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

Die [!DNL Marketing Channels] Verarbeitungsregel für [!UICONTROL YouTube Video Ads] -Kanal könnte wie folgt aussehen:

![Beispiel einer [!UICONTROL YouTube Video Ads] Regel](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> Stellen Sie sicher, dass Sie Ihre Regeln in der richtigen Reihenfolge ausführen. Wenn die beiden oben genannten Regeln in der richtigen Reihenfolge ausgeführt wurden, wird die [!DNL YouTube] Videoanzeigen-Traffic würde alle unter [!UICONTROL Paid Search] -Kanal, da die AMO-ID beide mit &quot;AL!&quot;beginnt. und enthalten &quot;!ytv!&quot;.

## Die EF ID in den Verarbeitungsregeln

Die AMO EF ID (EF ID) ist der zweite Trackingcode, der im [!DNL Analytics for Advertising] Integration. Ihr Hauptzweck besteht darin, zu verfolgen und weiterzugeben [!DNL Analytics] Ereignisdaten in die Adobe Advertising. Jedes Mal, wenn ein Clickthrough oder eine Durchsicht erfolgt, wird eine eindeutige EF-ID generiert, auch wenn es sich um genau dieselbe Anzeige für denselben Besucher handelt. Die EF ID wird nicht in der [!DNL Analytics] Reporting-Benutzeroberfläche, da sie in der Regel die Grenze von 500.000 individuellen Werten pro Variable in [!DNL Analytics], wodurch sie für Berichte unbrauchbar wird. Die Adobe Advertising-Metriken und -Metadaten werden nicht auf die EF ID angewendet. werden nur auf die AMO-ID angewendet. Die zusätzliche Granularität des Trackings ist für die Kampagnenoptimierung in der Adobe Advertising erforderlich, sodass beide IDs erforderlich sind.

Obwohl die EF ID-Dimension nicht direkt in verwendet wird [!DNL Analytics] Berichterstellung verwenden, kann die EF ID bei der Erstellung von Marketingkanälen hilfreich sein. Das EF ID-Suffix zeigt den Kanal (Anzeige oder Suche) an und ob der Besuch durch einen Clickthrough oder eine Durchsicht gesteuert wurde. Das Trennzeichen in der EF ID ist ein Doppelpunkt und nicht der Ausrufezeichen in der AMO-ID.

| EF ID Suffix | Kanal |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### Beispiele für Verarbeitungsregeln, die die EF ID verwenden

#### Clickthrough-Regel anzeigen

Erstellen Sie einen Display-Clickthrough-Marketing-Kanal, indem Sie nur Clickthroughs erfassen. Da die AMO-ID für Clickthroughs und Durchsichten gleich ist, verwendet diese Regel die EF ID-Variable und die `ef_id` Abfragezeichenfolgen-Parameter.

Manchmal werden Clickthroughs über die URL verfolgt (Standard). In anderen Fällen werden Clickthroughs über den letzten Ereignisdienst auf der Serverseite verfolgt, weshalb die URL nicht die Variable `ef_id` Parameter. Die Regel sucht daher nach Bedingungen, unter denen die EF ID-Variable oder die `ef_id` -Abfragezeichenfolgenparameter endet mit &quot;:d&quot;. Verwenden Sie die`Any`&quot;, da diese Regel für beide Bedingungen ausgelöst werden soll.

![Beispiel einer Display-Clickthrough-Regel](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### Durchsichtsregel anzeigen

Um einen Durchsichtskanal für die Anzeige zu erstellen, erstellen Sie eine Regel, in der die EF-ID mit &quot;:i&quot;endet. Da der Besucher nicht auf die Anzeige geklickt hat, enthält das Durchsichts-Tracking nicht die `ef_id` oder `s_kwcid` in der URL, sodass die Regel nur eine Bedingung erfordert.

![Beispiel einer Durchsichtsregel für die Anzeige](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [Grundlagen [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Warum können Kanaldaten zwischen Adobe Advertising und [!DNL Marketing Channels]](mc-data-variances.md)
>* [Verwenden [!DNL Analytics Marketing Channels] mit Adobe Advertising-Daten](mc-ac-data.md)
>* [Video: Verwenden [!DNL Marketing Channels] für Adobe Advertising Reporting](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Von [!DNL Analytics]](/help/integrations/analytics/ids.md)

