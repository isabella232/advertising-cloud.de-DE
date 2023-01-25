---
title: Manuelles Erstellen von Details zur Angebots-ID
description: Erfahren Sie, wie Sie Details für eine Angebots-ID manuell eingeben.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 20a57919-c68f-4c9d-a8e1-f49484f74655
source-git-commit: 3f80cdd81b1ba28519d3075922f57a1155e55dbd
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# Manuelles Erstellen von Details zur Angebots-ID

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Inventory]> [!UICONTROL Deals].**

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create]** und wählen Sie **[!UICONTROL Deal ID]**.

1. Geben Sie die [Deal-Einstellungen](deal-id-settings.md):

   1. Im [!UICONTROL Deal ID basics] Geben Sie die Details des Angebots sowie die Advertiser an, die auf den Deal zugreifen können. Für garantierte Angebote müssen Sie auch die geplanten Flugdaten und die geschätzte Anzahl der Impressionen angeben, und zwar ausschließlich zu Tracking-Zwecken. Verfolgen Sie garantierte Deal-Geschwindigkeit mit der Metrik &quot;PG-Impression-Geschwindigkeit&quot;auf der Seite &quot;Angebote&quot;.

   1. (Nur Administrator-Benutzer; optional) Im [!UICONTROL Technical] ändern Sie die Standardeinstellungen nach Bedarf.

   1. Klicken **[!UICONTROL Save]**.

1. (Nur garantierte Angebote) Wählen Sie die Anzeigen aus, die für das Angebot verwendet werden sollen, und erstellen Sie eine standardmäßige, programmgarantierte Platzierung (PG).

   Standardmäßige PG-Platzierungen stellen sicher, dass Ihr Deal immer ein Angebot für jede Angebotsanforderung zurückgibt. Wenn Sie keine standardmäßige PG-Platzierung erstellen, platzieren Platzierungen, die auf den Deal abzielen, keine Angebote, es sei denn, sie sind korrekt eingerichtet. Sie sollten immer eine standardmäßige PG-Platzierung erstellen. Im [!UICONTROL Placements] Ansicht, standardmäßige PG-Platzierungen haben eine [!UICONTROL Sub-type] Spaltenwert von &quot;[!UICONTROL PG Default].&quot;

   Sie können den Deal optional als Lagerbestandsziel in zusätzlichen Platzierungen verwenden, müssen sie jedoch korrekt einrichten, um Angebote zu platzieren.

   1. Im [!UICONTROL Ad & Campaign Selection] -Einstellungen wählen Sie die Anzeigen aus, die für den Deal verwendet werden sollen:

      1. Wählen Sie den Advertiser, die Kampagne und den Anzeigentyp aus. Wählen Sie optional einen Anzeigenstatus aus, nach dem die Anzeigen gefiltert werden sollen.

      1. Aktivieren Sie in der Liste der verfügbaren Anzeigen das Kontrollkästchen neben den einzelnen Anzeigen, die für das Geschäft verwendet werden sollen.

      1. Klicken **[!UICONTROL Apply]**.
   1. Im Bildschirm für die Platzierungseinstellungen:

      1. Geben Sie den Platzierungsnamen ein.

      1. (Optional) Bearbeiten Sie die [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md), einschließlich des Überschreibens des Standardangebots, das automatisch mit dem CPM-Wert aus dem Deal gefüllt wird; Änderung des Datumsbereichs; oder fügen Sie weitere Anzeigen hinzu.

      Der Deal wird automatisch im Abschnitt Inventarziele ausgerichtet. Alle anderen Targeting-Optionen sind nicht verfügbar.

      1. Klicken **[!UICONTROL Create placement]**.



Nachdem Sie den Deal erstellt haben, können Sie den Deal als Inventarziel für mehrere Platzierungen verwenden.

>[!NOTE]
>
> Sie müssen das Deal-Tag nicht zur Verifizierung an den Herausgeber senden.

>[!TIP]
>
>* Im [!UICONTROL Inventory] > [!UICONTROL Deals] Ansicht, die [!UICONTROL Pacing & Budget] zeigt an, wie der Deal zum festgelegten Flugdatum und Impressionsziel gelangt.
>
>* Wenn der Versand zu kurz oder zu schnell verläuft, wenden Sie sich an Ihren Herausgeber, um die Menge anzupassen, die durch den Deal gesendet wird.


>[!MORELIKETHIS]
>
>* [Manuelle Deal-ID-Einstellungen](deal-id-settings.md)
>* [Einrichten eines programmgesteuerten &quot;garantierten Angebots&quot;](programmatic-guaranteed-set-up.md)
>* [Senden einer Anzeige für einen programmgesteuerten, garantierten Deal mit [!DNL FreeWheel]](freewheel-submit.md)
>* [Über programmatische Garantievereinbarungen](programmatic-guaranteed-about.md)

<!-- >* [Specify Placements and Ads for a Private Deal](deal-id-attach-placements.md)-->
