---
title: Grundlagen [!DNL Marketing Channels]
description: Wichtige Informationen [!DNL Analytics Marketing Channels] that [!DNL Analytics for Advertising Cloud] -Benutzer sollten dies verstehen.
feature: Integration with Adobe Analytics
source-git-commit: 1ae45d0ceee2efc4fc52b86fd6737d4c7467a6ca
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# Grundlagen [!DNL Analytics Marketing Channels]

*Werbetreibende, die nur über eine Advertising Cloud-Adobe Analytics-Integration verfügen*

Auf dieser Seite werden wichtige Informationen zu [!DNL Analytics Marketing Channels] dass [!DNL Analytics for Advertising Cloud] -Benutzer müssen dies verstehen.

Vollständige Dokumentation zu [!DNL Marketing Channels], siehe[Erste Schritte mit [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html).&quot;

## Übersicht über [!DNL Marketing Channels]

[!DNL Marketing Channels] sind eine wichtige Funktion von Adobe Analytics. [!DNL Marketing Channels] Berichte zeigen an, wie Kunden über das Berichtsfenster zu Ihrer Website gelangen und wie sich die einzelnen Kanäle auf den Umsatz oder das Verhalten auf der Site auswirken.

Betrachten Sie das folgende Beispiel einer besuchsübergreifenden Journey. Jeder Besuch Ihrer Website wird durch den Marketingkanal gekennzeichnet, von dem aus der Besucher eingestiegen ist. Der erste Besuch, der auch als Erstkontaktkanal bezeichnet wird, ist E-Mail. Die Anzeige bei Besuch 2 ist ein teilnehmender Kanal und die kostenlose Suche gilt als Letztkontakt-Kanal. Wenn Sie [!UICONTROL Last Touch Attribution] Innerhalb [!UICONTROL Attribution IQ], würde die kostenlose Suche die volle Gutschrift für das Konversionsereignis von 250 USD erhalten. Mithilfe des Experience Cloud-ID-Diensts können Sie diese individuellen Besuche miteinander verknüpfen, um eine Journey durch einen einzelnen Besucher anzuzeigen.

![Beispiel für besuchsübergreifende Konversions-Journey in Marketingkanälen](/help/integrations/assets/a4adc-mc-sample-journey.png)

Durch Verwendung von [!UICONTROL Marketing Channels] Verarbeitungsregeln können Sie logische Gruppen erstellen, um die Kanäle zu bestimmen, die den Traffic fördern, und jeden Kanal zu verfolgen, wenn Benutzer zu Ihrer Site gelangen. Beispiel: die [!UICONTROL Email] -Kanal wird durch einen eindeutigen Trackingcode angezeigt, der beim Klick generiert wird und bei der Anmeldung durch Adobe Analytics den Besuch als Besucher einer E-Mail-Marketing-Kampagne kategorisiert.

## Verarbeitungsregeln und Festlegen von Marketingkanälen

Jedes Mal, wenn ein Benutzer auf eine Website gelangt, erfolgt dies über eine URL, auf die er klickt oder die er direkt in die Adressleiste eingegeben hat. Wenn der Benutzer die Website aufruft, [!DNL Analytics] verfolgt Informationen, die verwendet werden können, um den Kanal zu ermitteln, der den Besuch verursacht hat.

Häufig hängen Marketer Abfragezeichenfolgen-Parameter-Trackingcodes an Kanal-URLs an, um die Auswirkungen des Kanals auf ihre Site zu verfolgen. Sie können [!DNL Marketing Channels] Verarbeitungsregeln, um auf bestimmte Tracking-Parameter und Werte zu warten und den Kanal ohne zusätzliches Tracking zu bestimmen. Wenn beispielsweise alle E-Mail-Kampagnen-URLs dem Format `www.adobe.com?cid=email…` (wobei die URL den Abfragezeichenfolgenparameter und den Wert enthält) `cid=email`), können Sie eine Regel erstellen, die auf diesen Trackingcode überwacht und den Besuch im [!UICONTROL Email] -Kanal.

Andere Kanäle verfügen nicht über verfolgbare URL-Pfade und benötigen weitere Logik zur Identifizierung. Beispiel: [!UICONTROL Earned Social], bei dem ein Benutzer auf einen Link klickt, den ein anderer Benutzer organisch in einem sozialen Netzwerk freigegeben hat, ist ein wichtiger zu verfolgender Kanal. Der Marketing-Experte hat jedoch keine Möglichkeit, einen Trackingcode für Abfragezeichenfolgen-Parameter an die freigegebene URL anzuhängen. In diesem Fall können Sie eine Verarbeitungsregel erstellen, um die Referrer-Domäne von sozialen Netzwerken von Interesse und das Fehlen von gebührenpflichtigen Trackingcodes zu überwachen und den Kanal zu bestimmen. Die Besuche, die diese Anforderungen erfüllen, werden dann im Marketingkanalbericht als Earned Social nachverfolgt.

Adobe empfiehlt, mit Ihrem Analyseteam zusammenzuarbeiten, um einen umfassenden Satz von [!DNL Marketing Channels] Verarbeitungsregeln zur Verfolgung aller für Ihr Unternehmen relevanten Kanäle. Auf diese Weise können Sie leistungsstarke Attributionsberichte erstellen.

Informationen dazu, wie Advertising Cloud zu den Signalen beitragen kann, die zum Erstellen benutzerdefinierter Marketing-Kanäle erforderlich sind, finden Sie unter &quot;[Erstellen von Advertising-IDs mit [!DNL Marketing Channels] Regeln](mc-ids.md).&quot;

>[!MORELIKETHIS]
>
>* [Erstellen von Advertising Cloud-IDs mithilfe [!DNL Marketing Channels] Verarbeitungsregeln](mc-ids.md)
>* [Warum Kanaldaten zwischen Advertising Cloud und variieren können [!DNL Marketing Channels]](mc-data-variances.md)
>* [Verwenden [!DNL Analytics Marketing Channels] mit Advertising Cloud-Daten](mc-ac-data.md)
>* [Video: Reporting mit Advertising Cloud [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Übersicht über [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/overview.md)

