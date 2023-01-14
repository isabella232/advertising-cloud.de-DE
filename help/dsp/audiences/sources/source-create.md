---
title: Erstellen einer Zielgruppenquelle zum Aktivieren von Erstanbieterzielgruppen
description: Erfahren Sie, wie Sie eine Quelle erstellen, um Zielgruppen in Ihr Konto oder ein Advertiser-Konto zu importieren.
feature: DSP Audiences
exl-id: 16eb7cdb-4364-4e94-ba73-0f2d4d200cb9
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# Erstellen einer Zielgruppenquelle zum Aktivieren von Erstanbieterzielgruppen

*Beta-Funktion*

<!-- Will this remain for admin users/Adobe account teams only? -->

Erstellen Sie eine Quelle, um Zielgruppen in Ihr DSP- oder Advertiser-Konto zu importieren. Derzeit können Sie Zielgruppen aus [die [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html).

>[!NOTE]
>
>Nachdem Sie eine Quelle für die [!DNL Real-Time CDP], müssen Sie Ihre [!DNL Real-Time CDP] Zielgruppen durch das Adobe Advertising DSP Ziel in [!DNL Real-Time CDP] um mit dem Import zu beginnen. Siehe [die Schritte im Aktivierungs-Workflow](source-about.md#workflow-sources).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences] > [!UICONTROL Sources (BETA)].

1. Klicken [!UICONTROL Add Source].

1. Im [!UICONTROL Select a Type] wählen Sie den Quelltyp aus.

   *[!UICONTROL RT-CDP]*: Dieser Quelltyp für [die [!DNL Adobe Real-Time Customer Data Profile]](source-about.md), ist die einzige Option.

1. Geben Sie die [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* oder *[!UICONTROL Account]*.

1. Geben Sie den Rest ein [Quelleinstellungen](source-settings.md).

   Eine Kopie der [!UICONTROL Source Key] wird generiert. Du wirst den Wert später benötigen.

1. Klicken **[!UICONTROL Save]**.

1. Erstellen Sie in Experience Platform mithilfe der Funktion [!UICONTROL Source Key] , die in den DSP-Quelleinstellungen generiert wurde.

Anweisungen zum Aktivieren der DSP-Zielverbindung, Auswählen von Segmenten und Zugreifen auf Kontrollberechtigungen finden Sie unter[Adobe Advertising Cloud DSP-Verbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

>[!MORELIKETHIS]
>
>* [Einstellungen der Zielgruppenquelle](source-settings.md)
>* [Informationen zum Aktivieren authentifizierter Segmente aus Zielgruppen-Quellen](source-about.md)
>* [Authentifizierte Segmente von dauerhaften ID-Partnern aktivieren](source-durable-id.md)<!-- title?-->
>* [Adobe Advertising Cloud DSP-Verbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)

