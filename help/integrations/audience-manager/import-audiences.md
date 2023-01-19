---
title: Importieren von Adobe Audience Manager-Segmenten für Anzeigen-Targeting
description: Erfahren Sie, wie Sie Ihre [!DNL Adobe] Zielgruppen in Advertising DSP und Suche mithilfe von Adobe Audience Manager
feature: Integration with Adobe Audience Manager
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '764'
ht-degree: 0%

---

# Importieren von Adobe Audience Manager-Segmenten für Anzeigen-Targeting

DSP und [!DNL Advertising Search] kann jedes Mal Metadaten, Hierarchiedaten und eindeutige Zielgruppendaten für alle Daten eines Advertisers oder einer Agentur abrufen [!DNL Adobe] Zielgruppen<!-- segments or audiences? Standardize terms per AAM's docs -->. Dazu gehören Daten für:

* Adobe Audience Manager-Segmente

* Adobe Analytics-Segmente, die in Adobe Experience Cloud veröffentlicht werden

* Segmente, die in Adobe Experience Cloud mit dem [!DNL People core service]

* Segmente, die in Adobe Experience Platform erstellt und über Audience Manager an Adobe Advertising gesendet werden

So greifen Sie auf [!DNL Adobe] Zielgruppen in DSP oder [!DNL Creative], müssen Sie die Zielgruppen in DSP importieren. So greifen Sie auf [!DNL Adobe] Zielgruppen in [!DNL [!DNL Search]], müssen Sie die Zielgruppen in [!DNL [!DNL Search]].

## Voraussetzungen

* Der Werbetreibende muss [die [!DNL Adobe Experience Cloud Identity (ECID) Service]](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html) Version 2.0 oder höher. Die [!DNL Identity Service] bietet eine universelle, beständige ID zum Identifizieren Ihrer Besucher über alle Lösungen in Experience Cloud hinweg.

   Die Implementierung umfasst das Hinzufügen der [!DNL Identity service] Code für jede Webseite auf den Websites des Werbetreibenden.

* Die Organisation muss [aktiviert für Experience Cloud Services](https://experienceleague.adobe.com/docs/core-services/interface/services/core-services.html) und über ein Experience Cloud verfügen [!DNL Organization ID] (zuvor [!DNL IMS org ID]).

   Die [!UICONTROL Organization ID] ermöglicht Unternehmen mit mehreren Adobe Experience Cloud-Produkten die gemeinsame Nutzung von Daten für einige der Produkte.

* (Werbetreibende mit [!DNL Analytics]) Der Advertiser muss [implementieren [!DNL Analytics] using `appMeasurement.js`](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html) Version 1.6.4 oder höher.

* Die Website-Besucher des Advertisers enthalten keine große Menge an [!DNL Apple Safari] Benutzer.

* (Wird empfohlen, wenn der Advertiser sowohl Audience Manager als auch [!DNL Analytics]) Um die Aufrufe auf jeder Webseite zu reduzieren, entfernen Sie vorhandenen Audience Manager [!DNL Data Integration Library] Code für die Datenerfassung und Aktivierung der serverseitigen Weiterleitung für jede [!DNL Analytics] Report Suite . Weitere Informationen finden Sie unter &quot;[Übersicht über die serverseitige Weiterleitung](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

* (Empfohlen) Für höhere Übereinstimmungsraten senden Sie nur Erstanbieter-Website-Daten an Adobe Advertising. Wenn der Advertiser Drittanbieterdaten oder Offline-Daten aus einem Customer Relationship Management-System bündelt, kann die Datenleckage die Übereinstimmungsraten reduzieren.

## Importieren von Audience Manager-Zielgruppen in DSP

### Schritte zum Importieren von Zielgruppen in DSP

Die [!DNL Adobe] Teams für Konto- und Datenoperationen führen die folgenden Schritte aus.

1. Die [!DNL Adobe] Account-Team sollte die Einstellung auf Advertiser-Ebene konfigurieren &quot;[!UICONTROL Adobe Analytics Cloud].&quot;

1. Die [!DNL Adobe] Kontoteam sollte eine Anfrage senden<!-- Submit a request as a JIRA task? --> an das Dateneinsatzteam<!-- implementation team? --> , um mithilfe der Advertising DSP nativen API-Integration die Audience Manager-Segmente des Unternehmens zu importieren.

### Welche Veränderungen führen zu Audience Manager?

Die API automatisch:

* Erstellt zwei DSP Ziele in Audience Manager:

   * **[!UICONTROL Adobe Ad Cloud Cross-Channel (real-time)]**

   * **[!UICONTROL Adobe AdCloud Cross-Channel (batch)])**

* Ordnet die beiden Ziele allen Audience Manager-Segmenten zu, sodass Audience Manager die Segmente für das DSP Advertiser-Konto freigeben können, das mit demselben Experience Cloud verknüpft ist [!DNL Organization ID] wird für den Audience Manager verwendet. <!-- Verify -->

   Das Unternehmen kann optional nicht benötigte Segmente aus den Zielen in Audience Manager entfernen.

* Fügt das folgende Pixel zur Cookie-Synchronisierung zum Audience Manager-Container des Unternehmens hinzu, um die Reichweite von Kundenkampagnen zu verbessern:

   * Adobe AdCloud: 411 (Dies ist standardmäßig und automatisch als Teil von [!DNL Identity Service] Version 2.0. Organisationen mit [!DNL Identity Service] -Versionen unter 2.0 sollten dieses Pixel ihrem Audience Manager-Container hinzufügen.

## Importieren von Audience Manager-Zielgruppen in [!DNL Search]

### Schritte zum Importieren von Zielgruppen in [!DNL Search]

[!DNL Adobe] Das Personal führt die meisten oder alle der folgenden Schritte aus.

1. Die [!DNL Adobe] Das Account-Team sollte eine Anfrage an das Dateneinsatzteam senden, um eine Integration zwischen [!DNL Search] und Audience Manager. Beziehen Sie die Namen der Audience Manager-Segmente ein, in die Sie exportieren möchten [!DNL Search].

1. Konfigurieren Sie in Audience Manager Ziele für [!DNL Search]:

   1. Erstellen Sie zwei neue Ziele: `[!UICONTROL Adobe Media Optimizer (HTTP)]` und `[!UICONTROL Adobe Media Optimizer Batch Destination]`.

      [!DNL Media Optimizer] ist ein früherer Name für [!DNL Search].

   1. Geben Sie die Segmente für die einzelnen Ziele an.

      Mit dem [!UICONTROL Automatically map all current and future segments] festgelegt ist, werden alle Segmente täglich zugeordnet und synchronisiert.

      Die [!UICONTROL Manually map segments] -Option können Sie die Segmente manuell der Synchronisierung mit dem Batch-Ziel zuordnen (`[!UICONTROL Adobe Media Optimizer Batch Destination]`). Es müssen keine Segmente manuell dem HTTP-Ziel zugeordnet werden.

1. Within [!DNL Search], entweder [!DNL Search] Implementierungs-Team oder ein Benutzer mit der Rolle &quot;Client-Manager mit direktem Zugriff&quot;sollte den Import von [!UICONTROL Search] > [!UICONTROL Admin] > [!UICONTROL Audience Manager Setup].

   Sie müssen das Experience Cloud der Organisation eingeben [!DNL Organization ID] ([!DNL IMS org ID]). Die Kennung muss mit der für das Audience Manager-Konto des Unternehmens verwendeten identisch sein.

### Welche Veränderungen führen zu Audience Manager?

Die Organisation sieht zwei [!DNL Search] Ziele in Audience Manager:

* **[!UICONTROL Adobe Media Optimizer (HTTP)]**
* **[!UICONTROL Adobe Media Optimizer Batch Destination])**

## Datensynchronisation

Der erste Import dauert etwa 24 Stunden. Nach dem ersten Import werden die Daten in Echtzeit mit einer Verzögerung von einer bis zwei Sekunden synchronisiert.

<!--
### How DSP Syncs the Data

DSP syncs the data automatically using the [!DNL Adobe Experience Cloud Identity (ECID) Service]. During synchronization, the [!DNL ECID Service] calls Adobe Advertising at [!DNL cm.eversttech.net]. Because Adobe Advertising is a trusted domain, ID syncs take place from parent pages rather than within the destination publishing iframes, as they do with most third-party activation partners. Audience Manager identifies unique users by device IDs, using the [Audience Manager [!DNL Unique User ID (AAM UUID)]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html#global-device-ids), also called the [!DNL Device ID].
 
![Synchronization of [!DNL Adobe] audiences in DSP](/help/integrations/assets/audience-manager-sync.png)

### How Search Syncs the Data
-->

<!-- 
Segment membership data is sent only after one of the following events occurs:

* (Advertisers with DSP):

  * The segment is targeted in an Adobe Advertising display ad.

  * The segment is added to the [!DNL Adobe AdCloud Cross-Channel] batch and real-time destinations within the Audience Manager user interface.

* (Advertisers with [!DNL Search]):

  * The segment is targeted in an Adobe Advertising search ad.

  * The segment is added to the [!DNL Adobe Media Optimizer] batch and HTTP destinations within the Audience Manager user interface.
 -->
<!-- Is membership data/whatever available in Creative? If so, does it show the same as DSP? -->

## Wo finden Sie Ihre synchronisierten Segmente?

### In DSP

In DSP werden Segmentnamen nach der Audience Manager-Taxonomie organisiert und stehen mit den entsprechenden Segmentmitgliedschaftszahlen in zur Verfügung:

* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md#audience-targeting): Im [!UICONTROL Adobe Segments] des [!UICONTROL Audience Targeting] Abschnitt.

* In [Zielgruppeneinstellungen](/help/dsp/audiences/audience-settings.md): Im [!UICONTROL Adobe Segments] Registerkarte.

### In Advertising Creative

In [!DNL Creative], sind die Segmente in den Erlebniseinstellungen für Zielknoten verfügbar.

### In [!DNL Advertising Search]

In [!DNL [!DNL Search]], sind die Segmente verfügbar, wenn Sie eine [!DNL Google] Zielgruppe, die [!UICONTROL Data Source] &quot;[!UICONTROL Adobe Audience]&quot; von [!UICONTROL Campaigns] > [!UICONTROL Audiences] > [!UICONTROL Library].

Für jeden [!DNL Google] von Ihnen erstellte Zielgruppen, [!DNL Google] stellt die Zielgruppengröße bereit.

>[!MORELIKETHIS]
>
>* [Adobe Advertising-Integrationen mit Adobe Audience Manager](/help/integrations/audience-manager/overview.md)

