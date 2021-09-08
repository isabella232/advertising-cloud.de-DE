---
title: Erstellen einer Platzierung
description: Erfahren Sie, wie Sie eine Platzierung erstellen.
feature: Placements
exl-id: 4e37b571-9af4-4897-bff2-035a5f2600a5
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 1%

---

# Erstellen einer Platzierung

>[!TIP]
>
>Erstellen Sie Platzierungen basierend auf bestimmten Kampagnenzielen oder Berichtsanforderungen.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne, in der die Platzierung enthalten sein soll.

1. Klicken Sie über der Datentabelle auf **[!UICONTROL Create]**. Klicken Sie im Abschnitt [!UICONTROL Placement Types] des Menüs auf den Platzierungstyp.

   Der Platzierungstyp bestimmt den Anzeigentyp, den die Platzierung enthalten kann.

1. Geben Sie die [Platzierungseinstellungen](placement-settings.md) ein:

   1. Geben Sie die Einstellungen für [!UICONTROL Basics] an.

   1. Geben Sie im Abschnitt [!UICONTROL Goals] die [!UICONTROL Gross Budget] und optional zusätzliche Platzierungsziele an.
Einige Felder verfügen über Standardwerte, die Sie überschreiben können.

      Wenn das Paket, dem die Platzierung zugewiesen wird, über Geschwindigkeit auf Paketebene verfügt, spiegeln Ihre Ziele und Schritteinstellungen die Paketeinstellungen wider.

   1. (Optional) Schränken Sie im Abschnitt [!UICONTROL Geo-Targeting] die Positionen ein, die ein- oder ausgeschlossen sind.

      Wenn Sie bestimmte Orte nicht identifizieren, werden alle Orte als Ziel ausgewählt.

      >[!NOTE]
      >
      >Orte für Stadt und DMA sind nicht für Roku-Platzierungen verfügbar.

   1. Schränken Sie im Abschnitt [!UICONTROL Inventory Targeting] die Inventarquellen ein, die ein- oder ausgeschlossen werden sollen.

      Bei den meisten Platzierungstypen sind standardmäßig alle Inventartypen und alle Quellen für jeden Typ enthalten. Bei Platzierungen vom Typ [!DNL Roku] müssen Sie den Inventartyp und die Quellen angeben.

   1. (Optional) Schränken Sie im Abschnitt [!UICONTROL Site Targeting] die Zielseiten ein und geben Sie alle Sites an, die Sie ausschließen möchten.

   1. (Optional) Im Abschnitt [!UICONTROL Audience Targeting] :

      1. Schränken Sie die Zielgruppe ein. Dazu gehört die Auswahl von Zielgruppensegmenten für das Targeting innerhalb der Platzierung.

         Für [!DNL] Roku-Platzierungen können Sie die eindeutige Übereinstimmung DSP [-Zielgruppe mit  [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) nutzen, indem Sie ein oder mehrere Zielgruppensegmente einschließen, die mit dem [!DNL Roku]-deterministischen Datensatz (opted-in) abgeglichen werden können.
   1. (Für Kampagnen mit geräteübergreifendem Targeting auf Benutzerebene; (optional) Wenn die Platzierung auf eine oder mehrere spezifische Zielgruppen ausgerichtet ist, aktivieren Sie benutzerbasiertes geräteübergreifendes Targeting für die Platzierung.

      Personenbasiertes geräteübergreifendes Targeting wird von [!DNL LiveRamp] bereitgestellt, wobei nur US-Daten verwendet werden. Der Dienst steht allen Advertisern mit einem CPM von 0,35 USD für Impressionen zur Verfügung, die mithilfe des Gerätediagramms [!DNL LiveRamp] bereitgestellt werden (d. h. für Geräte, die nicht in den Zielgruppensegmenten gefunden werden).

   1. (Optional) Wenden Sie im Abschnitt [!DNL Brand Safety and Media Targeting] Einschränkungen hinsichtlich der Markensicherheit für Ihre Platzierungen an.

   1. (Optional) Geben Sie im Abschnitt [!DNL Tracking] die Drittanbieter-Ereignispixel oder Konversionspixel für Anzeigen in die Platzierung ein.

      >[!NOTE]
      >
      >([!DNL Roku] Platzierungen) Zu den von [!DNL Roku] genehmigten Drittanbieter für Pixel gehören [!DNL Acxiom], [!DNL comScore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal] a13/>, [!DNL Placed], [!DNL Polk] und [!DNL Research Now].[!DNL Oracle]


1. Klicken **[!UICONTROL Create Placement]**.

1. (Optional) Fügen Sie der Platzierung Anzeigen hinzu:

   1. Klicken **[!UICONTROL Attach an ad]**.

   1. Führen Sie einen der folgenden Schritte aus:
   * So erstellen Sie eine neue Anzeige:

      1. Klicken **[!UICONTROL Create a New Ad].**

      1. Geben Sie die Anzeigeneinstellungen für [Audioanzeigen](/help/dsp/campaign-management/ads/ad-settings-audio.md), [vernetzte TV](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md), [Display-Anzeigen](/help/dsp/campaign-management/ads/ad-settings-display.md), [mobile Anzeigen](/help/dsp/campaign-management/ads/ad-settings-mobile.md), [native Anzeigen](/help/dsp/campaign-management/ads/ad-settings-native.md) oder [Pre-Roll-Anzeigen](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md) an.

      1. Klicken **[!UICONTROL Save & Submit for Review]**.

      1. (Optional) Klicken Sie für jede zusätzliche Anzeige, die Sie für die Platzierung erstellen möchten, auf **[!UICONTROL Attach Another Ad]** und wiederholen Sie dann die Schritte 1 bis 3.

      1. Wenn Sie keine vorhandenen Anzeigen hinzufügen möchten, klicken Sie auf **[!UICONTROL I'm done for now]**.
   * So fügen Sie vorhandene Anzeigen in der Kampagne hinzu:

      1. Klicken **[!UICONTROL Select an Ad]**.
      1. Führen Sie einen der folgenden Schritte aus:
         * So fügen Sie jeweils eine Anzeige hinzu:
            1. Klicken Sie neben dem Anzeigennamen auf **[!UICONTROL Select].**.
            1. (Optional) Klicken Sie für jede zusätzliche Anzeige, die Sie anhängen möchten, auf **[!UICONTROL Attach Another Ad]** und wiederholen Sie dann den Vorgang.
         * So fügen Sie bis zu 20 Anzeigen gleichzeitig hinzu:
            1. Aktivieren Sie das Kontrollkästchen über der Anzeigenliste.
            1. Aktivieren Sie das Kontrollkästchen neben jeder hinzuzufügenden Anzeige.
            1. Klicken **[!UICONTROL Attach]**.
            1. Klicken Sie neben dem Anzeigennamen auf **[!UICONTROL Select]**.
      1. (Optional) So überschreiben Sie die standardmäßige Flugzeit und Anzeigenrotation für bestimmte Anzeigen in der Platzierung:
         1. Klicken **[!UICONTROL Custom Schedule Ads]**.

         1. Führen Sie einen der folgenden Schritte aus:

            * Um einen Flug hinzuzufügen, klicken Sie auf **[!UICONTROL Add Flight]** und geben Sie dann das Start- und Enddatum an.

            * Um einen vorhandenen Flug zu einer Anzeige hinzuzufügen, klicken Sie in der Anzeigenzeile für die Flugspalte auf **[!UICONTROL +]** .

            * Um einen vorhandenen Flug aus einer Anzeige zu entfernen, klicken Sie in der Anzeigenzeile für die Flugspalte auf **[!UICONTROL x]** .

            * (Wenn mehrere Anzeigen denselben Flug haben) Um die Anzeigen ungleichmäßig zu drehen, klicken Sie in den Fluginformationen auf **[!UICONTROL Even Rotation]** und geben Sie dann die relative Gewichtung ein, um die jede Anzeige gedreht werden soll (in Prozent).

               Die Gesamtgewichte müssen 100 betragen.
         1. Klicken Sie oben rechts auf **[!UICONTROL Continue]**.

         1. Überprüfen Sie die Flugdetails und klicken Sie dann auf **[!UICONTROL Save & Finish]**.




>[!MORELIKETHIS]
>
>* [Über die Platzierungsverwaltung](placement-about.md)
>* [Eine Platzierung bearbeiten](placement-edit.md)
>* [Bearbeiten des Anzeigenzeitplans für eine Platzierung](placement-edit-ad-schedule.md)
>* [Anhalten oder Aktivieren einer Platzierung](placement-pause-activate.md)
>* [Platzierungseinstellungen](placement-settings.md)
>* [Tastaturbefehle](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)

   >*[Fehlerbehebung Leistung](/help/dsp/optimization/troubleshooting-performance.md)

