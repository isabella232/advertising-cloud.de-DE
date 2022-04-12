---
title: Erstellen mehrerer Drittanbieteranzeigen
description: Erfahren Sie, wie Sie mehrere Anzeigen von Drittanbietern auf einmal erstellen.
feature: DSP Ads
exl-id: 83d35d27-1ab6-4fcf-877f-650a2dc6975a
source-git-commit: bcece4bfec6f8a765cced3ee230fd8cbf3055b7b
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# Erstellen mehrerer Drittanbieteranzeigen

Sie können bis zu 500 Anzeigen von Drittanbietern gleichzeitig erstellen, indem Sie Tags hochladen, die auf Kreativ-Assets verweisen, die auf Werbeservern von Drittanbietern gehostet werden. Sie können Tracking-Pixel für die Anzeigen einbeziehen.<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

Sie können entweder [!DNL DoubleClick] und [!DNL Flashtalking] Tagblätter oder eine manuell ausgefüllte Datei mit der bereitgestellten Vorlage.

>[!TIP]
>
> Die Best Practice ist die Verwendung von Drittanbieteranzeigen, die sicher über HTTPS bereitgestellt werden. URLs, die über HTTPS bereitgestellt werden, beginnen mit &quot;https&quot;.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne, in der die Anzeige enthalten sein soll.

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create]**. Klicken Sie im Abschnitt &quot;Anzeigentypen&quot;des Menüs auf **[!UICONTROL Bulk upload ads]**.

1. Wählen Sie den Adserver aus, auf dem die Anzeige gehostet wird: *[!UICONTROL DoubleClick]*, *[!UICONTROL Flashtalking]* oder *[!UICONTROL Other]*.

1. ([!DNL DoubleClick] und [!DNL Flashtalking] Anzeigen) Wählen Sie den Tag-Typ aus, der für jedes Video-Asset und jedes Display-Asset verwendet werden soll. Die verfügbaren Optionen variieren je nach Anzeigenserver.

1. (Anzeigen auf allen Anzeigen-Servern außer [!DNL DoubleClick] und [!DNL Flashtalking]) Klicken Sie auf **[!UICONTROL Download this template]** zum Herunterladen einer Vorlage in [!DNL Microsoft Excel] Tabellenformat (XLSX), das Sie mit Anzeigendaten füllen und lokal speichern können. Die erforderlichen Spalten enthalten [!UICONTROL Ad Name], [!UICONTROL VAST/VPAID URL or Ad Tag]und [!UICONTROL Ad Types].

1. Klicken **[!UICONTROL Upload]** und wählen Sie eine Datei im .xlsx- oder .xls-Format von Ihrem Gerät oder Netzwerk aus.

   Für [!DNL DoubleClick] und [!DNL Flashtalking] Anzeigen, laden Sie nicht bearbeitete Tag-Arbeitsblätter vom Anzeigen-Server hoch. Verwenden Sie für andere Adserver die Vorlage, die Sie in Schritt 3 heruntergeladen haben.

1. Klicken Sie nach Abschluss des Uploads auf **[!UICONTROL Start Building Ads]**.

1. Überprüfen Sie die Details und den Status jeder Anzeige:

   1. Überprüfen Sie den Status jeder Anzeige, der auf Validierungsprüfungen für das hochgeladene Tag basiert.
   1. (Optional) Führen Sie für jede Anzeige einen der folgenden Schritte aus:
      * Um eine Anzeige in der Vorschau anzuzeigen, klicken Sie auf ![play](/help/dsp/assets/play.png) in der Anzeigenzeile.
      * Um die Anzeigendetails zu bearbeiten, klicken Sie auf ![edit](/help/dsp/assets/edit.png), bearbeiten Sie die Details und klicken Sie auf **Speichern**.
      * Um eine Anzeige zu entfernen, klicken Sie auf **[!UICONTROL X]** in der Anzeigenzeile.

1. Klicken **[!UICONTROL Create *N *Anzeigen]**.

1. Führen Sie einen der folgenden Schritte aus:

   * Klicken **[!UICONTROL Done]**.

   * (Wenn eine Anzeige abgelehnt wird; optional) So bearbeiten Sie den Anzeigendatensatz und senden die Anzeige erneut zur Überprüfung:
      1. Klicken Sie auf den Anzeigennamen.
      1. Bearbeiten Sie die Anzeigeneinstellungen.
      1. Klicken **[!UICONTROL Save & submit for review]**.

>[!MORELIKETHIS]
>
>* [Über die Anzeigenverwaltung](ad-about.md)
>* [Anzeigenspezifikationen](ad-specs.md)
>* [Einzelne Anzeige erstellen](ad-create.md)
>* [Video: Massen-Upload von Anzeigen-Tags von Drittanbietern](https://experienceleague.adobe.com/docs/advertising-cloud-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html)

