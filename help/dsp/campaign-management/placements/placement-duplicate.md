---
title: Duplizieren von Platzierungen
description: Erfahren Sie, wie Sie eine oder mehrere Platzierungen duplizieren.
feature: DSP Placements
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Duplizieren von Platzierungen

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

Duplizieren Sie eine oder mehrere Platzierungen, um Platzierungen mit ähnlichen Einstellungen zu erstellen. Sie können:

* Mehrere Duplikate von Platzierungen erstellen
* Duplizieren Sie Platzierungen innerhalb der ursprünglichen Advertiser und Kampagnen oder in verschiedenen Kampagnen.
* (Für duplizierte Platzierungen in den ursprünglichen Kampagnen) Optional Duplizieren Sie die ursprünglichen Anzeigen.
* Status und Flugdaten der neuen Platzierungen ändern

Siehe[Nicht duplizierte Elemente](#placement-not-duplicated)&quot; für eine Liste der Platzierungseinstellungen, die nicht dupliziert werden.

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Campaigns]**.

1. Klicken Sie auf den Namen der Kampagne.

1. Klicken Sie im Untermenü auf **[!UICONTROL Placements]**.

1. Führen Sie einen der folgenden Schritte aus:

   * Um eine Platzierung zu duplizieren, klicken Sie auf  **[!UICONTROL ...]>[!UICONTROL Duplicate]** neben dem Paketnamen.

   * So duplizieren Sie mehrere Platzierungen:

      1. Aktivieren Sie das Kontrollkästchen neben jeder Platzierung, die dupliziert werden soll.

      1. Klicken Sie in der Symbolleiste für Massenaktionen auf **[!UICONTROL Duplicate]**.

1. Geben Sie die neuen Platzierungseinstellungen an:

   1. (Einzelplatzierungen) Geben Sie den neuen Platzierungsnamen ein.

   1. Im **[!UICONTROL Choose Package (Required)]** wählen Sie entweder das übergeordnete Paket oder **[!UICONTROL No package]*.

   1. (Optional) Ändern Sie die Standardeinstellungen.

   Die Einstellungen gelten für alle ausgewählten Platzierungen.

   Standardmäßig beziehen sich die neuen Platzierungen auf den ursprünglichen Anzeigentyp, werden den ursprünglichen Advertisern und Kampagnen zugewiesen, haben Flugpläne, die am aktuellen Tag beginnen, werden angehalten und enthalten nicht die ursprünglichen Anzeigen.

   Wenn Sie mehrere Platzierungen erstellen, werden die neuen Platzierungsnamen entsprechend der Konvention &lt;*original_placement_name #N*>, z. B. &quot;Meine Platzierung Nr. 2&quot;.

1. Klicken **[!UICONTROL Submit]**.

## Nicht duplizierte Elemente {#placement-not-duplicated}

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
>* [Über die Platzierungsverwaltung](placement-about.md)
>* [Erstellen einer Platzierung](placement-create.md)
>* [Eine Platzierung bearbeiten](placement-edit.md)
>* [Anzeigen des Änderungsprotokolls für eine Platzierung](placement-change-log.md)
>* [Platzierungseinstellungen](placement-settings.md)

