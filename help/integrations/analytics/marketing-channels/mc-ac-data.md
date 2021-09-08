---
title: Verwenden von [!DNL Marketing Channels] mit Advertising Cloud-Daten
description: Erfahren Sie, wie Sie Advertising Cloud-Daten in [!DNL Analytics Marketing Channels] verwenden.
feature: Integration with Adobe Analytics
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 0%

---

# Verwenden von [!DNL Analytics Marketing Channels] mit Advertising Cloud-Daten

*Werbetreibende, die nur über eine Advertising Cloud-Adobe Analytics-Integration verfügen*

Durch die Verwendung der Berichte Advertising Cloud und [!DNL Marketing Channels] erhalten Sie wertvolle Einblicke in die Beeinflussung der Site-Aktivität durch digitale Medien.

<!-- from video: By using Marketing Channels with your Advertising Cloud data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

Die folgende Abbildung zeigt, wie Advertising Cloud und [!DNL Marketing Channels] die einzelnen Besuche verfolgen, aus denen die Journey eines Besuchers besteht. Advertising Cloud-Berichte in [!DNL Analytics] sind auf Paid-Display- und Suchanzeigen beschränkt, die über Advertising Cloud unter Verwendung der AMO-ID gehandelt werden. [!DNL Marketing Channels] verfolgt jedoch alle in den [!DNL Marketing Channels] Verarbeitungsregeln konfigurierten Kanäle.

![So  [!DNL Marketing Channels] verfolgen Sie Advertising Cloud und die einzelnen Besuche auf der Journey eines Besuchers](/help/integrations/assets/a4adc-mc-sample-journey2.png)

Beim ersten Besuch kam der Benutzer über eine E-Mail-Kampagne auf die Website, führte zehn Seitenansichten durch und verließ dann die Website. Beim zweiten Besuch kam der Benutzer über eine Display-Anzeige auf die Site, führte zehn Seitenansichten aus und verließ dann die Site. Beim dritten Besuch kam der Benutzer über die natürliche Suche auf die Site, führte fünf Seitenansichten aus, führte eine Konversion von 250 USD und die linke Seite aus. Beachten Sie den Unterschied beim Tracking zwischen [!DNL Marketing Channels] und Advertising Cloud. Der einzige Kanal, den Advertising Cloud in dieser Journey verfolgt, ist [!UICONTROL Display]. Advertising Cloud verfolgt den Kanalbesuch von [!UICONTROL Display] und ordnet die nachfolgenden Interaktionsdaten (z. B. Seitenansichten) und Konversionen dem Einfluss dieser Werbung zu. [!DNL Marketing Channels]bietet jedoch einen umfassenden Überblick über alle Kanäle.

Da die AMO-ID über die Journey des Besuchers beibehalten wird, können Sie die AMO-ID-Daten verwenden, um zu sehen, wie Advertising Cloud andere Marketing-Kanäle beeinflusst. Die AMO-ID [bleibt standardmäßig 60 Tage lang bestehen](/help/integrations/analytics/overview.md). Sie können die Persistenz jedoch nach Bedarf konfigurieren.

## Kombinieren von Advertising Cloud- und Marketingkanaldaten zur Analyse der Medienleistung

Innerhalb von [!DNL Analytics] können Sie die Advertising Cloud, die Paid-Advertising-Daten beibehält, mit den [!DNL Marketing Channels] umfassenden Besuchsdaten kombinieren, um Ihre Medienleistung besser zu analysieren und so die Journey des Kunden besser beeinflussen zu können.

Die folgende Analyse verwendet die Advertising Cloud-Daten, um verschiedene Versionen davon anzuzeigen, wie sich eine Display-Werbung auf die Site-Konversion auswirkt. Alle drei Spalten verwenden dieselben Konversionsmetriken, aber jede Spalte erzählt eine andere Geschichte:

* Spalte 1 betrachtet die AMO-ID-Daten, die über die Journey des Besuchers hinweg persistent sind. Spalte 1 zeigt an, dass 641 Anwendungsstarts zu einem bestimmten Zeitpunkt mit einer Advertising Cloud-Anzeige verknüpft waren, entweder durch eine Durchsicht oder ein Clickthrough-Ereignis. Diese Ansicht berücksichtigt keine andere [!DNL Marketing Channels]-Attribution.

* Im Datensatz [!DNL Marketing Channels] werden die 641 Anwendungsstarts jedoch anderen Marketing-Kanälen zugeordnet. Die letzten beiden Spalten nehmen die 641 Anwendungen an und beschränken die Daten auf die Kanäle [!UICONTROL Display Click-Through] und [!UICONTROL Display View-Through], wobei die Konversionen angezeigt werden, die in einem Letztkontakt-Attributionsmodell auftreten.

![Beispiel, wie eine Display-Anzeige die Site-Konversion beeinflusst](/help/integrations/assets/a4adc-mc-display-impact.png)

Sie können diese Analyse einen Schritt weiter ausführen. Sie können die Advertising Cloud-Zeile weiter nach Marketing-Kanälen aufschlüsseln, um zu sehen, wo die Advertising Cloud-Konversionen den 641 Anwendungsstarts zugeordnet werden. Sie wissen bereits, dass fünf dieser Konversionen einem Last Touch-Display-Clickthrough und 19 einem Last Touch-Display-Clickthrough zugeordnet werden. Dadurch bleiben 617 Anwendungsstarts weiterhin anderen Marketingkanälen zugeordnet. Sie können die Dimension &quot;Letztkontakt Kanal&quot;per Drag-and-Drop auf das Zeilenelement &quot;Advertising Cloud DSP&quot;ziehen, um die Kanalzuordnung für den Rest der &quot;Anwendungsstarts&quot;anzuzeigen und die kanalübergreifende Auswirkung des Anzeigekanals anzuzeigen.

![Hinzufügen der Dimension &quot;Letztkontakt Kanal&quot;](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

Jetzt können Sie sehen, wie die verbleibenden Anwendungsstarts zugeordnet werden. E-Mail wird 357 Last Touch-Anwendungen Starts zugeschrieben, für die eine AMO-ID beibehalten wurde. Mithilfe dieser Art von Analyse können Sie sehen, wie sich die Display-Anzeigen von Advertising Cloud auf alle Kanäle ausgewirkt haben. Bei nur einem Datensatz und Attributionsmodell ist dieser Insight-Typ nicht verfügbar.

![Beispiel für die kanalübergreifende Auswirkung der Anzeigekanäle](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

Sie können die Analyse weiter verbessern, indem Sie ein Stack-Diagramm verwenden, das auf &quot;100 % gestapelt&quot;festgelegt ist, um Trend-Daten über einen bestimmten Zeitraum anzuzeigen. Diese Visualisierung erleichtert die Überwachung der von Ihren Display-Marketing-Kampagnen am stärksten betroffenen Letztkontakt-Marketing-Kanäle.

![Beispiel für die kanalübergreifende Trendwirkung der Anzeigekanäle](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [Grundlagen [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Verwenden von Advertising Cloud IDs zum  [!DNL Marketing Channels] Erstellen von Verarbeitungsregeln](mc-ids.md)
>* [Warum Kanaldaten zwischen Advertising Cloud und variieren können [!DNL Marketing Channels]](mc-data-variances.md)
>* [Video: Reporting mit Advertising Cloud [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [Übersicht über [!DNL Analytics for Advertising Cloud]](/help/integrations/analytics/overview.md)

