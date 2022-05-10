---
title: Einrichten eines programmgesteuerten "garantierten Angebots"
description: Erfahren Sie, wie Sie einen programmgesteuerten garantierten (PG) Deal einrichten, den Sie mit einem Herausgeber ausgehandelt haben.
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 9e371606-5428-4635-9653-7dc43449e489
source-git-commit: 3c9822890e96035fc9e44f8832efcc2889a8cb5f
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Einrichten eines programmgesteuerten &quot;garantierten Angebots&quot;

*[Nur unterstützte angebotsseitige Plattformen](programmatic-guaranteed-about.md)*

Nachdem Sie einen programmgesteuerten garantierten (PG) Vertrag mit einem unterstützten Publisher ausgehandelt haben, können Sie den Deal in DSP einrichten, indem Sie entweder die [!DNL Deal ID inbox] oder durch manuelles Eingeben der Details des Deals.

>[!NOTE]
>
> Bei PG-Angeboten verarbeitet der Herausgeber alle Budgetkürzungen, Budgetbegrenzungen und Targeting. Alle SSPs, die PG durch zulassen, DSP bestätigen, dass der Herausgeber eine Budgetbegrenzung einrichten kann.
>
> Einrichten programmgesteuerter garantierter Angebote für Herausgeber in [!DNL FreeWheel] erfordert zusätzliche Berechtigungen und Schritte. Siehe[Übersicht über die Einrichtung von programmatischen Garantievereinbarungen in [!DNL FreeWheel]](freewheel-overview.md)&quot;.

## Richten Sie mithilfe des [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

Dies ist die bevorzugte Methode für [!DNL FreeWheel], [!DNL Google Authorized Buyers]und [!DNL Magnite DV+].

1. [Akzeptieren des Deals](deal-id-inbox-accept.md).

1. Nachdem Sie den Deal gespeichert haben, wählen Sie die Anzeigen aus, die für den Deal verwendet werden sollen, und erstellen Sie eine programmgesteuerte, garantierte (PG) Standardplatzierung, wie Sie dazu aufgefordert werden.

   Die Erstellung einer standardmäßigen PG-Platzierung für den Deal ist obligatorisch, um 100 % Ihres Kaufs bereitzustellen. Dieser Platzierungstyp hat kein Targeting, sodass DSP jedem Angebotsantrag des Herausgebers ein Angebot zurückgeben kann.

   * Wenn Sie eine einzelne Transaktion akzeptieren, werden Sie automatisch zum Arbeitsablauf für die Erstellung der Platzierung mit PG-Standard weitergeleitet.

      Alle [!DNL FreeWheel] Vereinbarungen werden als eine einzige Vereinbarung vorgeschlagen.

   * Wenn Sie einen Vorschlag mit mehreren PG-Deal-IDs akzeptieren, identifizieren Sie jede PG-Standardplatzierung, die Sie erstellen müssen. Nachdem Sie alle erforderlichen Platzierungen erstellt haben, ist die Schaltfläche Weiter aktiviert.

1. (Optional) Richten Sie das Targeting des PG-Angebots in zusätzlichen PG- oder Nicht-PG-Platzierungen ein, indem Sie auf ![Optionen, Menü](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Ein Deal kann mehrere Platzierungen ansprechen, die eine beliebige Kombination von Medientypen unterstützen (z. B. vernetztes Fernsehen, Desktop und Audio).

## Manuelles Einrichten eines programmatischen Garantiedeals

Verwenden Sie diese Methode für alle anderen SSPs.

1. [Manuelles Einrichten der Details der Deal-ID](deal-id-create.md).

1. Nachdem Sie den Deal gespeichert haben, wählen Sie die Anzeigen aus, die für den Deal verwendet werden sollen, und erstellen Sie nach Aufforderung eine PG-Standardplatzierung.

   Die Erstellung einer PG-Standardplatzierung für den Kauf ist obligatorisch, um 100 % Ihres Kaufs bereitzustellen. Dieser Platzierungstyp hat kein Targeting, sodass DSP jedem Angebotsantrag des Herausgebers ein Angebot zurückgeben kann.

1. (Optional) Richten Sie das Targeting des PG-Angebots in zusätzlichen PG- oder Nicht-PG-Platzierungen ein, indem Sie auf ![Optionen, Menü](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   Ein Deal kann mehrere Platzierungen ansprechen, die eine beliebige Kombination von Medientypen unterstützen (z. B. vernetztes Fernsehen, Desktop und Audio).

>[!MORELIKETHIS]
>
>* [Über programmatische Garantievereinbarungen](programmatic-guaranteed-about.md)
>* [Tipps für die Aushandlung eines programmgesteuerten &quot;garantierten Angebots&quot;](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [Senden einer Anzeige für einen programmgesteuerten, garantierten Deal mit [!DNL FreeWheel]](freewheel-submit.md)
>* [Akzeptieren eines Angebots im Deal-ID-Posteingang](deal-id-inbox-accept.md)
>* [Manuelles Erstellen von Details zur Angebots-ID](deal-id-create.md)
>* [SSP-Partner](ssp-partners.md)
>* [Übersicht über die Funktionen des Bestands](inventory-overview.md)

