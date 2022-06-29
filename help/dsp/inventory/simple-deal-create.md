---
title: '"Erstellen Sie eine [!UICONTROL Simple Ad Serving] Deal"'
description: '"Erfahren Sie, wie Sie ein Tracking-Pixel für eine [!UICONTROL Simple Ad Serving] handeln."'
feature: DSP Simple Ad Serving
exl-id: d8de85ec-616c-44ed-9a1a-cc25713ad4a4
source-git-commit: 089d91f7d1b06e29d27ac95a46834127d19c141d
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Erstellen Sie eine [!UICONTROL Simple Ad Serving] Deal

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create]** und wählen Sie **[!UICONTROL Simple Ad Serving]**.

1. Geben Sie die [Deal-Einstellungen](simple-deal-settings.md):

   1. Im [!UICONTROL Select Ad Source] , geben Sie Informationen zum Publisher, Advertiser, Kampagne und Anzeigentyp an und klicken Sie auf **[!UICONTROL Next]**.

   1. Im [!UICONTROL Select Ad(s)] -Abschnitt geben Sie eine Anzeige an, die in DSP als Proxy verwendet werden soll:

      1. Führen Sie einen der folgenden Schritte aus:

         * Wählen Sie für vorhandene Anzeigen die zu verwendenden Anzeigen aus.

         * Erstellen Sie für neue Anzeigen einen Proxy [Drittanbieteranzeige](/help/dsp/campaign-management/ads/ad-create-multiple.md).
      >[!NOTE]
      > DSP bedient nicht die von Ihnen angegebenen Anzeigen. Der Herausgeber stellt die Anzeige bereit.

      1. Klicken **[!UICONTROL Next]**.
   1. Bearbeiten Sie in den Feed-Details die Feed-Details und klicken Sie auf **[!UICONTROL Next]**.

      Advertising Cloud DSP generiert automatisch eine Platzierung mit dem Namen &quot;SAS Placement - &lt;*Name des Deals*>&quot;,&quot;für die Anzeige. In der Platzierung wird der Deal automatisch im [!UICONTROL Inventory Targets] Abschnitt. Alle anderen Targeting-Optionen sind nicht verfügbar.



1. Senden Sie die Ereignisverfolgungspixel zur Implementierung an den Herausgeber auf eine der folgenden Arten:

   * (Optional) Wählen Sie im [!UICONTROL Activate Tag with Publisher] -Bildschirm das Deal-Tag an den Herausgeber senden.

      Wenn Sie die vorherigen Schritte abgeschlossen haben, generiert DSP eine E-Mail-Nachricht, die Sie an den Herausgeber senden können. Die Nachricht enthält die Details des Deals, einen Link, aus dem das Deal-Tag abgerufen werden soll, und einen Autorisierungscode für den Link.

      1. Überprüfen Sie die Details des Deals und führen Sie dann einen der folgenden Schritte aus:

         * Um die Informationen in eine E-Mail-Nachricht in eine E-Mail-Anwendung auf Ihrem Gerät einzufügen, klicken Sie auf **[!UICONTROL Email & Done]** und wählen Sie die E-Mail-Anwendung aus. Die [!UICONTROL CC:] -Feld mit einer [!DNL Adobe] Support-Adresse. Sie können die Nachricht dann an den entsprechenden Kontakt für den Herausgeber senden.

         * Um die Informationen in die Zwischenablage zu kopieren, klicken Sie auf **[!UICONTROL Copy Email].** Anschließend können Sie den Inhalt manuell in eine E-Mail-Nachricht einfügen und an den entsprechenden Kontakt für den Herausgeber senden. Sie müssen eine Kopie (CC:) in `publisher-support-global@adobe.com`. Wenn Sie mit dem Kopieren der Nachricht fertig sind, klicken Sie auf **[!UICONTROL Email & Done]**.
      1. (Falls erforderlich) Nehmen Sie mit dem Herausgeber Kontakt auf, um zu sehen, ob das Tag die entsprechenden Makros enthält, damit das Tag mit dem Anzeigenserver des Herausgebers funktioniert.
   * (Optional) Senden Sie die Pixel für die Ereignisverfolgung manuell an den Herausgeber:

      1. In der Adresszeile im [!UICONTROL Deals] Ansicht, klicken Sie auf ![Optionen, Menü](/help/dsp/assets/options-menu.png) **>[!UICONTROL show pixel]**.

         Die Ereignispixel enthalten eine [!UICONTROL Clickthrough] Pixel und [!UICONTROL Impression] Pixel. Video- und Audioanzeigen enthalten auch Ereignis-Pixel nach Quartil (aus [!UICONTROL 25% Complete] nach [!UICONTROL 100% Complete]).

      1. Kopieren Sie die Pixel für die Ereignisverfolgung und stellen Sie sie Ihrem Herausgeber bereit.



>[!MORELIKETHIS]
>
>* [Info [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [[!UICONTROL Simple Ad Serving] Einstellungen](simple-deal-settings.md)
>* [Detaillierte Berichte für ein Angebot anzeigen](/help/dsp/inventory/deal-view-report.md)


<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
