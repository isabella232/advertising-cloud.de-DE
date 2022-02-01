---
title: '[!UICONTROL Simple Ad Serving] Deal Settings'
description: Erfahren Sie mehr über die verfügbaren Einstellungen für [!UICONTROL Simple Ad Serving] Angebote.
feature: DSP Simple Ad Serving
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '474'
ht-degree: 0%

---

# [!UICONTROL Simple Ad Serving] Deal Settings

## Neu [!UICONTROL Simple Ad Serving] Angebote

### [!UICONTROL Select Ad Source]

| Parameter | Beschreibung |
|-----------|-------------|
| **[!UICONTROL Serving Type]** | Der Medientyp für diesen Deal: *[!UICONTROL Video],* *[!UICONTROL Display],* oder *[!UICONTROL Audio].* |
| **[!UICONTROL Publisher Site Served On]** | Der Name des Herausgebers, der diesen Bestand verkauft. Suchen Sie nach einem Herausgeber, indem Sie mindestens die ersten beiden Zeichen in den Namen eingeben. Wenden Sie sich an Ihren [!DNL Adobe] Account-Team. |
| **[!UICONTROL Advertiser]** | Ein einzelner Advertiser im Konto, der auf diesen Deal zugreifen kann. Wählen Sie außerdem die Kampagne und (optional) das Paket aus, in dem der Deal verfügbar ist. |
| **[!UICONTROL Media Quality Assessment?]** | (Manche Benutzer) Aktiviert die Anzeige, auf einer anderen DSP zur Überprüfung durch Drittanbieter ausgeführt zu werden. <!-- Who can select this? It's disabled for me. Need to see if there are additional fields when this is enabled. --> |
| **[!UICONTROL Ad Source]** | Die einzige Option ist *[!UICONTROL Site Serve (Event Pixels)]*. |
| **[!UICONTROL Ad Creation]** | (Nur neue Angebote) Ob:<ul><li>*[!UICONTROL Create New]:* So erstellen Sie eine Anzeige für dieses Geschäft.</li><li>*[!UICONTROL Select Ads]:* Verwenden einer vorhandenen Anzeige für dieses Geschäft.</li></ul> |
| **[!UICONTROL Ad Type]** | Der Anzeigentyp für diesen Deal. Wenn Sie neue Anzeigen für den Deal erstellen möchten, schließen Sie die Anzeigengröße oder -dauer wie gewünscht ein. Die verfügbaren Optionen variieren je nach Medientyp. |

{style=&quot;table-layout:auto&quot;}

### [!UICONTROL Select Ad(s)]

(Wenn Sie vorhandene Anzeigen verwenden) Die Anzeigen, die in den Deal einbezogen werden sollen. Aktivieren Sie das Kontrollkästchen neben jeder Anzeige, die einbezogen werden soll.

### [!UICONTROL Select & Upload [Media Type]]

(Nur neue Anzeigen) Screens zum Erstellen einer neuen [Erstanbieter-Anzeige](/help/dsp/campaign-management/ads/ad-create.md) oder [Drittanbieteranzeige](/help/dsp/campaign-management/ads/ad-create-third-party.md).

### [!UICONTROL Feed Details]

| Parameter | Beschreibung |
|-----------|-------------|
| **[!UICONTROL Media CPM]** | Die Kosten pro Tausend Impressionen (CPM), wie in der Preiskarte für Ihren Vertrag widergespiegelt. Wenden Sie sich an [!DNL Adobe] Account-Team für diesen Wert. <br><br>Geben Sie auch die Währung für das Geschäft an. Alle Benutzer können USD auswählen oder, wenn die SSP zusätzliche Währungen unterstützt, die Währung für das DSP. |
| **[!UICONTROL Third Party Billed Fees]** | (Optional) Eine statische Drittanbietergebühr, die als nicht abrechnungsfähige Kosten verfolgt werden soll, sowie die Währung für die Transaktion.<br><br>Alle Benutzer können USD auswählen oder, wenn die SSP zusätzliche Währungen unterstützt, die Währung für das DSP. **HINWEIS:** Abrechenbare Gebühren werden im [!UICONTROL Net CPM] Metrik. |
| **[!UICONTROL Third Party Fee Description]** | (Optional) Eine Beschreibung der Drittanbietergebühren. |
| **[!UICONTROL Flight Dates]** | Die Start- und Enddaten für Traffic, der diesen Deal verwendet. Die Flugdaten müssen innerhalb der Flugdaten der Kampagne angegeben werden. Die Anzeigen-Tags geben nur während des angegebenen Fluges eine Antwort zurück.<br><br> Es empfiehlt sich, eine separate einfache Werbekampagne mit einer Jahresdauer zu erstellen und darin Trackingpixel zu erstellen. |
| **[!UICONTROL Impressions]** | (Optional) Die geschätzte Anzahl von Impressionen, die Sie mit diesem Deal erwarten. Dieser Wert dient nur zu Tracking-Zwecken und zur Kennzeichnung, wann Versandziele erreicht werden. Der Herausgeber steuert die tatsächliche Anzeigenbereitstellung. Es empfiehlt sich, eine große Anzahl von Impressionen einzugeben, damit das Tag in DSP aktiv bleibt, damit es bei Bedarf verlängert oder erweitert werden kann. |
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
>* [Erstellen Sie eine [!UICONTROL Simple Ad Serving] Deal](simple-deal-create.md)
>* [Anzeigen von Ereignisverfolgungspixel für eine [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)

