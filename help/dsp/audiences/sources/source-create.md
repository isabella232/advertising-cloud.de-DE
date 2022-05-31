---
title: Erstellen einer Zielgruppenquelle zum Aktivieren von Erstanbieterzielgruppen
description: Erfahren Sie, wie Sie eine Quelle erstellen, um Zielgruppen in Ihr Konto oder ein Advertiser-Konto zu importieren.
feature: DSP Audiences
source-git-commit: d1ebbd79b6ccf0249829feef134122f083060563
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 0%

---

# Erstellen einer Zielgruppenquelle zum Aktivieren von Erstanbieterzielgruppen

*Beta-Funktion*

<!-- Will this remain for admin users/Adobe account teams only? -->

Erstellen Sie eine Quelle, um Zielgruppen in Ihr DSP- oder Advertiser-Konto zu importieren. Derzeit können Sie Zielgruppen aus [die [!DNL Adobe Real-Time Customer Data Profile (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html).

>[!NOTE]
>
>Nachdem Sie eine Quelle für die [!DNL Real-Time CDP], müssen Sie Ihre [!DNL Real-Time CDP] Zielgruppen durch das Adobe Advertising Cloud DSP-Ziel in [!DNL Real-Time CDP] um mit dem Import zu beginnen. Siehe [die Schritte im Aktivierungs-Workflow](source-about.md#workflow-sources).

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences] > [!UICONTROL Sources (BETA)].

1. Klicken [!UICONTROL Add Source].

1. Im [!UICONTROL Select a Type] wählen Sie den Quelltyp aus.

   *[!UICONTROL RT-CDP]*: Dieser Quelltyp für [die [!DNL Adobe Real-Time Customer Data Profile]](source-about.md), ist die einzige Option.

1. Geben Sie die [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* oder *[!UICONTROL Account]*.

1. Geben Sie den Rest ein [Quelleinstellungen](source-settings.md).

   Eine Kopie der [!UICONTROL Source Key] wird generiert. Du wirst den Wert später benötigen.

1. Klicken **[!UICONTROL Save]**.

1. Erstellen Sie in Experience Platform eine Adobe Advertising Cloud DSP-Zielverbindung mit dem [!UICONTROL Source Key] , die in den DSP-Quelleinstellungen generiert wurde.

Anweisungen zum Aktivieren der Advertising Cloud-Zielverbindung, Auswählen von Segmenten und Zugreifen auf Kontrollberechtigungen finden Sie unter[Adobe Advertising Cloud DSP-Verbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).&quot;

>[!MORELIKETHIS]
>
>* [Einstellungen der Zielgruppenquelle](source-settings.md)
>* [Informationen zum Aktivieren authentifizierter Segmente aus Zielgruppen-Quellen](source-about.md)
>* [Authentifizierte Segmente von dauerhaften ID-Partnern aktivieren](source-durable-id.md)<!-- title?-->
>* [Adobe Advertising Cloud DSP-Verbindung](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)

