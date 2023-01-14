---
title: Eine Kampagne duplizieren
description: Erfahren Sie, wie Sie eine Kampagne duplizieren.
feature: DSP Campaigns
exl-id: 2bb4030d-22b0-4a16-aeed-35f64a19df6a
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---

# Eine Kampagne duplizieren

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplizieren Sie eine Kampagne, um eine neue Kampagne mit ähnlichen Einstellungen zu erstellen. Sie können:

* Duplizieren Sie die Kampagne für den ursprünglichen Advertiser oder für einen anderen
* Optional Duplizieren Sie die Originalpakete und -platzierungen
* Ändern der Flugdaten der neuen Kampagne

Siehe[Nicht duplizierte Elemente](#campaign-not-duplicated)&quot; für eine Liste der Platzierungseinstellungen, die nicht dupliziert werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie neben dem Kampagnennamen auf **... >[!UICONTROL Duplicate]**.

1. Geben Sie die neuen Kampagneneinstellungen an:

   1. Geben Sie den neuen Kampagnennamen und das Endflugdatum ein.

   1. (Optional) Ändern Sie die Standardeinstellungen.

      Standardmäßig wird die neue Kampagne dem ursprünglichen Advertiser zugewiesen, hat einen Flugplan, der am aktuellen Tag beginnt, und enthält die ursprünglichen Pakete und Platzierungen.

1. Klicken **[!UICONTROL Submit]**.

## Nicht duplizierte Elemente {#campaign-not-duplicated}

Alle Einstellungen der ursprünglichen Platzierungen werden dupliziert, mit Ausnahme:

* Experimenteinstellungen
* (Wenn Sie die Flugdaten ändern) Benutzerdefinierte Anzeigenplanung
* (Wenn Sie keine Anzeigen anhängen) Benutzerdefinierte Anzeigengewichtung und -planung
* Standardplatzierungen für programmatisch garantierte (PG) Angebote und Platzierungen für [!UICONTROL Simple Ad Serving] Angebote
* (Wenn Sie Platzierungen in eine andere Kampagne kopieren):
   * Geo-Ziele
   * Ereignispixel
   * Anzeigen
   * Platzierungsebene [!DNL DoubleVerify Authentic Brand Safety] Segmente (die die Segmente auf Advertiser-Ebene überschreiben)

>[!MORELIKETHIS]
>
>* [Über Campaign Management](campaign-about.md)
>* [Erstellen einer Kampagne](campaign-create.md)
>* [Eine Kampagne bearbeiten](campaign-edit.md)
>* [Kampagneneinstellungen](campaign-settings.md)

