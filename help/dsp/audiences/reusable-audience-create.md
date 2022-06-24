---
title: Wiederverwendbare Zielgruppe erstellen
description: Erfahren Sie, wie Sie wiederverwendbare Zielgruppen erstellen, die aus Zielgruppensegmenten und anderen gespeicherten Zielgruppen bestehen.
feature: DSP Audiences
exl-id: 48e3dc4c-6e2d-452c-8d69-7e6211d808e0
source-git-commit: 37e5a4fbb7e2ccda77ab0afd49054ec4d1dabf76
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# Wiederverwendbare Zielgruppe erstellen

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

Sie können wiederverwendbare Zielgruppen speichern und verwalten, bei denen es sich um Gruppen von Zielgruppensegmenten und sogar andere gespeicherte Zielgruppen handelt, die Sie als Ziele oder Ausschlüsse für mehrere Platzierungen verwenden können.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Audiences]>[!UICONTROL All Audiences]**.

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create]**.

1. Eindeutige Eingabe [!UICONTROL Audience Name].

1. (Optional) Deaktivieren Sie die Option zum **[!UICONTROL Share with all advertisers in my account]**.

   Wenn Sie eine Zielgruppe freigeben, wird die Zielgruppe als Ziel oder Ausschluss für alle Advertiser innerhalb des Kontos verfügbar. Die einzelnen Segmente in der Zielgruppe stehen jedoch nur Benutzern zur Verfügung, für die die Segmente freigegeben sind. Wenn Sie beispielsweise eine Zielgruppe mit Adobe Analytics-Segmenten für einen Advertiser freigeben, der nicht demselben [!DNL Analytics] -Konto verwenden, wird die Vorschau des Segments in dieser Zielgruppe für diesen Advertiser nicht angezeigt. Nur die für diesen Advertiser verfügbaren Segmente werden in der Zielgruppe in der Vorschau angezeigt.

1. Klicken **[!UICONTROL Save]**.

1. Erstellen Sie die Zielgruppe:

   >[!NOTE]
   >
   >Während der Erstellung der Audience wird im Detail [Daten zur Zielgruppengröße](audience-about.md) im rechten Bereich aktualisiert wird

   * So erstellen Sie die Segmentlogik manuell mithilfe von Segmenten, die im [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments]und [!UICONTROL Saved Audiences] Tabs](audience-settings.md), führen Sie die folgenden Schritte aus.

      * Um das erste Segment hinzuzufügen, suchen Sie das Segment im linken Bereich und aktivieren Sie das Kontrollkästchen neben dem Segmentnamen.

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




1. Klicken **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Über Zielgruppen-Management](audience-about.md)
>* [Zielgruppeneinstellungen](audience-settings.md)
>* [Syntax für Zielgruppensegmentlogik](audience-segment-logic-syntax.md)
>* [Verfügbare Drittanbieter von Daten](third-party-data-providers.md)
>* [Erstellen und Implementieren eines benutzerdefinierten Segments](custom-segment-create.md)
>* [Erstellen und Implementieren eines [!UICONTROL CCPA Opt-Out-of-Sale] Segment](ccpa-opt-out-segment-create.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)

