---
title: Nutzungsszenarios
description: Erfahren Sie mehr über Anwendungsfälle für die Freigabe Ihrer Advertising DSP Mediendaten für Audience Manager.
feature: Integration with Adobe Audience Manager
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 0%

---

# Nutzungsszenarios für die Erfassung von Daten zur Exposition von Medien in Adobe Audience Manager

*Advertiser nur mit Advertising DSP*

*Werbetreibende mit nur einer Adobe Advertising-Adobe Audience Manager-Integration*

Im Folgenden finden Sie einige Möglichkeiten, wie Sie von der Erfassung Ihrer Daten zur Anzeige DSP Medien profitieren können <!-- ad impression data? --> in Audience Manager.

## Neuigkeit und Frequenzverwaltung

Durch die Erfassung von Impressionsdaten in Audience Manager können Sie Ihr Frequenzmanagement verbessern, indem Sie Benutzersegmente erstellen, die einer bestimmten Anzeige oder Kampagne ausgesetzt waren. Sie können diese Segmente für Anzeigen-Targeting verwenden, wenn Sie die Häufigkeit erhöhen möchten, oder für die Unterdrückung von Anzeigen, wenn Sie die Häufigkeit begrenzen möchten.

Auch mit Audience Manager [!DNL Segment Builder]können Sie [Neuigkeit und Frequenzkontrollen](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html) auf [regelbasierte Eigenschaften](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) die aussagekräftige Signale enthalten. So können Sie z. B. die Anzahl der Wiedergaben eines bestimmten Kreativelements innerhalb einer Medienkampagne auf einen Benutzer begrenzen. Lesen Sie &quot;[Sofortige geräteübergreifende Unterdrückung](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html)&quot;, um zu erfahren, wie das geht.<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## Sequenzielles Messaging

Durch die Erfassung von Impressionsdaten können Sie ein Segment von Benutzern erstellen, die einer Kampagne oder Anzeige ausgesetzt waren, und dieses Segment für sequenzielles Messaging oder Unterdrückung verwenden. Sie können beispielsweise Benutzer, die kreative Inhalte gesehen haben, erneut ansprechen `123` aber nicht geklickt oder konvertiert haben, indem sie ihnen kreative `456`.

Gehen Sie wie folgt vor, um dieses Beispiel in Audience Manager auszuführen:<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. Erstellen Sie eine Eigenschaft, um Benutzer zu erfassen, die das Kreativ gesehen haben.

   Um beispielsweise die Eigenschaft zu benennen `Creative Trait 123`verwenden Sie die folgende Eigenschaftsregel:

   `d_creative == 123 AND d_event == imp`

1. Erstellen Sie eine Eigenschaft, um Benutzer zu erfassen, die klicken oder konvertieren.

   Um diese Eigenschaft beispielsweise zu benennen `Click and Converter`verwenden Sie die folgende Eigenschaftsregel:

   `d_event == click OR d_event=conv`

1. Erstellen Sie ein Segment mit dem Namen `Retarget Users` , um mit Benutzern zu füllen, die kreative Inhalte gesehen haben `123` aber nicht geklickt oder konvertiert haben. Verwenden Sie die folgende Eigenschaftsregel:

   `Creative Trait 123 AND NOT Click and Converter`

1. Segment zuordnen `Retarget Users` zu einem Ziel zu gelangen und Benutzer mit kreativen Elementen im Ziel anzusprechen `456`.

## [!DNL Adobe Audience Analytics] und Daten zur Campaign-Exposition

Sobald Kampagnendaten für Impressions- und Klickdaten in Audience Manager verfügbar sind, können Sie Eigenschaften und Benutzersegmente erstellen, die einer bestimmten Kampagne oder Taktik ausgesetzt waren oder damit interagiert wurden. Mit [[!DNL Audience Analytics] Integration](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html), können Ihre Audience Manager-Segmente mit [!DNL Analytics] für weitere Analysen. Mögliche Anwendungsfälle sind:

* **Interaktionsanalyse zwischen DSP und [!DNL Adobe Advertising Search] Anzeigen:** Der Standard [[!DNL Analytics for Advertising] Integration](/help/integrations/analytics/overview.md) bietet keine Einblicke in die Interaktion zwischen DSP und [!DNL [!DNL Search]], da beide Kanäle AMO-IDs verwenden, die den AMO-ID-Attributionsregeln entsprechen, für die ein Suchklick eine Durchsicht der Anzeige außer Kraft setzt. Durch Erstellung eines DSP Belichtungssegments in Audience Manager können Sie [!DNL Audience Analytics] zur Analyse der Interaktion zwischen DSP und [!DNL [!DNL Search]] Anzeigen in [!DNL Analytics].

* **Häufigkeitsanalyse:** Sie können in Audience Manager Segmente erstellen, die darauf basieren, wie oft ein Benutzer einer bestimmten Anzeige oder Kampagne ausgesetzt war. Anschließend können Sie die verschiedenen Belichtungssegmente in Analytics analysieren, um festzustellen, wie sich das Benutzerverhalten in Abhängigkeit von der Anzahl DSP Belichtungen ändert.

## [!DNL Audience Optimization Reports]

Sie können [Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html) , um potenzielle Leistungsmöglichkeiten für Segmente in Ihren Kampagnen zu ermitteln. Diese Berichte kombinieren Kampagnenimpressions-, Klick- und Konversionsdaten mit Segmentmetriken, um segmentorientierte Optimierungen und einen effektiven Kanalmix zu erhalten.

### Typen relevanter Audience Optimizationen-Berichte

| Bericht | Beschreibung |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] Bericht](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html) | Vergleicht zugeordnete und nicht zugeordnete Segmente nach Impressionen und Konversionsraten. |
| [[!UICONTROL Trend Analysis and Volume Analysis] Berichte]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html) | Gibt Daten zu Impressionen, Clickthrough-Raten und Konversionen für eine breite Palette von Werbedimensionen zurück. |
| [[!UICONTROL Optimal Frequency] Bericht](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html) | Hilft Ihnen, das optimale Gleichgewicht zwischen der Anzahl der bereitgestellten Impressionen und Konversionen zu ermitteln. Damit können Sie die Anzahl der Impressionen anpassen, die angezeigt werden sollen, bevor Sie beginnen, rückläufige Erträge zu sehen. |
| [[!UICONTROL Unique User Reach] Bericht](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html) | Ein Punktdiagramm, in dem jede Blase im direkten Verhältnis zur Anzahl der Unique Users für die ausgewählte Dimension skaliert wird. |

### Überlegungen

* Wenn [!DNL Audience Optimization Reports] Benutzer verfügen über rollenbasierte Zugriffskontrollen (RBAC), und [!DNL Adobe Customer Care] muss eine Zuordnung zwischen der Advertiser-ID und dem Audience Manager-Integrationscode der Organisation konfigurieren. Administratoren können dann RBAC-Berechtigungen für verschiedene Benutzer bereitstellen.

* Konversionsberichte in [!DNL Audience Optimization Reports] erfordert eine Einrichtung durch den Endbenutzer. Benutzer müssen Metadatendateien ausfüllen.

* [!DNL Audience Optimization Reports] unterstützt keine Änderungen an Kampagnen-Metadaten (z. B. Kampagnenname oder Platzierungsname).

* Klicks auf Suchanzeigen sind in [!DNL Audience Optimization Reports] nur, wenn sie mit Impressionen korreliert werden. Mit anderen Worten: Suchklicks werden als Konversionen infolge von Impressionen behandelt. Daher sind viele Suchklicks möglicherweise nicht in [!DNL Audience Optimization Reports].

>[!MORELIKETHIS]
>
>* [Übersicht über das Senden von DSP-Exposure-Daten an Adobe Audience Manager](overview.md)
>* [Erfassen von Klick- und Impressionsdaten aus Advertising DSP Kampagnen](collect.md)

