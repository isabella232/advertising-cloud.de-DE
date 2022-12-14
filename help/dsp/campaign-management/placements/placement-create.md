---
title: Erstellen einer Platzierung
description: Erfahren Sie, wie Sie eine Platzierung erstellen.
feature: DSP Placements
exl-id: 4e37b571-9af4-4897-bff2-035a5f2600a5
source-git-commit: 86f8df0c438a68dabba8f5b2abeb106d3320d7ef
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 1%

---

# Erstellen einer Platzierung

>[!TIP]
>
>Erstellen Sie Platzierungen basierend auf bestimmten Kampagnenzielen oder Berichtsanforderungen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne, in der die Platzierung enthalten sein soll.

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create]**. Im [!UICONTROL Placement Types] auf den Platzierungstyp klicken.

   Der Platzierungstyp bestimmt den Anzeigentyp, den die Platzierung enthalten kann.

1. Geben Sie die [Platzierungseinstellungen](placement-settings.md):

   1. Geben Sie die [!UICONTROL Basics] -Einstellungen.

   1. Im [!UICONTROL Goals] -Abschnitt, geben Sie die [!UICONTROL Gross Budget] und optional zusätzliche Platzierungsziele angeben.

      Einige Felder verfügen über Standardwerte, die Sie überschreiben können.

      Wenn das Paket, dem die Platzierung zugewiesen wird, über Geschwindigkeit auf Paketebene verfügt, spiegeln Ihre Ziele und Schritteinstellungen die Paketeinstellungen wider.

   1. (Optional) Im [!UICONTROL Geo-Targeting] -Abschnitt die ein- oder ausgeschlossenen Speicherorte einschränken.

      Wenn Sie bestimmte Orte nicht identifizieren, werden alle Orte als Ziel ausgewählt.

      >[!NOTE]
      >
      >Orte für Stadt und DMA sind nicht für Roku-Platzierungen verfügbar.

   1. Im [!UICONTROL Inventory Targeting] -Abschnitt die Inventarquellen einschränken, die ein- oder ausgeschlossen werden sollen.

      Bei den meisten Platzierungstypen sind standardmäßig alle Inventartypen und alle Quellen für jeden Typ enthalten. Für [!DNL Roku] Platzierungen, müssen Sie den Inventartyp und die Quellen angeben.

   1. (Optional) Im [!UICONTROL Site Targeting] einschränken Sie die Sites ein, die Sie als Ziel auswählen möchten, und geben Sie alle Sites an, die Sie ausschließen möchten.

   1. (Optional) Im [!UICONTROL Audience Targeting] Abschnitt:

      1. Schränken Sie die Zielgruppe ein. Dazu gehört die Auswahl von Zielgruppensegmenten für das Targeting innerhalb der Platzierung.

         Für [!DNL] Roku-Platzierungen, können Sie [DSP eindeutige Zielgruppenübereinstimmung mit [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) durch Einschließen eines oder mehrerer Zielgruppensegmente, die mit der [!DNL Roku] (Opt-in) deterministischer Datensatz.
   1. (Für Kampagnen mit geräteübergreifendem Targeting auf Benutzerebene; (optional) Wenn die Platzierung auf eine oder mehrere spezifische Zielgruppen ausgerichtet ist, aktivieren Sie benutzerbasiertes geräteübergreifendes Targeting für die Platzierung.

      Personenbasiertes geräteübergreifendes Targeting wird bereitgestellt von [!DNL LiveRamp] ausschließlich US-Daten verwenden. Der Dienst steht allen Advertisern mit einem CPM-Preis von 0,35 USD für Impressionen zur Verfügung, die mithilfe der [!DNL LiveRamp] Gerätediagramm (d. h. für Geräte, die nicht in den Zielgruppensegmenten gefunden werden).

   1. (Optional) Im [!DNL Brand Safety and Media Targeting] sollten Sie Einschränkungen der Markensicherheit für Ihre Platzierungen anwenden.

   1. (Optional) Im [!DNL Tracking] Geben Sie für Anzeigen in der Platzierung Ereignispixel von Drittanbietern oder Konversionspixel ein.

      >[!NOTE]
      >
      >([!DNL Roku] Platzierungen) Drittanbieter, die von [!DNL Roku] include [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]und [!DNL Research Now].


1. Klicken **[!UICONTROL Create Placement]**.

1. (Optional) Fügen Sie der Platzierung Anzeigen hinzu:

   1. Klicken **[!UICONTROL Attach an ad]**.

   1. Führen Sie einen der folgenden Schritte aus:
   * So erstellen Sie eine neue Anzeige:

      1. Klicken **[!UICONTROL Create a New Ad].**

      1. Geben Sie die Anzeigeneinstellungen für [Audio-Anzeigen](/help/dsp/campaign-management/ads/ad-settings-audio.md), [vernetztes Fernsehen](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md), [Display-Anzeigen](/help/dsp/campaign-management/ads/ad-settings-display.md), [mobile Anzeigen](/help/dsp/campaign-management/ads/ad-settings-mobile.md), [native Anzeigen](/help/dsp/campaign-management/ads/ad-settings-native.md), [Pre-Roll-Anzeigen](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)oder [universelle Videoanzeigen](/help/dsp/campaign-management/ads/ad-settings-universal-video.md).

      1. Klicken **[!UICONTROL Save & Submit for Review]**.

      1. (Optional) Klicken Sie für jede zusätzliche Anzeige, die Sie für die Platzierung erstellen möchten, auf **[!UICONTROL Attach Another Ad]** und wiederholen Sie dann die Schritte 1 bis 3.

      1. Wenn Sie keine vorhandenen Anzeigen hinzufügen, klicken Sie auf **[!UICONTROL I'm done for now]**.
   * So fügen Sie vorhandene Anzeigen in der Kampagne hinzu:

      1. Klicken **[!UICONTROL Select an Ad]**.

      1. Führen Sie einen der folgenden Schritte aus:

         * So fügen Sie jeweils eine Anzeige hinzu:

            1. Klicken Sie neben dem Anzeigennamen auf **[!UICONTROL Select].**

            1. (Optional) Klicken Sie für jede zusätzliche Anzeige, die Sie anhängen möchten, auf **[!UICONTROL Attach Another Ad]** und wiederholen Sie dann den Prozess.
         * So fügen Sie bis zu 20 Anzeigen gleichzeitig hinzu:

            1. Aktivieren Sie das Kontrollkästchen über der Anzeigenliste.

            1. Aktivieren Sie das Kontrollkästchen neben jeder hinzuzufügenden Anzeige.

            1. Klicken **[!UICONTROL Attach]**.

            1. Klicken Sie neben dem Anzeigennamen auf **[!UICONTROL Select]**.
      1. (Optional) So überschreiben Sie die standardmäßige Flugzeit und Anzeigenrotation für bestimmte Anzeigen in der Platzierung:

         1. Klicken **[!UICONTROL Custom Schedule Ads]**.

         1. Führen Sie einen der folgenden Schritte aus:

            * Um einen Flug hinzuzufügen, klicken Sie auf **[!UICONTROL Add Flight]** und geben Sie dann das Start- und Enddatum an.

            * Um einen vorhandenen Flug zu einer Anzeige hinzuzufügen, klicken Sie auf **[!UICONTROL +]** in der Anzeigenzeile für die Flugspalte.

            * Um einen vorhandenen Flug aus einer Anzeige zu entfernen, klicken Sie auf **[!UICONTROL x]** in der Anzeigenzeile für die Flugspalte.

            * (Wenn mehrere Anzeigen denselben Flug haben) Um die Anzeigen ungleichmäßig zu drehen, klicken Sie auf **[!UICONTROL Even Rotation]** in den Fluginformationen und geben Sie dann die relative Gewichtung der einzelnen Anzeigen in Prozent an.

               Die Gesamtgewichte müssen 100 betragen.
         1. Klicken Sie oben rechts auf **[!UICONTROL Continue]**.

         1. Überprüfen Sie die Flugdetails und klicken Sie dann auf **[!UICONTROL Save & Finish]**.






>[!MORELIKETHIS]
>
>* [Über die Platzierungsverwaltung](placement-about.md)
>* [Eine Platzierung bearbeiten](placement-edit.md)
>* [Bearbeiten des Anzeigenzeitplans für eine Platzierung](placement-edit-ad-schedule.md)
>* [Anhalten oder Aktivieren einer Platzierung](placement-pause-activate.md)
>* [Anzeigen des Änderungsprotokolls für eine Platzierung](placement-change-log.md)
>* [Platzierungseinstellungen](placement-settings.md)
>* [Tastaturbefehle](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)

   >*[Fehlerbehebung bei der Leistung](/help/dsp/optimization/troubleshooting-performance.md)
>* [Video: Erstellen einer standardmäßigen Anzeigeplatzierung](https://video.tv.adobe.com/v/340454)

