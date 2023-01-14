---
title: Verwenden [!DNL Marketing Channels] mit Adobe Advertising-Daten
description: Erfahren Sie, wie Sie Adobe Advertising-Daten in [!DNL Analytics Marketing Channels].
feature: Integration with Adobe Analytics
exl-id: c9403a03-58aa-4633-bb97-51afc30843ad
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '708'
ht-degree: 0%

---

# Verwenden [!DNL Analytics Marketing Channels] mit Adobe Advertising-Daten

*Werbetreibende mit nur einer Adobe Advertising-Adobe Analytics-Integration*

Durch Verwendung von Adobe Advertising und [!DNL Analytics Marketing Channels] Berichte erhalten Sie wertvolle Einblicke in die Einflussnahme Ihrer digitalen Medien auf die Site-Aktivität.

<!-- from video: By using Marketing Channels with your Adobe Advertising data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

Die folgende Abbildung zeigt, wie Adobe Advertising und [!DNL Marketing Channels] die individuellen Besuche verfolgen, aus denen die Journey eines Besuchers besteht. Adobe Advertising-Berichte in [!DNL Analytics] sind auf die Werbung für gebührenpflichtige Display-, Such-, Social- und Commerce-Kanäle beschränkt, die über Adobe Advertising unter Verwendung der AMO-ID weitergeleitet wird. Allerdings [!DNL Marketing Channels] verfolgt alle in der [!DNL Marketing Channels] Verarbeitungsregeln.

![Wie Adobe Advertising und [!DNL Marketing Channels] einzelne Besuche auf der Journey eines Besuchers verfolgen](/help/integrations/assets/a4adc-mc-sample-journey2.png)

Beim ersten Besuch kam der Benutzer über eine E-Mail-Kampagne auf die Website, führte zehn Seitenansichten durch und verließ dann die Website. Beim zweiten Besuch kam der Benutzer über eine Display-Anzeige auf die Site, führte zehn Seitenansichten aus und verließ dann die Site. Beim dritten Besuch kam der Benutzer über die natürliche Suche auf die Site, führte fünf Seitenansichten aus, führte eine Konversion von 250 USD und die linke Seite aus. Beachten Sie den Unterschied bei der Verfolgung zwischen [!DNL Marketing Channels] und Werbung für Adoben. Der einzige Kanal, den Adobe Advertising in diesem Journey verfolgt, ist [!UICONTROL Display]. Adobe Advertising verfolgt die [!UICONTROL Display] Kanalbesuch und ordnet die nachfolgenden Interaktionsdaten (z. B. Seitenansichten) und Konversionen dem Einfluss dieser Werbung zu. [!DNL Marketing Channels]bietet jedoch einen umfassenden Überblick über alle Kanäle.

Da die AMO-ID durch die Journey des Besuchers erhalten bleibt, können Sie die AMO-ID-Daten verwenden, um zu sehen, wie Adobe Advertising andere Marketingkanäle beeinflusst. Die AMO-ID [ist standardmäßig 60 Tage lang persistent](/help/integrations/analytics/overview.md), aber Sie können die Persistenz nach Bedarf konfigurieren.

## Kombinieren von Daten zu Adobe Advertising- und Marketingkanälen zur Analyse der Medienleistung

Within [!DNL Analytics]können Sie die Adobe Advertising-Daten, die Paid-Advertising-Daten beibehalten, mit der [!DNL Marketing Channels] umfassende Besuchsdaten, um Ihre Medienleistung besser zu analysieren, sodass Sie die Journey der Kunden besser beeinflussen können.

Die folgende Analyse verwendet die Adobe Advertising-Daten, um verschiedene Versionen davon anzuzeigen, wie sich eine Display-Werbung auf die Site-Konversion auswirkt. Alle drei Spalten verwenden dieselben Konversionsmetriken, aber jede Spalte erzählt eine andere Geschichte:

* Spalte 1 betrachtet die AMO-ID-Daten, die über die Journey des Besuchers hinweg persistent sind. Spalte 1 zeigt an, dass 641 App-Starts zu einem Zeitpunkt entweder durch einen Durchsichts- oder ein Clickthrough-Ereignis mit einer Adobe-Werbeanzeige verknüpft waren. Diese Ansicht nimmt keine andere an [!DNL Marketing Channels] Attribution berücksichtigen.

* Im [!DNL Marketing Channels] jedoch werden die 641 Anwendungen Starts anderen Marketing-Kanälen zugeordnet. Die letzten beiden Spalten nehmen die 641 Anwendungen auf und beschränken die Daten auf die [!UICONTROL Display Click-Through] und [!UICONTROL Display View-Through] Kanäle, die die Konversionen anzeigen, die in einem Letztkontakt-Attributionsmodell auftreten.

![Beispiel, wie eine Display-Anzeige die Site-Konversion beeinflusst](/help/integrations/assets/a4adc-mc-display-impact.png)

Sie können diese Analyse einen Schritt weiter ausführen. Sie können die Zeile &quot;Adobe Advertising&quot;weiter nach Marketingkanälen aufschlüsseln, um zu sehen, wo die Adobe-Advertising-Konversionen den 641 &quot;Applications Starts&quot;zugeordnet werden. Sie wissen bereits, dass fünf dieser Konversionen einem Last Touch-Display-Clickthrough und 19 einem Last Touch-Display-Clickthrough zugeordnet werden. Dadurch bleiben 617 Anwendungsstarts weiterhin anderen Marketingkanälen zugeordnet. Sie können die Dimension &quot;Letztkontakt Kanal&quot;per Drag-and-Drop auf den Zeileneintrag Werbung DSP ziehen, um die Kanalzuordnung für den Rest der Anwendungsstarts anzuzeigen und die kanalübergreifende Auswirkung des Anzeigekanals anzuzeigen.

![Hinzufügen der Dimension &quot;Letztkontakt Kanal&quot;](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

Jetzt können Sie sehen, wie die verbleibenden Anwendungsstarts zugeordnet werden. E-Mail wird 357 Last Touch-Anwendungen Starts zugeschrieben, für die eine AMO-ID beibehalten wurde. Mithilfe dieses Analysetyps können Sie sehen, wie sich Werbeanzeigen von Adobe auf alle Kanäle ausgewirkt haben. Bei nur einem Datensatz und Attributionsmodell ist dieser Insight-Typ nicht verfügbar.

![Beispiel für die kanalübergreifende Auswirkung der Anzeigekanäle](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

Sie können die Analyse weiter verbessern, indem Sie ein Stack-Diagramm verwenden, das auf &quot;100 % gestapelt&quot;festgelegt ist, um Trend-Daten über einen bestimmten Zeitraum anzuzeigen. Diese Visualisierung erleichtert die Überwachung der von Ihren Display-Marketing-Kampagnen am stärksten betroffenen Letztkontakt-Marketing-Kanäle.

![Beispiel für die kanalübergreifende Trendwirkung der Anzeigekanäle](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [Grundlagen [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Erstellen von Adobe Advertising-IDs mit [!DNL Marketing Channels] Verarbeitungsregeln](mc-ids.md)
>* [Warum können Kanaldaten zwischen Adobe Advertising und [!DNL Marketing Channels]](mc-data-variances.md)
>* [Video: Verwenden [!DNL Marketing Channels] für Adobe Advertising Reporting](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Übersicht über [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)

