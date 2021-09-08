---
title: Senden einer Anzeige für ein PG-Geschäft an [!DNL FreeWheel]
description: Erfahren Sie, wie Sie bei einem Herausgeber auf FreeWheel eine Genehmigung für eine Anzeige für ein programmgesteuertes garantiertes Angebot anfordern können.
feature: Private Inventory, Deal IDs
exl-id: null
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# Senden einer Anzeige für einen programmgesteuerten garantierten Deal an FreeWheel

*Nur Konten mit der Berechtigung  [!DNL FreeWheel] &quot;Programmatisch garantiert&quot;*

Sobald Sie [ein programmgesteuertes garantiertes Angebot für einen Herausgeber auf FreeWheel](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox) angenommen haben, einschließlich der Auswahl einer Anzeige und der Erstellung der programmgarantierten Standardplatzierung, die für den Deal verwendet werden soll, müssen Sie die Anzeige zur Genehmigung an FreeWheel senden.

>[!PREREQUISITES]
>
>Arbeiten Sie mit Ihrem Adobe-Kontoteam zusammen, um sicherzustellen, dass Ihr [!DNL DSP]-Konto über die Berechtigung verfügt, den programmgarantierten Workflow [!DNL FreeWheel] zu verwenden.

1. Kopieren Sie den Anzeigenschlüssel für die Anzeige, die mit dem FreeWheel-Deal verwendet wird:

   1. Klicken Sie auf den Namen der Kampagne.

   1. Klicken Sie im Untermenü auf **[!UICONTROL Ads]**.

   1. Klicken Sie neben dem Anzeigennamen auf **[!UICONTROL ...]>[!UICONTROL Edit]** .

   1. Kopieren Sie nach dem Öffnen der Anzeigeneinstellungen den alphanumerischen Anzeigenschlüssel in die URL, die in der Adressleiste des Browsers angezeigt wird.

      In der folgenden URL ist der Anzeigenschlüssel beispielsweise `3NtNC5ZbaGZtqbei8jD3`

      `https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads`

1. Senden Sie die Anzeige an FreeWheel:

   1. Suchen Sie in der Ansicht [!UICONTROL Deals] den Deal.

   1. Klicken Sie in der Zeile &quot;Deal&quot;auf ![Menü &quot;Optionen](/help/dsp/assets/options-menu.png) **[!UICONTROL submit to [!DNL FreeWheel]]**.

   1. Überprüfen Sie die Deal-ID, geben Sie die **[!UICONTROL Ad Key]** ein, die Sie in Schritt 1 kopiert haben, und klicken Sie dann auf **[!UICONTROL Submit]**.

   Die Anzeige muss vor der Ausführung gesendet und genehmigt werden.

1. [Überprüfen Sie den Status](freewheel-check-status.md) der Anzeigenübermittlung.

>[!MORELIKETHIS]
>
>* [Übersicht über die Einrichtung programmgesteuerter Garantiegeschäfte in FreeWheel](freewheel-overview.md)
>* [Akzeptieren eines Angebots im Deal-ID-Posteingang](deal-id-inbox-accept.md)
>* [Überprüfen des Status von Anzeigen  [!DNL FreeWheel] für programmgesteuerte garantierte Angebote](freewheel-check-status.md)
>* [Fehlercodes für FreeWheel-Anzeigenübermittlungen](freewheel-error-codes.md)

