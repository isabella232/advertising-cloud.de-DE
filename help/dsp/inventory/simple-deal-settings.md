---
title: '''[!UICONTROL Simple Ad Serving] Deal Settings'''
description: Erfahren Sie mehr über die verfügbaren Einstellungen für [!UICONTROL Simple Ad Serving] Angebote.
feature: DSP Simple Ad Serving
exl-id: 1a8f215c-c52b-4099-a55f-99c4232b7a22
source-git-commit: 3eb63e9d7161c354736ce53ee21518882c541884
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# [!UICONTROL Simple Ad Serving] Deal Settings

## Neu [!UICONTROL Simple Ad Serving] Angebote

### [!UICONTROL Select Ad Source]

| Parameter | Beschreibung |
|-----------|-------------|
| **[!UICONTROL Serving Type]** | Der Medientyp für diesen Deal: *[!UICONTROL Video],* *[!UICONTROL Display],* oder *[!UICONTROL Audio].* |
| **[!UICONTROL Publisher Site Served On]** | Der Name des Herausgebers, der diesen Bestand verkauft. Suchen Sie nach einem Herausgeber, indem Sie mindestens die ersten beiden Zeichen in den Namen eingeben. Wenden Sie sich an Ihren [!DNL Adobe] Account-Team. |
| **[!UICONTROL Advertiser]** | Ein einzelner Advertiser im Konto, der auf diesen Deal zugreifen kann. Also select the campaign and (optionally) the package in which the deal is available. |
| **[!UICONTROL Media Quality Assessment?]** | (Manche Benutzer) Aktiviert die Anzeige, auf einer anderen DSP zur Überprüfung durch Drittanbieter ausgeführt zu werden. <!-- Who can select this? It's disabled for me. Need to see if there are additional fields when this is enabled. --> |
| **[!UICONTROL Ad Source]** | Die einzige Option ist *[!UICONTROL Site Serve (Event Pixels)]*. |
| **[!UICONTROL Ad Creation]** | (Nur neue Angebote) Ob:<ul><li>*[!UICONTROL Create New]:* So erstellen Sie eine Anzeige für dieses Geschäft.</li><li>*[!UICONTROL Select Ads]:* Verwenden einer vorhandenen Anzeige für dieses Geschäft.</li></ul> |
| **[!UICONTROL Ad Type]** | Der Anzeigentyp für diesen Deal. If you&#39;re going to create new ads for the deal, include the ad size or duration, as requested. The available options vary by media type. |

{style=&quot;table-layout:auto&quot;}

### [!UICONTROL Select Ad(s)]

(Wenn Sie vorhandene Anzeigen verwenden) Die Anzeigen, die in den Deal einbezogen werden sollen. Aktivieren Sie das Kontrollkästchen neben jeder Anzeige, die einbezogen werden soll.

### [!UICONTROL Select & Upload [Media Type]]

(Nur neue Anzeigen) Screens zum Erstellen einer neuen [Drittanbieteranzeige](/help/dsp/campaign-management/ads/ad-create-multiple.md).

### [!UICONTROL Feed Details]

| Parameter | Beschreibung |
|-----------|-------------|
| **[!UICONTROL Media CPM]** | Die Kosten pro Tausend Impressionen (CPM), wie in der Preiskarte für Ihren Vertrag widergespiegelt. Wenden Sie sich an [!DNL Adobe] Account-Team für diesen Wert. <br><br>Geben Sie auch die Währung für das Geschäft an. Alle Benutzer können USD auswählen oder, wenn die SSP zusätzliche Währungen unterstützt, die Währung für das DSP. |
| **[!UICONTROL Third Party Billed Fees]** | (Optional) A static third-party fee to be tracked as a non-billable cost,  and the currency for the deal.<br><br>Alle Benutzer können USD auswählen oder, wenn die SSP zusätzliche Währungen unterstützt, die Währung für das DSP. **HINWEIS:** Abrechenbare Gebühren werden im [!UICONTROL Net CPM] Metrik. |
| **[!UICONTROL Third Party Fee Description]** | (Optional) Eine Beschreibung der Drittanbietergebühren. |
| **[!UICONTROL Flight Dates]** | Die Start- und Enddaten für Traffic, der diesen Deal verwendet. Die Flugdaten müssen innerhalb der Flugdaten der Kampagne angegeben werden. Die Anzeigen-Tags geben nur während des angegebenen Fluges eine Antwort zurück.<br><br> Es empfiehlt sich, eine separate einfache Werbekampagne mit einer Jahresdauer zu erstellen und darin Trackingpixel zu erstellen. |
| **[!UICONTROL Impressions]** | (Optional) Die geschätzte Anzahl von Impressionen, die Sie mit diesem Deal erwarten. This value is used for tracking purposes only and to flag when delivery goals are met; the publisher controls actual ad delivery. The best practice is to enter a high number of impressions to keep the tag active within DSP so it can be renewed or extended if needed. |
| **[!UICONTROL Deal Name]** | Der Name des Deals. Geben Sie einen Namen ein oder wählen Sie *[!UICONTROL Auto Generate Deal Name]* , damit DSP einen Namen basierend auf den Geschäftsdetails generieren kann.<br><br>Beispiel eines automatisch generierten Namens: `Campaign-desktop_video_preroll_15-24Kitchen-$10_USD-jdoe-SAS` |
| **[!UICONTROL Attached Ads]** | (Schreibgeschützt) Die Anzeigen, die Teil des Deals sind. Um eine Anzeige zu bearbeiten, klicken Sie auf den Anzeigennamen. Um eine Anzeige aus dem Angebot zu entfernen, klicken Sie auf **[!UICONTROL X]** neben dem Anzeigennamen. |

{style=&quot;table-layout:auto&quot;}

<!-- 
## Existing Simple Ad Serving Deals

Changes aren't applied retroactively.
-->

<!-- completely different settings layout, so need a separate section for them -->

<!-- From Abhinav: Editable fields are Name, Start & End date, Impressions & CPM. Changes are not applied retroactively.

But I see:

| Parameter | Description |
|-----------|-------------|

| **[!UICONTROL Are you using Deal ID?] | (Read-only) Whether the deal was set up as a [!UICONTROL Deal ID] (*[!DNL Yes]*)  or a [!UICONTROL Simple Ad Serving] deal (*[!DNL No]*). |
| **[!UICONTROL Inventory Type] | (Read-only) The inventory type for the deal. |
| **[!UICONTROL Feed Name] | The name of the [!UICONTROL Simple Ad Serving] deal. |
| **[!UICONTROL Publisher Ad Server] | (Read-only)  |
| **[!UICONTROL Publisher maximum ad length] | The maximum length of the ad, per the publisher. |
| **[!UICONTROL Publisher minimum ad length] | The minimum length of the ad, per the publisher. |
| **[!UICONTROL Fill Type] | (Read-only)  |
| **[!UICONTROL Contracted CPM] | This field is required if billing through TubeMogul, but enter your CPM in this field to track your actual spend. |
| **[!UICONTROL 3rd party technology CPM] | (Optional)  |
| **[!UICONTROL Planned Flight Dates] | The beginning and end dates for the deal flight. These dates don't control ad delivery but are used to track delivery pacing. **THIS IS CONTRARY TO WHAT THE NEW DEAL SETTINGS ABOVE, FROM ABHINAV, SAY**> |
| **[!UICONTROL Target Impressions] | (Optional) The estimated number of impressions you expect to run using this deal. This value is used for tracking purposes only and to flag when delivery goals are met; the publisher controls actual ad delivery. The best practice is to enter a high number of impressions to keep the tag active within DSP so it can be renewed or extended if needed. |
 -->

>[!MORELIKETHIS]
>
>* [Info [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [Create a [!UICONTROL Simple Ad Serving] Deal](simple-deal-create.md)
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)

