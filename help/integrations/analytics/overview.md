---
title: Übersicht über [!DNL Analytics for Advertising]
description: Übersicht über [!DNL Analytics for Advertising]
feature: Integration with Adobe Analytics
exl-id: 31367c8b-3410-4110-9ae6-11defe625355
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '1076'
ht-degree: 0%

---

# Übersicht über [!DNL Analytics for Advertising]

*Advertiser mit Advertising DSP und[!DNL Advertising Search]*

[!DNL Analytics for Advertising] integriert Adobe Analytics und Adobe Advertising, um die Produktfunktionen zu erweitern und zu erweitern.

Die Integration ermöglicht es Advertisern, Clickthrough- und Durchsichts-Site-Interaktionen in ihren [!DNL Analytics] Instanzen, sodass Marken sehen können, wie ihre Werbeausgaben zu Site-Interaktionen und kritischen Geschäftszielen führen.

Darüber hinaus kann Adobe Advertising auf die umfangreichen Erstanbieterdaten zugreifen, die [!DNL Analytics] erfasst mithilfe von [!DNL Analytics] Tags bereits auf der Site. Dies ermöglicht ein robusteres Journey-Management, Erstanbieter-Remarketing und die Berichterstellung für gebührenpflichtige Medien-Sites. Adobe Advertising kann die [!DNL Analytics] Daten zur Ausgaben- und Angebotsoptimierung.

Bei ordnungsgemäßer Arbeit [!DNL Analytics for Advertising] verwischt die Linien zwischen zwei traditionellen Rollen: Anzeigen-Journey-Management (die Aktivität, durch Werbung Benutzer auf die Site zu leiten) und Verstehen der Site-Interaktion durch Webanalysen.

Primäre Vorteile:

* Senden [!DNL Analytics] Segmente direkt zur Adobe Advertising für Erstanbieter-Site-Remarketing.
* Verwendung [!DNL Analytics] benutzerspezifische und standardmäßige Ereignisse als Konversionssignale zur Optimierung der Paid-Media-Werbung.
* Nutzen Sie die Vorteile von [!DNL Analytics] Analysis Workspace , um Einstiegspunkte und Besuchsverhalten besser zu verstehen.
* Schaffen Sie eine engere Zusammenarbeit zwischen Webanalysten und Paid-Media-Teams.
* Verwenden Sie persistente Anzeigen-Durchsichts- und Clickthrough-IDs für Adobe Advertising in [!DNL Analytics] , um die Site-Interaktion zu verstehen.
* Erweitern Sie herkömmliche Berichte zu gebührenpflichtigen Medien in Analysis Workspace mit benutzerdefinierten Metriken, benutzerdefinierten Dimensionen und Site-Aktivitäten, die beim Exportieren von Daten oder Pixeln in Werbeserver oder andere DSP nicht erreichbar sind.
* Nutzen Sie die Vorteile von [!DNL Analytics] Code, der bereits auf Ihrer Website zur Verfolgung und Optimierung in der Adobe Advertising verwendet wird.

>[!TIP]
>
> Sehen Sie sich eine [Videoeinführung in [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics).

## Verwenden von Analytics für Berichte zu gebührenpflichtigen Medien

[!DNL Analytics for Advertising] verbessert die Berichterstellung und Einblicke, wie Ihre Werbung das Site-Verhalten fördert, indem Sie:

* Verwenden Sie persistente Anzeigen-Durchsichts- und Clickthrough-IDs für Adobe Advertising in [!DNL Analytics] , um die Site-Interaktion zu verstehen.
* Nutzen Sie Analysis Workspace, um Einstiegspunkte und Besuchsverhalten auf der Site besser zu verstehen. Sie können auf Paid-Media-Dimensions- und Ereignisdaten zugreifen, zu denen die Entitätsnamen von Adobe-Werbekampagnen (bis hin zu Platzierungen und Anzeigen) und die zugehörigen Metriken wie Klicks, Impressionen und Kosten gehören.

Verwendung [!DNL Analytics] als Reporting-Tool für gebührenpflichtige Medien benötigt Ihr Unternehmen eine Experience Cloud-Anmeldung mit Zugriff auf Analysis Workspace. Ihr Adobe Advertising-Team hilft Ihnen dabei, Ihre Adobe Advertising-Daten einzelnen Report Suites in Analysis Workspace zuzuordnen. Sie können Adobe Advertising-Daten an eine beliebige Report Suite senden. Beachten Sie jedoch die Report Suites, die der Adobe Advertising zugeordnet wurden, und jene, die dies nicht getan haben. Abhängig von der Report Suite kann dies die gemeldeten Daten ändern.

[Adobe Advertising-IDs in [!DNL Analytics]](ids.md) funktioniert wie andere eVars mit einem benutzerdefinierten, beständigen Ablauf. Standardmäßig ist das Attributions-Lookback-Fenster während der Adobe Advertising-Implementierung auf 60 Tage eingestellt. Wenden Sie sich an Ihre [!DNL Adobe] Account-Team.

Adobe Advertising-Dimensionen werden mit dem Suffix &quot;(AMO-ID)&quot;angehängt (z. B. &quot;Anzeigentyp (AMO-ID)&quot;). Siehe[Adobe Advertising-Metriken in Analysis Workspace](advertising-cloud-metrics-in-analytics.md)&quot; für eine Liste der verfügbaren Dimensionen.

>[!NOTE]
>
> Wenn Sie Adobe Advertising-Daten (oder einen beliebigen Datensatz) in [!DNL Analytics]Beachten Sie, dass Metriken und Berichte auf den Regeln basieren, die in [!DNL Analytics]. Die Daten können sich von denen in anderen Berichterstattungssystemen unterscheiden, z. B. in Berichten für Werbeserver, [!DNL DSP] Berichte oder Suchmaschinenberichte. So verstehen Sie die Datenunterschiede in [!DNL Analytics]müssen Sie wissen, wann die Daten der eVar ablaufen, was einen Besuch definiert, was als Letztkontakt-Attribution im Vergleich zur persistenten Attribution insgesamt gilt und andere Faktoren. Weitere Informationen finden Sie unter [Erwartete Datenabweichungen zwischen [!DNL Analytics] und Adobe Advertising](data-variances.md).

## Verwenden von Analytics zur Leistungsoptimierung von Adobe-Werbekampagnen und -Portfolios

Ohne zusätzliche Pixel zu benötigen, [!DNL Analytics for Advertising] ermöglicht eine bessere Optimierung und einfachere Zielgruppensegmentierung, indem zwei Hauptsignale an die Adobe Advertising gesendet werden:

* Als Angebotssignale zu verwendende Konversionsmetriken:
   * Standardmetriken, wie [!UICONTROL Revenue] und [!UICONTROL Cart Views].
   * Site-Interaktionsmetriken, z. B. Seitenansichts- und Besuchsmetriken.
   * benutzerspezifische Umsatzmetriken.
   * reservierte Umsatzmetriken.
* In erstellte Segmente [!DNL Analytics] und in Experience Cloud veröffentlicht.

   Sie können [!DNL Analytics] Segmente für Erstanbieter-Site-Retargeting in [!DNL DSP] und Paid Search-Werbung.

   ([!DNL Search] Nur Advertiser mit [!DNL Analytics] Audience Manager können jedoch auch nicht aus Google-Website-Tag-basierte Zielgruppen (Remarketing-Listen) und Zielgruppen für die Kundenübereinstimmung (Kundenlisten) aus erstellen. [!DNL Analytics] Segmente, die für Experience Cloud freigegeben sind.

### Site-Konversionsmetriken als Angebotssignale

Sie können Ihre Standardereignisse und benutzerspezifischen Ereignisse aus [!DNL Analytics] um gewichtete Ziele in der Adobe Advertising zu erstellen. Ziele informieren über Angebotsentscheidungen für Ihre [!DNL DSP] Packages und Suchportfolios.

>[!NOTE]
>
> Berechnete Metriken können nicht zugeordnet werden aus [!DNL Analytics] in die Werbung für Adoben.

Ihr Adobe Advertising-Team hilft Ihnen dabei, die für die gebührenpflichtige Medienleistung relevanten Ereignisse zu identifizieren und sie der Adobe Advertising zuzuordnen, wo sie erscheinen werden in [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

Siehe[Analytics-Metriken in Adobe Advertising](analytics-data-in-advertising-cloud.md)für eine Liste der verfügbaren Metriken.

### Analytics-Segmente für Site-Retargeting

Adobe Advertising kann aufnehmen [!DNL Analytics] Segmente für Remarketing-Zwecke für Advertising DSP und [!DNL Search] Anzeigen, die die native Experience Cloud-Zielgruppenintegration zwischen [!DNL Analytics] und Experience Cloud.

So greifen Sie auf die [!DNL Analytics] Segmente, muss ein Advertiser-Konto über die [Experience Cloud-ID-Dienst](https://experienceleague.adobe.com/docs/id-service/using/home.html) aktiviert. Wenn der ID-Dienst aktiviert ist, werden alle Segmentsegmente (einschließlich der in [!DNL Analytics] und in Experience Cloud veröffentlicht werden, in Adobe Audience Manager erstellte Segmente, in Experience Cloud erstellte Segmente mithilfe der Variablen [!DNL People core service], und Segmente, die in Adobe Experience Platform erstellt und über Audience Manager an Adobe Advertising gesendet wurden) werden in der Adobe Advertising verfügbar, sobald sie verarbeitet werden.

[!DNL Analytics] -Segmente sind innerhalb von 24 Stunden verfügbar und werden täglich aktualisiert.

Weitere Informationen zum Experience Cloud Audiences-Dienst finden Sie unter [Experience Cloud Audiences](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Beispiele zur Verwendung der Integration

### Verwenden von Adobe Advertising-Daten in Analysis Workspace

Informationen dazu, wie Sie mit Ihren Adobe Advertising-Daten visuelle Berichte in Analysis Workspace erstellen können, finden Sie im Video &quot;[Einführung in Workspace und Reporting](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html).&quot;

### Erstellen von Adobe Advertising Dashboards

Informationen dazu, wie Sie Ihre Adobe Advertising-Daten mit Ihren Zielen in Analysis Workspace vergleichen können, finden Sie im Video &quot;[Erstellen von Adobe Advertising Dashboards mit Adobe Analytics](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-dashboards-a4adc.html).&quot;

### Verwenden der Adobe Advertising ID für die Site-Einstiegsanalyse

Informationen dazu, wie Sie einen Site-Einstiegsbericht für Adobe Advertising erstellen können, um Wochentage, Tageszeit, Browser und geografische Einflüsse zu überwachen, finden Sie im Video .[Erstellen von Adobe Advertising Site-Einstiegsberichten](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-site-entry-a4adc.html).&quot;

>[!MORELIKETHIS]
>
>* [Video: Einführung in [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html)
>* [Voraussetzungen und Schlüsselinformationen für die Implementierung [!DNL Analytics for Advertising]](prerequisites.md)
>* [Von Analytics verwendete Adobe Advertising-IDs](ids.md)
>* [JavaScript-Code für Analytics für Advertising](/help/integrations/analytics/javascript.md)
>* [Erwartete Datenabweichungen zwischen [!DNL Analytics] und Adobe Advertising](data-variances.md)
>* [Adobe Advertising-Metriken in Analysis Workspace](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Daten in Adobe Advertising](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

