---
title: Übersicht über das Senden von DSP-Exposure-Daten an Adobe Audience Manager
description: Erfahren Sie, wie Sie mit Audience Manager-Ereignispixel Impressions- und Klickdaten aus Advertising DSP Kampagnen erfassen können.
feature: Integration with Adobe Audience Manager
exl-id: 916b7deb-511e-4fbf-96d9-b274a48dc748
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Übersicht über das Senden von DSP-Exposure-Daten an Adobe Audience Manager

*Advertiser nur mit Advertising DSP*

*Werbetreibende mit nur einer Adobe Advertising-Adobe Audience Manager-Integration*

Advertising DSP Kunden mit Adobe Audience Manager können Audience Manager-Ereignispixel verwenden, um Daten auf Impressionsebene und Klickdaten aus DSP Kampagnen zu erfassen. Die Ereignispixel senden die Daten als umsetzbare Signale an den Audience Manager. Diese Signale ermöglichen verschiedene DSP Anwendungsfälle, z. B. erweiterte Segmentierung, Frequenzverwaltung, Marketing-Analyse und Reporting-Einblicke.

DSP lädt Sie nicht dazu ein, diese Signale an den Audience Manager zu senden. Sie zahlen jedoch die standardmäßigen Audience Manager-Erfassungskosten basierend auf Server-Aufrufen gemäß Ihrem Audience Manager-Vertrag. Audience Manager entfernt doppelte Ereignisse, die auf zwei verschiedene Arten verfolgt werden, sodass jedes Ereignis nur einmal geladen wird.

>[!NOTE]
>
> Audience Manager unterstützt auch die Erfassung von Daten aus Adserver-Protokolldateien, was weniger Flexibilität bietet. Dieser Prozess wird in dieser Dokumentation nicht behandelt.

## Primäre Vorteile

* DSP Kampagnendaten fließen in Echtzeit in den Audience Manager und Sie können sie zum Erstellen regelbasierter Eigenschaften verwenden, mit denen Sie Segmente definieren.

* Segmente sind unmittelbar nach der Benutzer- und Segmentqualifikation für das Targeting verfügbar, wodurch Echtzeit-Targeting gefördert wird.

* Sie können die Kampagnendaten für Anwendungsfälle wie Frequenzlimitierung für kreative Kreativinhalte, Retargeting von Benutzern, die früheren Kampagnen ausgesetzt waren, und Analyse des nachgelagerten Site-Verhaltens und der Einstiegspunkte nutzen.

* Die aggregierten Daten bieten eine einheitliche Ansicht der Kampagnenleistung, helfen bei der Identifizierung benutzerdefinierter Konversionspfade und können zur Verbesserung der Ereignissequenz verwendet werden, die über den Audience Manager zu Konversionen führt [!DNL Audience Optimization Reports] oder durch [[!DNL Audience Analytics] Integration mit Adobe Analytics](/help/integrations/audience-manager/audience-analytics.md).

## Tracking der Daten

Die Audience Manager-Impressions- und Klickereignis-Pixel sind Cookie-basiert. Die Pixel erfassen keine Ereignisse, die in Cookie-losen Umgebungen wie mobilen Apps und vernetztem TV (CTV) auftreten.

### Impression-Tracking-Pixel

Audience Manager verfolgt Impressionsdaten für eine Anzeige, wenn Sie ein transparentes Ereignis-Tracking-Pixel mit einer Größe von 1,5 Pixel an die Anzeige anhängen. Das Ereignis-Pixel wird jedes Mal geladen, wenn die Anzeige einem Benutzer bereitgestellt und vom Webbrowser geladen wird. Das Pixel wird aus einer clientspezifischen Subdomäne von [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), die eine veraltete Domäne für Audience Manager ist und Parameter als Schlüssel-Wert-Paare enthält. Der Ereignisaufruf erfasst Impressions- und Konversionsdaten und sendet sie an die Datenerfassungsserver des Audience Managers.

### Klick-Tracking-Pixel

Audience Manager verfolgt Klicks ähnlich wie Impressionen, allerdings wird das transparente Ereignispixel nicht jedes Mal geladen, wenn die Anzeige bereitgestellt wird. Stattdessen werden die Klickdaten in der Clickthrough-URL der Anzeige verfolgt. Die Anzeige verweist auf eine clientspezifische Subdomäne von [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html), eine veraltete Domäne für Audience Manager, zur Verarbeitung durch die Datenerfassungsserver des Audience Managers. Der Server leitet den Benutzer dann zur gewünschten Landingpage weiter. Die URL enthält Parameter als Schlüssel-Wert-Paare.

>[!NOTE]
>
>Wenn Ihr Unternehmen [!DNL Analytics] -Tracking verwenden, ist möglicherweise kein Klick-Tracking für Audience Manager erforderlich. Adobe Analytics erfasst Klicksignale und kann sie an den Audience Manager senden, indem [serverseitige Weiterleitung](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

>[!MORELIKETHIS]
>
>* [Erfassen von Klick- und Impressionsdaten aus Advertising DSP Kampagnen](collect.md)
>* [Nutzungsszenarios](use-cases.md)

