---
title: Einrichten eines programmgesteuerten "garantierten Angebots"
description: Erfahren Sie, wie Sie einen programmgesteuerten garantierten (PG) Deal einrichten, den Sie mit einem Herausgeber ausgehandelt haben.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 9e371606-5428-4635-9653-7dc43449e489
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# Einrichten eines programmgesteuerten &quot;garantierten Angebots&quot;

*[Nur unterstützte angebotsseitige Plattformen](programmatic-guaranteed-about.md)*

Nachdem Sie mit einem unterstützten Publisher einen programmgesteuerten garantierten (PG) Vertrag ausgehandelt haben, können Sie den Deal in DSP entweder mithilfe von [!DNL Deal ID inbox] oder durch manuelles Eingeben der Details des Deals einrichten.

>[!NOTE]
>
> Bei PG-Angeboten verarbeitet der Herausgeber alle Budgetkürzungen, Budgetbegrenzungen und Targeting. Alle SSPs, die PG durch zulassen, DSP bestätigen, dass der Herausgeber eine Budgetbegrenzung einrichten kann.
>
> Das Einrichten programmgesteuerter garantierter Angebote für Herausgeber auf [!DNL FreeWheel] erfordert zusätzliche Berechtigungen und Schritte. Weitere Informationen finden Sie unter &quot;[Übersicht über das Einrichten programmgesteuerter garantierter Angebote in [!DNL FreeWheel]](freewheel-overview.md)&quot;.

## Einrichten eines programmgesteuerten Garantierten Angebots mit dem [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

Dies ist die bevorzugte Methode für [!DNL FreeWheel], [!DNL Google Authorized Buyers] und [!DNL Rubicon].

1. [Akzeptieren Sie den Deal](deal-id-inbox-accept.md).

1. Nachdem Sie den Deal gespeichert haben, wählen Sie die Anzeigen aus, die für den Deal verwendet werden sollen, und erstellen Sie eine programmgesteuerte, garantierte (PG) Standardplatzierung, wie Sie dazu aufgefordert werden.

   Die Erstellung einer standardmäßigen PG-Platzierung für den Deal ist obligatorisch, um 100 % Ihres Kaufs bereitzustellen. Dieser Platzierungstyp hat kein Targeting, sodass DSP jedem Angebotsantrag des Herausgebers ein Angebot zurückgeben kann.

   * Wenn Sie eine einzelne Transaktion akzeptieren, werden Sie automatisch zum Arbeitsablauf für die Erstellung der Platzierung mit PG-Standard weitergeleitet.

      Alle [!DNL FreeWheel]-Angebote werden als ein einziges Angebot vorgeschlagen.

   * Wenn Sie einen Vorschlag mit mehreren PG-Deal-IDs akzeptieren, identifizieren Sie jede PG-Standardplatzierung, die Sie erstellen müssen. Nachdem Sie alle erforderlichen Platzierungen erstellt haben, ist die Schaltfläche Weiter aktiviert.

1. (Optional) Richten Sie das Targeting des PG-Geschäfts in zusätzlichen, nicht PG-Platzierungen ein.

## Manuelles Einrichten eines programmatischen Garantiedeals

Verwenden Sie diese Methode für alle anderen SSPs.

1. [Richten Sie die Details zur Deal-ID manuell ein](deal-id-create.md).

1. Nachdem Sie den Deal gespeichert haben, wählen Sie die Anzeigen aus, die für den Deal verwendet werden sollen, und erstellen Sie nach Aufforderung eine PG-Standardplatzierung.

   Die Erstellung einer PG-Standardplatzierung für den Kauf ist obligatorisch, um 100 % Ihres Kaufs bereitzustellen. Dieser Platzierungstyp hat kein Targeting, sodass DSP jedem Angebotsantrag des Herausgebers ein Angebot zurückgeben kann.

1. (Optional) Richten Sie das Targeting des PG-Geschäfts in zusätzlichen, nicht PG-Platzierungen ein.

>[!MORELIKETHIS]
>
>* [Über programmatische Garantievereinbarungen](programmatic-guaranteed-about.md)
>* [Tipps für die Aushandlung eines programmgesteuerten &quot;garantierten Angebots&quot;](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [Senden einer Anzeige für einen programmgesteuerten, garantierten Deal mit [!DNL FreeWheel]](freewheel-submit.md)
>* [Akzeptieren eines Angebots im Deal-ID-Posteingang](deal-id-inbox-accept.md)
>* [Manuelles Erstellen von Details zur Angebots-ID](deal-id-create.md)
>* [SSP-Partner](ssp-partners.md)
>* [Übersicht über die Funktionen des Bestands](inventory-overview.md)

