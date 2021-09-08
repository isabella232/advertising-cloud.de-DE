---
title: Warum können Kanaldaten zwischen Advertising Cloud und [!DNL Marketing Channels] variieren
description: Erfahren Sie, warum die von der AMO-ID verfolgten Kanaldaten von den von [!DNL Analytics Marketing Channels] verfolgten Kanaldaten variieren können.
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Warum können Kanaldaten zwischen Advertising Cloud und [!DNL Marketing Channels] variieren

*Werbetreibende, die nur über eine Advertising Cloud-Adobe Analytics-Integration verfügen*

Eine häufig gestellte Frage von Benutzern, die über die Integration der Advertising Cloud- und [!DNL Marketing Channels]-Datensätze lernen, lautet: &quot;Was verursacht die Datenabweichung zwischen der AMO-ID und [!DNL Marketing Channels]?&quot; Oder manchmal: &quot;Warum sind die Daten kaputt? Ich benötige, dass alle Metriken in allen Berichten übereinstimmen.&quot; Glücklicherweise zeigen Diskrepanzen nicht an, dass die Daten &quot;beschädigt&quot;sind, und Diskrepanzen werden erwartet und sogar gewünscht. Sehen wir uns an, warum die Integration auf diese Weise entworfen wurde.

Die beiden Datensätze weisen unterschiedliche Hauptanwendungsfälle auf:

* [!DNL Marketing Channels]: Der primäre Anwendungsfall für  [!DNL Marketing Channels] besteht darin, Daten über mehrere Kanäle hinweg mit einem gemeinsamen Attributionsmodell zu vergleichen. Analysten können die Dimension [!UICONTROL Marketing Channel] verwenden, um bessere Einblicke in die Interaktion zwischen Kanälen zu erhalten. Diese Einblicke können dazu beitragen, Entscheidungen auf Makroebene darüber zu treffen, wie in die einzelnen Kanäle investiert werden soll, und können zu Einblicken darüber führen, wie Besucher aus den einzelnen Kanälen mit der Website interagieren.

   Die Dimension [!DNL Analytics] [!UICONTROL Marketing Channel] ist daher so konfiguriert, dass alle Kanäle erfasst und verfolgt werden. [!DNL Marketing Channels] kann auch so konfiguriert werden, dass Advertising Cloud DSP-Durchsichten und Clickthroughs erfasst werden. Dies geschieht in Bezug auf die anderen Marketingkanäle.

* Advertising Cloud AMO ID: Das Hauptanwendungsbeispiel für die Advertising Cloud AMO ID-Daten besteht darin, die erweiterten [!DNL Adobe Sensei]-basierten Bidding-Algorithmen von Advertising Cloud zu nutzen. Die Algorithmen treffen automatisch Tausende von Angebotsentscheidungen auf Mikroebene, die täglich getroffen werden, um Werbeausgaben zu maximieren und die Ziele der [!DNL DSP]-Kampagne oder des [!DNL Search]-Portfolios zu erreichen. Je mehr Konversionsdaten die Algorithmen mit Kampagnen verbinden können, desto besser können die Algorithmen diese Angebotsentscheidungen treffen.

   Um diese Daten zu erfassen, übergibt die Integration [!DNL Analytics for Advertising Cloud] unbearbeitete AMO-IDs, die als Clickthrough- und Durchsichts-Trackingcodes in der AMO-ID-Dimension von Adobe Analytics übersetzt werden können. Diese Daten werden entweder als benutzerspezifische Variable (eVar) oder als reservierte Variable (rVar) gespeichert. Clickthroughs für andere Kanäle werden nicht in der AMO-ID-Dimension festgelegt, sodass die AMO-ID-Dimension die Eingabe aus diesen anderen Kanälen nicht verfolgen kann. Das Ergebnis ist, dass die AMO-ID über die Einstiegspunkte [!DNL Marketing Channes]l beibehalten wird.

Weitere Informationen zu möglichen Datenabweichungen zwischen Advertising Cloud-verfolgten Daten und [!DNL Analytics]-verfolgten Daten finden Sie unter &quot;[Erwartete Datenabweichungen zwischen [!DNL Analytics] und Advertising Cloud](../data-variances.md)&quot;.

>[!MORELIKETHIS]
>
>* [Erwartete Datenabweichungen  [!DNL Analytics] zwischen und Advertising Cloud](/help/integrations/analytics/data-variances.md)
>* [Grundlagen [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Verwenden von Advertising Cloud IDs zum  [!DNL Marketing Channels] Erstellen von Verarbeitungsregeln](mc-ids.md)
>* [ [!DNL Analytics Marketing Channels] Verwenden mit Advertising Cloud-Daten](mc-ac-data.md)
>* [Video: Reporting mit Advertising Cloud [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)

