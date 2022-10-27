---
title: Package duplizieren
description: Erfahren Sie, wie Sie ein Paket duplizieren.
feature: DSP Packages
exl-id: 4c37883f-5feb-4513-9573-ed4e32606132
source-git-commit: 5ed402a7c83072a7af6a06757050486c6d7d7080
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---

# Package duplizieren

Duplizieren Sie ein Paket, um ein Paket mit ähnlichen Einstellungen zu erstellen. Sie können:

* Duplizieren Sie das Paket innerhalb des ursprünglichen Advertisers und der Kampagne oder in verschiedenen Kampagnen.
* Duplizieren Sie optional die Platzierungen im Paket
* (Für duplizierte Pakete innerhalb der ursprünglichen Kampagnen) Duplizieren Sie optional die ursprünglichen Anzeigen und die Ereignispixel auf Platzierungsebene.
* Ändern der Flugdaten des neuen Packages

Siehe[Nicht duplizierte Elemente](#package-not-duplicated)&quot; für eine Liste der Platzierungseinstellungen, die nicht dupliziert werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.
1. Klicken Sie auf den Namen der Kampagne, um die [!UICONTROL Packages] anzeigen.
1. Klicken Sie neben dem Paketnamen auf  **[!UICONTROL ...]>[!UICONTROL Duplicate]**.
1. Geben Sie die neuen Paketeinstellungen an:
   1. Geben Sie den neuen Paketnamen ein.
   1. (Optional) Ändern Sie die Standardeinstellungen.

      Standardmäßig:

      * Das neue Paket wird dem ursprünglichen Advertiser und der Kampagne zugewiesen.
      * Das neue Paket wird am aktuellen Tag aktiv.<!-- and the flight continues for NN  days. -->
      * Platzierungen innerhalb des ursprünglichen Pakets werden in das neue Paket kopiert.
      * Die Anzeigen und die Ereignispixel auf Platzierungsebene werden nicht in das neue Paket kopiert.
1. Klicken **[!UICONTROL Submit]**.

## Nicht duplizierte Elemente {#package-not-duplicated}

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
>* [Über Package Management](package-about.md)
>* [Erstellen eines Pakets](package-create.md)
>* [Bearbeiten eines Pakets](package-edit.md)
>* [Anzeigen des Änderungsprotokolls für ein Paket](package-change-log.md)
>* [Paketeinstellungen](package-settings.md)

