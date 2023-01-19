---
title: Eine wiederverwendbare Zielgruppe bearbeiten
description: Erfahren Sie, wie Sie eine wiederverwendbare Zielgruppe bearbeiten.
feature: DSP Audiences
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 0%

---

# Eine wiederverwendbare Zielgruppe bearbeiten

Wenn Sie eine Zielgruppe bearbeiten, die in Platzierungen oder anderen wiederverwendbaren Zielgruppen verwendet wird, werden die Änderungen sofort auf diese Platzierungen und Zielgruppen angewendet.<!-- verify -->

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]>[!UICONTROL All audiences]**.

1. Halten Sie den Cursor über die Zielgruppenzeile und klicken Sie auf **[!UICONTROL Edit]**.

1. Bearbeiten Sie die Zielgruppeneinstellungen auf eine der folgenden Arten:

   >[!NOTE]
   >
   >Wenn Sie die Zielgruppensegmentlogik bearbeiten, wird die [Daten zur Zielgruppengröße](audience-about.md) wird im rechten Bereich aktualisiert.

   * (Optional) So bearbeiten Sie die **[!UICONTROL Audience Name]** click ![Bearbeiten](/help/dsp/assets/edit.png) Geben Sie neben dem Zielgruppennamen einen eindeutigen Zielgruppennamen ein und klicken Sie auf **[!UICONTROL Apply]**.

   * (Optional) Um die Segmentlogik manuell zu bearbeiten, verwenden Sie Segmente, die auf der [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments]und [!UICONTROL Saved Audiences] Tabs](audience-settings.md), führen Sie die folgenden Schritte aus.

      * So fügen Sie ein Segment zu einer vorhandenen Segmentgruppe hinzu:
      1. Klicken Sie im rechten Bereich auf die Segmentgruppe.

      1. (Optional) Ändern Sie die Gruppenlogik in *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* oder *[!UICONTROL Exclude All]* nach Bedarf.

         *[!UICONTROL Exclude All]* ist nicht für die erste Segmentgruppe verfügbar. Erstellen Sie für eine Zielgruppe, die nur Ausschlüsse enthält, diese Zielgruppe als *[!UICONTROL Include Any]* und wählen Sie dann in einer Platzierung diese Zielgruppe aus dem Menü Ausgeschlossene Zielgruppen aus.

      1. Suchen Sie das neue Segment im linken Bereich und aktivieren Sie das Kontrollkästchen neben dem Segmentnamen.

         Die Segmentgruppe wird automatisch mit dem neuen Segment aktualisiert.
   * So fügen Sie eine neue Segmentgruppe hinzu:

      1. Klicken **[!UICONTROL + New Group]** im rechten Bereich.

      1. (Optional) Ändern Sie die Logik zwischen der vorherigen Gruppe und der neuen Gruppe in *[!UICONTROL And]* oder *[!UICONTROL Or]* nach Bedarf.

      1. Suchen Sie die Segmente für die neue Gruppe im linken Bereich und aktivieren Sie die Kontrollkästchen neben den Segmentnamen.

      1. (Optional) Ändern Sie die Gruppenlogik in *[!UICONTROL Include Any]*, *[!UICONTROL Include All]* oder *[!UICONTROL Exclude All]* nach Bedarf.
   * So verwenden Sie die Segmentlogik aus einer vorhandenen Zielgruppe:

      1. Kopieren Sie die Segmentlogik aus der vorhandenen Zielgruppe auf eine der folgenden Arten:

         * Halten Sie in der Ansicht &quot;Alle Zielgruppen&quot;den Cursor über die Zeile &quot;Zielgruppe&quot;und klicken Sie auf **[!UICONTROL More]>[!UICONTROL Copy to Clipboard]**.

         * Klicken Sie in den Einstellungen für die vorhandene Zielgruppe oben im Bedienfeld für die Segmentlogik auf **[!UICONTROL More]>[!UICONTROL Copy to Clipboard]**.

         * Erstellen Sie in einem Texteditor manuell die Segmentlogik mithilfe von alphanumerischen Segment-IDs und [Boolesche Syntax](audience-segment-logic-syntax.md)und kopieren Sie sie in die Zwischenablage.
      1. Klicken **[!UICONTROL paste in an audience rule to begin building]**, fügen Sie die vorhandene Segmentlogik in das Eingabefeld ein und klicken Sie dann auf **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >Wenn die Zielgruppe bereits eine Segmentlogik enthält, wird beim Einfügen in die neue Segmentlogik die vorhandene Logik überschrieben.





1. Klicken **[!UICONTROL Save]**.

1. Klicken Sie in der Bestätigungsnachricht auf **[!UICONTROL Continue]**.

>[!MORELIKETHIS]
>
>* [Über Zielgruppen-Management](audience-about.md)
>* [Wiederverwendbare Zielgruppe erstellen](reusable-audience-create.md)
>* [Duplizieren einer wiederverwendbaren Zielgruppe](reusable-audience-duplicate.md)
>* [Details zu einer wiederverwendbaren Zielgruppe anzeigen](reusable-audience-view-details.md)
>* [Wiederverwendbare Zielgruppe freigeben](reusable-audience-share.md)
>* [Wiederverwendbare Zielgruppe exportieren](reusable-audience-export.md)
>* [Kopieren Sie den Segmentschlüssel für eine wiederverwendbare Zielgruppe in die Zwischenablage.](reusable-audience-clipboard.md)
>* [Eine wiederverwendbare Zielgruppe löschen](reusable-audience-delete.md)
>* [Zielgruppeneinstellungen](audience-settings.md)
>* [Syntax für Zielgruppensegmentlogik](audience-segment-logic-syntax.md)
>* [Verfügbare Drittanbieter von Daten](third-party-data-providers.md)

