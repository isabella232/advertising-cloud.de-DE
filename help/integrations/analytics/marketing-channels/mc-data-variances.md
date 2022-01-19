---
title: Warum Kanaldaten zwischen Advertising Cloud und variieren können [!DNL Marketing Channels]
description: Erfahren Sie, warum sich die von der AMO-ID verfolgten Kanaldaten von den von [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: 4605dc7d-43d7-414f-a509-6096c6cf5fd2
source-git-commit: b99d0ce78dc2adc16e555ef618393ef2fc11067d
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Warum Kanaldaten zwischen Advertising Cloud und variieren können [!DNL Marketing Channels]

*Werbetreibende, die nur über eine Advertising Cloud-Adobe Analytics-Integration verfügen*

Eine häufig gestellte Frage von Benutzern, die über die Integration der Advertising Cloud und [!DNL Marketing Channels] -Datensätze lautet &quot;Wodurch wird die Datenabweichung zwischen der AMO-ID und [!DNL Marketing Channels]?&quot; Oder manchmal: &quot;Warum sind die Daten kaputt? Ich benötige, dass alle Metriken in allen Berichten übereinstimmen.&quot; Glücklicherweise zeigen Diskrepanzen nicht an, dass die Daten &quot;beschädigt&quot;sind, und Diskrepanzen werden erwartet und sogar gewünscht. Sehen wir uns an, warum die Integration auf diese Weise entworfen wurde.

Die beiden Datensätze weisen unterschiedliche Hauptanwendungsfälle auf:

* [!DNL Marketing Channels]: Der primäre Anwendungsfall für [!DNL Marketing Channels] ist der Vergleich von Daten über mehrere Kanäle mit einem gemeinsamen Attributionsmodell. Analysten können [!UICONTROL Marketing Channel] -Dimension zu erhalten, um bessere Einblicke in die Interaktion zwischen Kanälen zu erhalten. Diese Einblicke können dazu beitragen, Entscheidungen auf Makroebene darüber zu treffen, wie in die einzelnen Kanäle investiert werden soll, und können zu Einblicken darüber führen, wie Besucher aus den einzelnen Kanälen mit der Website interagieren.

   Die [!DNL Analytics] [!UICONTROL Marketing Channel] -Dimension konfiguriert ist, um alle Kanäle zu erfassen und zu verfolgen. [!DNL Marketing Channels] kann auch so konfiguriert werden, dass Advertising Cloud DSP-Durchsichten und Clickthroughs erfasst werden. Dies geschieht in Bezug auf die anderen Marketingkanäle.

* Advertising Cloud AMO ID: Der primäre Anwendungsfall der Advertising Cloud AMO ID-Daten besteht darin, die erweiterten Funktionen von Advertising Cloud zu nutzen [!DNL Adobe Sensei]-gestützte Angebotsalgorithmen. Die Algorithmen treffen automatisch Tausende von Angebotsentscheidungen auf Mikroebene, die täglich getroffen werden, um die Werbeausgaben zu maximieren und die Ziele der [!DNL DSP] Kampagne oder [!DNL Search] Portfolio. Je mehr Konversionsdaten die Algorithmen mit Kampagnen verbinden können, desto besser können die Algorithmen diese Angebotsentscheidungen treffen.

   Um diese Daten zu erfassen, muss die Variable [!DNL Analytics for Advertising Cloud] Bei der Integration werden unbearbeitete AMO-IDs übergeben, die als Clickthrough- und Durchsichts-Trackingcodes in der AMO-ID-Dimension von Adobe Analytics übersetzt werden können. Diese kann entweder als benutzerdefinierte Variable (eVar) oder als reservierte Variable (rVar) gespeichert werden. Clickthroughs für andere Kanäle werden nicht in der AMO-ID-Dimension festgelegt, sodass die AMO-ID-Dimension die Eingabe aus diesen anderen Kanälen nicht verfolgen kann. Das Ergebnis ist, dass die AMO-ID beibehalten wird. [!DNL Marketing Channels] Einstiegspunkte.

Weitere Informationen zu möglichen Datenabweichungen zwischen Advertising Cloud-verfolgten Daten und [!DNL Analytics]-getrackte Daten, siehe[Erwartete Datenabweichungen zwischen [!DNL Analytics] und Advertising Cloud](../data-variances.md).&quot;

>[!MORELIKETHIS]
>
>* [Erwartete Datenabweichungen zwischen [!DNL Analytics] und Advertising Cloud](/help/integrations/analytics/data-variances.md)
>* [Grundlagen [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Erstellen von Advertising Cloud-IDs mithilfe [!DNL Marketing Channels] Verarbeitungsregeln](mc-ids.md)
>* [Verwenden [!DNL Analytics Marketing Channels] mit Advertising Cloud-Daten](mc-ac-data.md)
>* [Video: Reporting mit Advertising Cloud [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)

