---
title: Überblick über [!DNL Analytics for Advertising Cloud]
description: Überblick über [!DNL Analytics for Advertising Cloud]
feature: Integration with Adobe Analytics
exl-id: 31367c8b-3410-4110-9ae6-11defe625355
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 0%

---

# Übersicht über [!DNL Analytics for Advertising Cloud]

*Advertiser mit Advertising Cloud DSP und Advertising Cloud Search*

[!DNL Analytics for Advertising Cloud] integriert Adobe Analytics und Adobe Advertising Cloud, um die Funktionen der einzelnen Produkte zu erweitern und zu erweitern.

Die Integration ermöglicht es Advertisern, Clickthrough- und Durchsichts-Site-Interaktionen in ihren [!DNL Analytics]-Instanzen zu verfolgen, sodass Marken sehen können, wie ihre Werbeausgaben zu Site-Interaktionen und wichtigen Geschäftszielen führen.

Darüber hinaus kann Advertising Cloud auf die umfangreichen Erstanbieterdaten zugreifen, die [!DNL Analytics] mit [!DNL Analytics] -Tags erfasst, die bereits auf der Site vorhanden sind. Dies ermöglicht ein robusteres Journey-Management, Erstanbieter-Remarketing und die Berichterstellung für gebührenpflichtige Medien-Sites. Advertising Cloud kann die [!DNL Analytics]-Daten weiter für die Ausgaben- und Angebotsoptimierung verwenden.

Bei ordnungsgemäßer Verwendung verwischt [!DNL Analytics for Advertising Cloud] die Zeilen zwischen zwei herkömmlichen Rollen: Anzeigen-Journey-Management (die Aktivität, durch Werbung Benutzer auf die Site zu leiten) und Verstehen der Site-Interaktion durch Webanalysen.

Primäre Vorteile:

* Senden Sie [!DNL Analytics]-Segmente direkt an Advertising Cloud für Erstanbieter-Website-Remarketing.
* Verwenden Sie [!DNL Analytics] benutzerspezifische und standardmäßige Ereignisse als Konversionssignale zur Optimierung der Paid-Media-Werbung.
* Nutzen Sie die Vorteile von [!DNL Analytics] Analysis Workspace, um Einstiegspunkte und Besuchsverhalten auf der Site besser zu verstehen.
* Schaffen Sie eine engere Zusammenarbeit zwischen Webanalysten und Paid-Media-Teams.
* Verwenden Sie beständige Advertising Cloud-Durchsichts- und Clickthrough-IDs innerhalb von [!DNL Analytics], um die Site-Interaktion zu verstehen.
* Erweitern Sie herkömmliche Berichte zu gebührenpflichtigen Medien in Analysis Workspace mit benutzerdefinierten Metriken, benutzerdefinierten Dimensionen und Site-Aktivitäten, die beim Exportieren von Daten oder Pixeln in Werbeserver oder andere DSP nicht erreichbar sind.
* Nutzen Sie den [!DNL Analytics]-Code, der bereits auf Ihrer Website zur Verfolgung und Optimierung in Advertising Cloud verfügbar ist.

>[!TIP]
>
> Sehen Sie sich eine [Videoeinführung zu [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html?lang=en#analytics) an.

## Verwenden von Analytics für Berichte zu gebührenpflichtigen Medien

[!DNL Analytics for Advertising Cloud] verbessert die Berichterstellung und Einblicke, wie Ihre Werbung das Site-Verhalten fördert, indem Sie:

* Verwenden Sie beständige Advertising Cloud-Durchsichts- und Clickthrough-IDs innerhalb von [!DNL Analytics], um die Site-Interaktion zu verstehen.
* Nutzen Sie Analysis Workspace, um Einstiegspunkte auf der Site und das Besuchsverhalten besser zu verstehen. Sie können auf Paid-Media-Dimensions- und Ereignisdaten zugreifen, zu denen Advertising Cloud-Kampagnenentitätsnamen (bis hin zu Platzierungen und Anzeigen) und die zugehörigen Metriken wie Klicks, Impressionen und Kosten gehören.

Um [!DNL Analytics] als Reporting-Tool für gebührenpflichtige Medien verwenden zu können, benötigt Ihr Unternehmen eine Experience Cloud-Anmeldung mit Zugriff auf Analysis Workspace. Ihr Advertising Cloud-Team hilft Ihnen bei der Zuordnung Ihrer Advertising Cloud-Daten zu einzelnen Report Suites in Analysis Workspace. Sie können Advertising Cloud-Daten an eine beliebige Report Suite senden. Beachten Sie jedoch die Report Suites, die Advertising Cloud zugeordnet wurden, und jene, die dies nicht getan haben. Abhängig von der Report Suite kann dies die gemeldeten Daten ändern.

[Advertising Cloud-IDs  [!DNL Analytics]](ids.md) mit einer benutzerdefinierten, beständigen Gültigkeit funktionieren wie andere eVars. Standardmäßig ist das Attributions-Lookback-Fenster während der Advertising Cloud-Implementierung auf 60 Tage eingestellt. Wenden Sie sich an Ihren Adobe-Kundenbetreuer, um diese Einstellung zu ändern.

Advertising Cloud-Dimensionen werden mit dem Suffix &quot;(AMO-ID)&quot;angehängt (z. B. &quot;Anzeigentyp (AMO-ID)&quot;). Eine Liste der verfügbaren Dimensionen finden Sie unter &quot;[Advertising Cloud-Metriken in Analysis Workspace](advertising-cloud-metrics-in-analytics.md)&quot;.

>[!NOTE]
>
> Beachten Sie bei der Anzeige von Advertising Cloud-Daten (oder beliebigen Datensätzen) in [!DNL Analytics], dass Metriken und Berichte auf den Regeln basieren, die in [!DNL Analytics] festgelegt sind. Die Daten können sich von denen in anderen Berichterstattungssystemen unterscheiden, z. B. in Berichten zu Anzeigenservern, [!DNL DSP]-Berichten oder Suchmaschinenberichten. Um die Datenunterschiede in [!DNL Analytics] zu verstehen, müssen Sie wissen, wann die eVar-Daten ablaufen, was einen Besuch definiert, was als Letztkontakt-Attribution im Vergleich zur persistenten Gesamtzuordnung betrachtet wird und andere Faktoren. Weitere Informationen finden Sie unter [Erwartete Datenabweichungen zwischen [!DNL Analytics] und Advertising Cloud](data-variances.md).

## Verwenden von Analytics für Advertising Cloud-Kampagnen und -Portfolios

Ohne zusätzliche Pixel zu benötigen, ermöglicht [!DNL Analytics for Advertising Cloud] eine bessere Optimierung und einfachere Zielgruppensegmentierung, indem zwei Hauptsignale an Advertising Cloud gesendet werden:

* Als Angebotssignale zu verwendende Konversionsmetriken:
   * Standardmetriken, wie [!UICONTROL Revenue] und [!UICONTROL Cart Views].
   * Site-Interaktionsmetriken, z. B. Seitenansichts- und Besuchsmetriken.
   * benutzerspezifische Umsatzmetriken.
   * reservierte Umsatzmetriken.
* Segmente, die in [!DNL Analytics] erstellt und in Experience Cloud veröffentlicht wurden.

   Sie können [!DNL Analytics]-Segmente für Erstanbieter-Site-Retargeting in [!DNL DSP] und Paid-Search-Anzeigen verwenden.

   (Nur Advertising Cloud Search) Werbetreibende mit [!DNL Analytics], jedoch nicht Audience Manager, können auch Google-Website-Tag-basierte Zielgruppen (Remarketing-Listen) und Zielgruppen für Kundenabgleich (Kundenlisten) aus [!DNL Analytics]-Segmenten erstellen, die für Experience Cloud freigegeben sind.

### Site-Konversionsmetriken als Angebotssignale

Sie können Standardereignisse und benutzerspezifische Ereignisse von [!DNL Analytics] verwenden, um gewichtete Ziele in Advertising Cloud zu erstellen. Ziele informieren über Angebotsentscheidungen für Ihre [!DNL DSP]-Pakete und Suchportfolios.

>[!NOTE]
>
> Sie können berechnete Metriken von [!DNL Analytics] nicht Advertising Cloud zuordnen.

Ihr Advertising Cloud-Team hilft Ihnen dabei, die Ereignisse, die für die Leistung von Paid Media relevant sind, zu identifizieren und der Advertising Cloud zuzuordnen, wo sie unter [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Transaction Properties] angezeigt werden.

Eine Liste der verfügbaren Metriken finden Sie unter &quot;[Analytics-Metriken in Advertising Cloud](analytics-data-in-advertising-cloud.md)&quot;.

### Analytics-Segmente für Site-Retargeting

Advertising Cloud kann [!DNL Analytics]-Segmente für Remarketing-Zecke für Advertising Cloud DSP- und [!DNL Search]-Anzeigen erfassen, indem die native Experience Cloud-Zielgruppenintegration zwischen [!DNL Analytics] und Experience Cloud verwendet wird.

Um auf die Segmente [!DNL Analytics] zugreifen zu können, muss für ein Advertiser-Konto der [Experience Cloud-ID-Dienst](https://experienceleague.adobe.com/docs/id-service/using/home.html) aktiviert sein. Wenn der ID-Dienst aktiviert ist, werden alle Segmentsegmente (einschließlich in [!DNL Analytics] erstellte und in Experience Cloud veröffentlichte Experience Cloud, in Adobe Audience Manager erstellte Segmente, in Experience Cloud mit [!DNL People core service] erstellte Segmente und in Adobe Experience Platform erstellte Segmente, die über Audience Manager an Advertising Cloud gesendet werden) in Advertising Cloud verfügbar, sobald sie verarbeitet werden.

[!DNL Analytics] -Segmente sind innerhalb von 24 Stunden verfügbar und werden täglich aktualisiert.

Weitere Informationen zum Experience Cloud-Zielgruppendienst finden Sie unter [Experience Cloud-Zielgruppen](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html).

## Beispiele zur Verwendung der Integration

### Verwenden von Advertising Cloud-Daten in Analysis Workspace

Informationen dazu, wie Sie mit Ihren Advertising Cloud-Daten visuelle Berichte in Analysis Workspace erstellen können, finden Sie im Video &quot;[Einführung in Workspace und Reporting](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-analysis-workspace-a4adc.html)&quot;.

### Erstellen von Advertising Cloud-Dashboards

Informationen dazu, wie Sie Ihre Advertising Cloud-Daten mit Ihren Zielen in Analysis Workspace vergleichen können, finden Sie im Video &quot;[Advertising Cloud-Dashboards mit Adobe Analytics erstellen](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-dashboards-a4adc.html)&quot;.

### Verwenden der Advertising Cloud ID für die Site-Einstiegsanalyse

Wie Sie einen Advertising Cloud-Site-Einstiegsbericht erstellen können, um Wochentag, Tageszeit, Browser und geografische Einflüsse zu überwachen, erfahren Sie im Video &quot;[Advertising Cloud Site Entry Reports erstellen](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/analytics-site-entry-a4adc.html)&quot;.

>[!MORELIKETHIS]
>
>* [Video: Einführung in [!DNL Analytics for Advertising Cloud]](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/analytics/intro-a4adc.html)
>* [Voraussetzungen und Schlüsselinformationen für die Implementierung [!DNL Analytics for Advertising Cloud]](prerequisites.md)
>* [Von Analytics verwendete Advertising Cloud IDs](ids.md)
>* [JavaScript-Code für Analytics für Advertising Cloud](/help/integrations/analytics/javascript.md)
>* [Erwartete Datenabweichungen  [!DNL Analytics] zwischen und Advertising Cloud](data-variances.md)
>* [Advertising Cloud-Metriken in Analysis Workspace](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Daten in Advertising Cloud](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)

