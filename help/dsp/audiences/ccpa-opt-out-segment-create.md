---
title: Erstellen und Implementieren eines CCPA-Opt-out-of-Sale-Segments
description: Erfahren Sie, wie Sie ein Segment erstellen und implementieren, um Benutzer-IDs aus Kunden-Opt-out-Kaufanfragen zu verfolgen.
feature: CCPA, Segments
exl-id: aebe0c5b-382f-4e4a-b145-c32f32d216ca
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 0%

---

# Erstellen und Implementieren eines CCPA-Opt-out-of-Sale-Segments

Sie können ein Segment erstellen, um Benutzer-IDs aus Opt-out-Kaufanfragen von Verbrauchern auf Ihrer Website gemäß dem California Consumer Privacy Act (CCPA) zu verfolgen. Benutzer bleiben unbegrenzt in CCPA-Opt-out-Segmenten.

Sobald das Segment-Pixel-Tag implementiert ist, beginnt Advertising Cloud mit der Erfassung eines Pools von IDs im Namen des Advertisers.

>[!NOTE]
>
>* Informationen zur Kommunikation von CCPA-Opt-out-of-Sale-Anfragen an Advertising Cloud mithilfe der Adobe Experience Platform Privacy Service-API finden Sie unter [https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html).
>* Um Benutzer zu verfolgen, die Webseiten zu Zwecken besuchen, die nicht mit dem Tracking von CCPA-Opt-out-Kaufereignissen in Verbindung stehen, sowie Benutzer, die Anzeigen von Desktop-, Mobil- und CTV-Geräten ausgesetzt sind, erstellen Sie ein [benutzerdefiniertes Segment](/help/dsp/audiences/custom-segment-create.md).


1. Erstellen Sie das Segment:

   1. Klicken Sie im Hauptmenü auf **Zielgruppen > Segmente**.

   1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create]**.

   1. Geben Sie einen eindeutigen **[!UICONTROL Segment Name]** ein.

      Empfohlener Segmentname: &quot;&lt;*Ihr Advertiser-Name* - CCPA Opt-out of Sale&quot;(z. B. &quot;Acme - CCPA Opt-out of Sale&quot;)

   1. Wählen Sie für [!UICONTROL Segment Type] **[!UICONTROL CCPA Opt-out of sale]** aus.

   1. Klicken **[!UICONTROL Save]**.

1. Kopieren Sie ein Pixel-Tag und implementieren Sie es, um das Segment zu verfolgen:

   1. Kehren Sie zu **[!UICONTROL Audiences]>[!UICONTROL Segments]** zurück.

   1. Halten Sie in der Segmentzeile den Cursor über das neue Segment und klicken Sie auf **[!UICONTROL Get pixel]**.

   1. Kopieren Sie das Bildpixel (beginnend mit `<img src="https://rtd-tm.everesttech.net"`), um Benutzer-IDs von Desktop- und mobilen Besuchern auf eine Webseite zu erfassen.

   1. Stellen Sie das Tag dem Advertiser oder Website-Kontakt für die Bereitstellung zur Verfügung. Verwenden Sie dazu den Mechanismus, den das Unternehmen verwendet, um CCPA-Opt-out-Anfragen für den Verkauf zu verfolgen (z. B. die Verwendung einer Consent Management Platform).

      Möglicherweise muss die IT-Abteilung des Werbetreibenden oder eine andere Gruppe die Tag-Bereitstellung planen oder darüber informiert werden.

      Sobald das Pixel implementiert ist, beginnt Advertising Cloud mit der Erfassung eines Pools von IDs im Namen des Werbetreibenden.

      Obwohl die Wahl und Logik der Implementierung dem Advertiser obliegt, hier ein Beispiel dafür, wie ein Advertiser das Pixel auslösen kann:

      1. Ein Verbraucher landet auf der Homepage des Werbetreibenden.
      1. Der Verbraucher findet die Schaltfläche &quot;CCPA-Opt-out vom Verkauf&quot;des Werbetreibenden und klickt darauf.
      1. Dem Verbraucher wird eine Liste der Dienstleister angezeigt, mit denen der Werber arbeitet.
      1. Der Verbraucher prüft das Kontrollkästchen, um den Verkauf von Daten an Adobe Advertising Cloud abzuwählen.

         Diese Aktion Trigger das Pixel, das ausgelöst und die Cookie-ID des Verbrauchers innerhalb des angegebenen Segments &quot;[!UICONTROL CCPA Opt-out of sale]&quot;erfasst werden soll.

>[!MORELIKETHIS]
>
>* [Adobe Advertising Cloud-Unterstützung für den California Consumer Privacy Act: Opt-out-Support für Verbraucher](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html)
>* [Über  [!UICONTROL CCPA Opt-out-of-Sale] Segmente und Berichte](ccpa-opt-out-about.md)
>* [Abruf von Kundenabmeldeberichten](ccpa-opt-out-segment-report-retrieve.md)
>* [Erstellen und Implementieren eines benutzerdefinierten Segments](custom-segment-create.md)
>* [Über Zielgruppen-Management](audience-about.md)

