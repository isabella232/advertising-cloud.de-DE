---
title: Übersicht über [!DNL Analytics for Advertising Cloud]
description: Übersicht über [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 31367c8b-3410-4110-9ae6-11defe625355
source-git-commit: bfbfc293ad04b294c813ce7c8a11200e70fc812f
workflow-type: tm+mt
source-wordcount: '1086'
ht-degree: 0%

---

# Übersicht über [!DNL Analytics for Advertising Cloud]

*Advertiser mit Advertising Cloud DSP und Advertising Cloud Search*

[!DNL Analytics for Advertising Cloud] integriert Adobe Analytics und Adobe Advertising Cloud, um die Funktionen der einzelnen Produkte zu erweitern und zu erweitern.

Die Integration ermöglicht es Advertisern, Clickthrough- und Durchsichts-Site-Interaktionen in ihren [!DNL Analytics] Instanzen, sodass Marken sehen können, wie ihre Werbeausgaben zu Site-Interaktionen und kritischen Geschäftszielen führen.

Darüber hinaus kann Advertising Cloud auf die umfangreichen Erstanbieterdaten zugreifen, die [!DNL Analytics] erfasst mithilfe von [!DNL Analytics] Tags bereits auf der Site. Dies ermöglicht ein robusteres Journey-Management, Erstanbieter-Remarketing und die Berichterstellung für gebührenpflichtige Medien-Sites. Advertising Cloud kann die [!DNL Analytics] Daten zur Ausgaben- und Angebotsoptimierung.

Bei ordnungsgemäßer Arbeit [!DNL Analytics for Advertising Cloud] verwischt die Linien zwischen zwei traditionellen Rollen: Anzeigen-Journey-Management (die Aktivität, durch Werbung Benutzer auf die Site zu leiten) und Verstehen der Site-Interaktion durch Webanalysen.

Primäre Vorteile:

* Senden [!DNL Analytics] Segmente direkt an Advertising Cloud senden, um Erstanbieter-Site-Remarketing zu ermöglichen.
* Verwendung [!DNL Analytics] benutzerspezifische und standardmäßige Ereignisse als Konversionssignale zur Optimierung der Paid-Media-Werbung.
* Nutzen Sie die Vorteile von [!DNL Analytics] Analysis Workspace , um Einstiegspunkte und Besuchsverhalten besser zu verstehen.
* Schaffen Sie eine engere Zusammenarbeit zwischen Webanalysten und Paid-Media-Teams.
* Verwenden beständiger Advertising Cloud-Durchsichts- und Clickthrough-IDs in [!DNL Analytics] , um die Site-Interaktion zu verstehen.
* Erweitern Sie herkömmliche Berichte zu gebührenpflichtigen Medien in Analysis Workspace mit benutzerdefinierten Metriken, benutzerdefinierten Dimensionen und Site-Aktivitäten, die beim Exportieren von Daten oder Pixeln in Werbeserver oder andere DSP nicht erreichbar sind.
* Nutzen Sie die Vorteile von [!DNL Analytics] Code, der bereits auf Ihrer Website zur Verfolgung und Optimierung in Advertising Cloud bereitgestellt wird.

>[!TIP]
>
> Sehen Sie sich eine [Videoeinführung in [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics).

## Verwenden von Analytics für Berichte zu gebührenpflichtigen Medien

[!DNL Analytics for Advertising Cloud] verbessert die Berichterstellung und Einblicke, wie Ihre Werbung das Site-Verhalten fördert, indem Sie:

* Verwenden beständiger Advertising Cloud-Durchsichts- und Clickthrough-IDs in [!DNL Analytics] , um die Site-Interaktion zu verstehen.
* Nutzen Sie Analysis Workspace, um Einstiegspunkte auf der Site und das Besuchsverhalten besser zu verstehen. Sie können auf Paid-Media-Dimensions- und Ereignisdaten zugreifen, zu denen Advertising Cloud-Kampagnenentitätsnamen (bis hin zu Platzierungen und Anzeigen) und die zugehörigen Metriken wie Klicks, Impressionen und Kosten gehören.

Verwendung [!DNL Analytics] als Reporting-Tool für gebührenpflichtige Medien benötigt Ihr Unternehmen eine Experience Cloud-Anmeldung mit Zugriff auf Analysis Workspace. Ihr Advertising Cloud-Team hilft Ihnen bei der Zuordnung Ihrer Advertising Cloud-Daten zu einzelnen Report Suites in Analysis Workspace. Sie können Advertising Cloud-Daten an eine beliebige Report Suite senden. Beachten Sie jedoch die Report Suites, die Advertising Cloud zugeordnet wurden, und jene, die dies nicht getan haben. Abhängig von der Report Suite kann dies die gemeldeten Daten ändern.

[Advertising Cloud IDs in [!DNL Analytics]](ids.md) funktioniert wie andere eVars mit einem benutzerdefinierten, beständigen Ablauf. Standardmäßig ist das Attributions-Lookback-Fenster während der Advertising Cloud-Implementierung auf 60 Tage eingestellt. Wenden Sie sich an Ihre [!DNL Adobe] Kundenbetreuer.

Advertising Cloud-Dimensionen werden mit dem Suffix &quot;(AMO-ID)&quot;angehängt (z. B. &quot;Anzeigentyp (AMO-ID)&quot;). Siehe[Advertising Cloud-Metriken in Analysis Workspace](advertising-cloud-metrics-in-analytics.md)&quot; für eine Liste der verfügbaren Dimensionen.

>[!NOTE]
>
> Wenn Sie Advertising Cloud-Daten (oder einen beliebigen Datensatz) in [!DNL Analytics]Beachten Sie, dass Metriken und Berichte auf den Regeln basieren, die in [!DNL Analytics]. Die Daten können sich von denen in anderen Berichterstattungssystemen unterscheiden, z. B. in Berichten für Werbeserver, [!DNL DSP] Berichte oder Suchmaschinenberichte. So verstehen Sie die Datenunterschiede in [!DNL Analytics]müssen Sie wissen, wann die Daten der eVar ablaufen, was einen Besuch definiert, was als Letztkontakt-Attribution im Vergleich zur persistenten Attribution insgesamt gilt und andere Faktoren. Weitere Informationen finden Sie unter [Erwartete Datenabweichungen zwischen [!DNL Analytics] und Advertising Cloud](data-variances.md).

## Verwenden von Analytics für Advertising Cloud-Kampagnen und -Portfolios

Ohne zusätzliche Pixel zu benötigen, [!DNL Analytics for Advertising Cloud] ermöglicht eine bessere Optimierung und einfachere Zielgruppensegmentierung, indem zwei Hauptsignale an Advertising Cloud gesendet werden:

* Als Angebotssignale zu verwendende Konversionsmetriken:
   * Standardmetriken, wie [!UICONTROL Revenue] und [!UICONTROL Cart Views].
   * Site-Interaktionsmetriken, z. B. Seitenansichts- und Besuchsmetriken.
   * benutzerspezifische Umsatzmetriken.
   * reservierte Umsatzmetriken.
* In erstellte Segmente [!DNL Analytics] und in Experience Cloud veröffentlicht.

   Sie können [!DNL Analytics] Segmente für Erstanbieter-Site-Retargeting in [!DNL DSP] und Paid Search-Werbung.

   (Nur Advertising Cloud Search) Advertiser mit [!DNL Analytics] Audience Manager können jedoch auch nicht aus Google-Website-Tag-basierte Zielgruppen (Remarketing-Listen) und Zielgruppen für die Kundenübereinstimmung (Kundenlisten) aus erstellen. [!DNL Analytics] Segmente, die für Experience Cloud freigegeben sind.

### Site-Konversionsmetriken als Angebotssignale

Sie können Ihre Standardereignisse und benutzerspezifischen Ereignisse aus [!DNL Analytics] zur Festlegung gewichteter Ziele in Advertising Cloud. Ziele informieren über Angebotsentscheidungen für Ihre [!DNL DSP] Packages und Suchportfolios.

>[!NOTE]
>
> Berechnete Metriken können nicht zugeordnet werden aus [!DNL Analytics] nach Advertising Cloud.

Ihr Advertising Cloud-Team hilft Ihnen dabei, die Ereignisse zu identifizieren und zuzuordnen, die für die Leistung von Paid Media relevant sind, wo sie in Advertising Cloud angezeigt werden. [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

Siehe[Analytics-Metriken in Advertising Cloud](analytics-data-in-advertising-cloud.md)für eine Liste der verfügbaren Metriken.

### Analytics-Segmente für Site-Retargeting

Advertising Cloud kann aufnehmen [!DNL Analytics] Segmente für Remarketing-Zwecke für Advertising Cloud DSP und [!DNL Search] Anzeigen, die die native Experience Cloud-Zielgruppenintegration zwischen [!DNL Analytics] und Experience Cloud.

So greifen Sie auf die [!DNL Analytics] Segmente, muss ein Advertiser-Konto über die [Experience Cloud-ID-Dienst](https://experienceleague.adobe.com/docs/id-service/using/home.html) aktiviert. Wenn der ID-Dienst aktiviert ist, werden alle Segmentsegmente (einschließlich der in [!DNL Analytics] und in Experience Cloud veröffentlicht werden, in Adobe Audience Manager erstellte Segmente, in Experience Cloud erstellte Segmente mithilfe der Variablen [!DNL People core service]und Segmente, die in Adobe Experience Platform erstellt und über Audience Manager an Advertising Cloud gesendet wurden) in Advertising Cloud verfügbar werden, sobald sie verarbeitet werden.

[!DNL Analytics] -Segmente sind innerhalb von 24 Stunden verfügbar und werden täglich aktualisiert.

Weitere Informationen zum Experience Cloud Audiences-Dienst finden Sie unter [Experience Cloud Audiences](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Beispiele zur Verwendung der Integration

### Verwenden von Advertising Cloud-Daten in Analysis Workspace

Informationen dazu, wie Sie mit Ihren Advertising Cloud-Daten visuelle Berichte in Analysis Workspace erstellen können, finden Sie im Video &quot;[Einführung in Workspace und Reporting](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

### Erstellen von Advertising Cloud-Dashboards

Informationen dazu, wie Sie Ihre Advertising Cloud-Daten mit Ihren Zielen in Analysis Workspace vergleichen können, finden Sie im Video &quot;[Erstellen von Advertising Cloud-Dashboards mit Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### Verwenden der Advertising Cloud ID für die Site-Einstiegsanalyse

Informationen zum Erstellen eines Advertising Cloud Site-Einstiegsberichts zur Überwachung von Wochentagen, Tageszeiten, Browsern und geografischen Einflüssen finden Sie im Video .[Erstellen von Advertising Cloud Site-Einstiegsberichten](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-site-entry-a4adc.html).&quot;

>[!MORELIKETHIS]
>
>* [Video: Einführung in [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html)
>* [Voraussetzungen und Schlüsselinformationen für die Implementierung [!DNL Analytics for Advertising Cloud]](prerequisites.md)
>* [Von Analytics verwendete Advertising Cloud IDs](ids.md)
>* [JavaScript-Code für Analytics für Advertising Cloud](/help/integrations/analytics/javascript.md)
>* [Erwartete Datenabweichungen zwischen [!DNL Analytics] und Advertising Cloud](data-variances.md)
>* [Advertising Cloud-Metriken in Analysis Workspace](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Daten in Advertising Cloud](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

