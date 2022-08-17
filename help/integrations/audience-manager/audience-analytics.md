---
title: '"[!DNL Adobe][!DNL Audience Analytics] für Advertising Cloud-Kunden"'
description: Erfahren Sie, wie Sie [!DNL Adobe][!DNL Audience Analytics] Anwendungsfälle für Werbung
feature: Integration with Adobe Audience Manager
source-git-commit: d83e36847d0e14bc7e83106c0a221680060c2e58
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# [!DNL Adobe][!DNL Adobe] für Advertising Cloud-Kunden

[[!DNL Adobe][!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) ist eine Integration zwischen Adobe Audience Manager und Adobe Analytics, durch die Audience Manager Segmente an senden können. [!DNL Analytics] für erweiterte Einblicke in die Site-Aktivität.

Advertising Cloud-Kunden profitieren von der Verwendung von [!DNL Audience Analytics]. Die Integration ermöglicht Ihnen Folgendes:

* Senden von Advertising Cloud-Belichtungsdaten direkt an [!DNL Analytics] um die Auswirkungen der Aktivität des oberen Trichters auf die nachgelagerte Site-Aktivität zu ermitteln.

* Bestimmen Sie die Marketing-Kanäle und Site-Einstiegspunkte aus Anzeigen zur oberen Trichterexposition.

* Integration deklarieren mit [!DNL Analytics for Advertising Cloud] , um demografische Segmente von Drittanbietern aus zu integrieren. [Audience Manager [!DNL Audience Marketplace]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/audience-marketplace/audience-marketplace.html) mit [!DNL Analytics for Advertising Cloud] Daten für weitere Einblicke in Benutzerprofile.

   [!DNL Audience Marketplace] bietet Zugriff auf Drittanbieter-Daten-Feeds mit Abonnementmodellen &quot;Aktivierung&quot;, mit denen Käufer Daten an ein Ziel senden können. Wenn die Daten in einer [!DNL Analytics] Ziel, dann werden keine Aktivierungsgebühren erhoben.

* (Werbetreibende mit Advertising Cloud DSP) Fügen Sie zusätzliche Expositionssegmente für Einblicke in das ganzheitliche Journey-Management hinzu.

   Advertising Cloud DSP kann Belichtungsdaten als umsetzbare Signale an Audience Manager senden, indem Adobe Experience Platform- oder Audience Manager-Impressions-Tracking-Pixel implementiert werden. Senden der gleichen Daten an [!DNL Analytics] ermöglicht die erweiterte Datenanalyse. Siehe[Überblick über die Integration von Advertising Cloud-Mediendaten mit Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot;.

Weitere Informationen finden Sie unter [!DNL Audience Analytics], einschließlich der Voraussetzungen und des Workflows, siehe[Übersicht über Audience Analytics](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html).&quot;

## Beispiele für die Verwendung [!DNL Audience Analytics] Daten mit Advertising Cloud-Daten

Im Folgenden finden Sie Beispiele für die Verwendung der kombinierten Daten in [!DNL Analytics] [!DNL Analysis Workspace].

### Auswirkungen der Aktivität &quot;Oberer Trichter&quot;auf die nachgelagerte Aktivität anzeigen

Verwenden Sie Expositionssegmente der Audience Manager, um die Auswirkungen der Aktivität der oberen Trichtersite auf die nachgelagerte Site-Aktivität zu sehen. Schließen Sie Advertising Cloud- oder Drittanbieter-Makro-IDs in Ihre Tracking-Pixel ein, um die Auswirkungen auf einer detaillierten Ebene von der Kampagnenebene bis zur Ebene der Site zu verfolgen, auf der der Benutzer verfügbar war.

Hauptvorteile:

* Tracking der Belichtung nach Trichter-/Anzeigentypen und Verwendung [!DNL Audience Analytics] zur Bestimmung der Einstiegsraten und Überschneidungen mit der nächsten Phase der Journey.

* Ermitteln Sie die Auswirkungen der Aktivität des oberen Trichters auf die nachgelagerte Site-Aktivität.

* Verbinden [!DNL Analytics for Advertising Cloud]<!-- which doesn't include the last exposure event --> und [!DNL Audience Analytics] data <!-- (which includes the user's last exposure event) --> , um eine ganzheitliche Journey zu bestimmen.

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
>* [Advertising Cloud-Integrationen mit Adobe Audience Manager](/help/integrations/audience-manager/overview.md)

