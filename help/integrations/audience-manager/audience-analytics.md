---
title: '''[!DNL Adobe] [!DNL Audience Analytics] für Adobe Advertising-Kunden'
description: Erfahren Sie, wie Sie [!DNL Adobe] [!DNL Audience Analytics] Anwendungsfälle für Werbung
feature: Integration with Adobe Audience Manager
exl-id: e05ba560-d3d5-4024-b1ba-956e878a2578
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 0%

---

# [!DNL Adobe] [!DNL Audience Analytics] für Adobe Advertising-Kunden

[[!DNL Adobe] [!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) ist eine Integration zwischen Adobe Audience Manager und Adobe Analytics, durch die Audience Manager Segmente an senden können. [!DNL Analytics] für erweiterte Einblicke in die Site-Aktivität.

Adobe Advertising-Kunden können von der Verwendung von [!DNL Audience Analytics]. Die Integration ermöglicht Ihnen Folgendes:

* Senden von Adobe Advertising-Belichtungsdaten direkt an [!DNL Analytics] um die Auswirkungen der Aktivität des oberen Trichters auf die nachgelagerte Site-Aktivität zu ermitteln.

* Bestimmen Sie die Marketing-Kanäle und Site-Einstiegspunkte aus Anzeigen zur oberen Trichterexposition.

* Integration deklarieren mit [!DNL Analytics for Advertising] , um demografische Segmente von Drittanbietern aus zu integrieren. [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) mit [!DNL Analytics for Advertising] Daten für weitere Einblicke in Benutzerprofile.

   [!DNL Audience Marketplace] bietet Zugriff auf Drittanbieter-Daten-Feeds mit Abonnementmodellen &quot;Aktivierung&quot;, mit denen Käufer Daten an ein Ziel senden können. Wenn die Daten in einer [!DNL Analytics] Ziel, dann werden keine Aktivierungsgebühren erhoben.

* (Advertiser mit Advertising DSP) Fügen Sie zusätzliche Expositionssegmente für Einblicke in das ganzheitliche Journey-Management hinzu.

   Advertising DSP können Belichtungsdaten als umsetzbare Signale an Audience Manager senden, indem Adobe Experience Platform- oder Audience Manager-Impressions-Tracking-Pixel implementiert werden. Senden der gleichen Daten an [!DNL Analytics] ermöglicht die erweiterte Datenanalyse. Siehe[Übersicht über die Adobe Advertising Media-Datenintegration mit Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot;.

Weitere Informationen finden Sie unter [!DNL Audience Analytics], einschließlich der Voraussetzungen und des Workflows, siehe[Übersicht über Audience Analytics](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html).&quot;

## Beispiele für die Verwendung [!DNL Audience Analytics] Daten mit Adobe Advertising-Daten

Im Folgenden finden Sie Beispiele für die Verwendung der kombinierten Daten in [!DNL Analytics] [!DNL Analysis Workspace].

### Auswirkungen der Aktivität &quot;Oberer Trichter&quot;auf die nachgelagerte Aktivität anzeigen

Verwenden Sie Expositionssegmente der Audience Manager, um die Auswirkungen der Site-Aktivität des oberen Trichters auf die nachgelagerte Site-Aktivität zu sehen. Fügen Sie Adobe Advertising oder Makro-IDs von Drittanbietern in Ihre Tracking-Pixel ein, um die Auswirkungen auf einer detaillierten Ebene zu verfolgen, von der Kampagnenebene bis zur Ebene der Site, auf der der Benutzer verfügbar war.

Hauptvorteile:

* Tracking der Belichtung nach Trichter-/Anzeigentypen und Verwendung [!DNL Audience Analytics] zur Bestimmung der Einstiegsraten und Überschneidungen mit der nächsten Phase der Journey.

* Ermitteln Sie die Auswirkungen der Aktivität des oberen Trichters auf die nachgelagerte Site-Aktivität.

* Verbinden [!DNL Analytics for Advertising]<!-- which doesn't include the last exposure event --> und [!DNL Audience Analytics] data <!-- (which includes the user's last exposure event) --> , um eine ganzheitliche Journey zu bestimmen.

Im Folgenden finden Sie Beispiele für Berichte, die Sie in [!DNL Analysis Workspace].

![Auswirkungen der Aktivität des oberen Trichters auf die nachgelagerte Site-Aktivität](/help/integrations/assets/audience-analytics-upper-funnel-exposure.png)

### Verwendung [!DNL Audience Analytics] Drittanbieter-Segmentdaten für die Benutzerprofilanalyse

Verwenden Sie Audience Manager von Drittanbietern, um eine genauere Analyse der Interaktion der Benutzer mit Ihrer Site zu erhalten. Mithilfe der Informationen können Sie neue Zielgruppen von Drittanbietern bestimmen, für die Medien aktiviert werden sollen. Dies hängt davon ab, wie Profile aus Drittanbietersegmenten mit wichtigen Leistungsindikatoren für die Sites von Medienkampagnen interagieren.

>[!TIP]
> Verwenden des Audience Managers `Audiences ID` und `Audiences Name` -Dimensionen [!DNL Analytics]wie alle anderen Dimensionen, die [!DNL Analytics] erfasst.

Im Folgenden finden Sie Beispiele für Berichte, die Sie in [!DNL Analysis Workspace].

![Verwenden von Drittanbietersegmenten zur Anreicherung der Benutzerprofilanalyse](/help/integrations/assets/audience-analytics-third-party-report.png)

>[!MORELIKETHIS]
>
>* [Adobe Advertising-Integrationen mit Adobe Audience Manager](/help/integrations/audience-manager/overview.md)

