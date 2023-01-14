---
title: Informationen zum Aktivieren authentifizierter Segmente aus Zielgruppen-Quellen
description: Erfahren Sie mehr über die Aufnahme von Erstanbietersegmenten aus einer Kundendatenplattform.
feature: DSP Audiences
exl-id: 3e6ede23-2b27-4b1d-bfa2-e823824633c4
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Informationen zum Aktivieren authentifizierter Segmente aus Zielgruppen-Quellen

<!-- Doesn't specifically explain what you can do in our UI -->
*Beta-Funktion*

DSP können Erstanbietersegmente erfassen, die aus authentifizierten Signalen bestehen, die in einer Kundendatenplattform (CDP) erstellt wurden. Sie können die aufgenommenen Segmente als Ziele für Ihre Platzierungen verwenden.

## [!DNL Adobe Real-Time Customer Data Profile]

DSP ist in die [die [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html), der Teil der Adobe Experience Platform ist.

In [!DNL Real-time CDP], *Ziele* sind Verbindungen zu externen Datenplattformen, die eine nahtlose Datenaktivierung ermöglichen. Beispielsweise können Sie Ziele verwenden, um Ihre bekannten Kundenbeziehungen (z. B. Hash-E-Mail-Adressen) für gezielte Werbung in digitalen Formaten zu aktivieren, die von DSP unterstützt werden.

Weitere Informationen zu Zielen finden Sie in der Experience Platform [Zielhandbuch](https://experienceleague.adobe.com/docs/experience-platform/destinations/home.html), einschließlich einer Übersicht über das Produkt, Anweisungen für [Erstellen von Ziel-Arbeitsbereichen](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/destinations-workspace.html) und [Erstellen von Zielverbindungen](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html)und [Aktivieren von Daten für Ziele](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/activate-segment-streaming-destinations.html).

### Workflow für die Verwendung der DSP Integration mit [!DNL Real-time CDP] {#workflow-sources}

<!-- Make sure that titles make the distinctions clear -- everything can't be "Activate XXX." -->

1. [Übersetzen von Kundendatensegmenten in DSP [!DNL LiveRamp RampIDs]](source-durable-id.md) die in einer bidbaren Umgebung erkennbar sind.<!-- I don't think I need this here: This requires DSP account-level and campaign-level settings to enable segment sharing with [!DNL LiveRamp], which will translate customer data to [!DNL RampIDs] to create targetable segments. Your DSP account team will perform this configuration. -->

1. [Erstellen einer Zielgruppenquelle](source-create.md) , um Zielgruppen in Ihr DSP- oder Advertiser-Konto zu importieren.

1. [Konfigurieren Sie eine [!DNL Real-Time CDP] Zielverbindung in Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).

Weitere Unterstützung erhalten Sie bei Ihrem [!DNL Adobe] Kontoteam oder `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Authentifizierte Segmente von dauerhaften ID-Partnern aktivieren](source-durable-id.md)
>* [Erstellen einer Zielgruppenquelle zum Aktivieren von Erstanbieterzielgruppen](source-create.md)
>* [Einstellungen der Zielgruppenquelle](source-settings.md)
>* [Adobe Advertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [Zielkatalog - Übersicht](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)

