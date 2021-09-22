---
title: Häufig gestellte Fragen zur Kampagnenverwaltung
description: Erfahren Sie mehr über das Kampagnenmanagement, einschließlich der Wartezeit für Änderungen und was passiert, wenn Sie während eines Fluges Budgetänderungen vornehmen.
feature: DSP Packages, DSP Placements
exl-id: 9034ab2c-b8b0-4759-bc87-5f73857bb062
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# Häufig gestellte Fragen zur Kampagnenverwaltung

<!-- Most of this information should be moved into the relevant topics (especially editing topics). -->

## Latenz der Einstellungsänderungen

* Wann wird die Änderung wirksam, wenn Sie eine Platzierungs- oder Paketeinstellung ändern?

   Einstellungsänderungen treten in der Regel sofort in Kraft, können jedoch bis zu 12 Stunden dauern.

   Wenn es der letzte Bereitstellungstag ist, nehmen Sie Änderungen frühzeitig vor, damit DSP genügend Zeit hat, das Paket basierend auf den Änderungen neu zu alibrieren. Wenn Sie z. B. von der gerade Geschwindigkeit zum Frontload-Geschwindigkeit wechseln, muss DSP neu bewerten, wie die Ausgaben auf den Rest des Fluges verteilt werden. Nehmen Sie diese Änderung nicht vor, wenn Sie nur noch eine Stunde Zeit haben, um am letzten Tag des Fluges zu liefern.

## Budgetaktualisierungen - Mid-Flight

* Wie lange dauert es DSP, wenn Sie eine Platzierung ändern, um das Package-Budget neu zuzuweisen?

   Die Budgetzuweisung basiert auf der Platzierungsleistung, die anhand eines Durchschnitts von 14 Tagen bewertet wird. Änderungen an einer Platzierung führen nur dann zu Änderungen an der Budgetzuweisung, wenn sie Leistungsänderungen während des 14-Tage-Durchschnitts verursachen.

   Wenn Leistungsänderungen auftreten, ordnet DSP das Package-Budget während des nächsten Budgetoptimierungszyklus, der etwa um Mitternacht (00:00 Uhr) in der Zeitzone der Kampagne stattfindet, entsprechend den Platzierungen zu.

* Wie wird das Budget neu zugewiesen, wenn eine Platzierung aus einem Paket entfernt und zu einem anderen Paket hinzugefügt wird?

   Der gesamte Ausgabenverlauf einer Platzierung wird an die Platzierung angehängt und damit von Paket zu Paket verschoben.

   Wenn Sie eine Platzierung aus einem Paket entfernen, hat das Paket keinen Verlauf der Platzierungsausgaben mehr. Das Package-Budget wird (Package-Budget - entferntes Platzierungs-Budget) / verbleibendes Zeitintervall im Flug sein. Das Paket-Budget wird dann den Platzierungen zugewiesen, die im Paket verbleiben.

   Wenn Sie dieselbe Platzierung zu einem anderen Paket hinzufügen, berücksichtigt DSP den Ausgabenverlauf der Platzierung, wenn das Budget für alle Platzierungen im neuen Paket zugewiesen wird.

* Wie ändert sich das Package-Tempo am letzten Tag eines Fluges?

   Am letzten Tag eines Fluges wird der Tag von 24 Stunden auf 23 Stunden verkürzt, sodass das Budget des Pauschalangebots nicht überschritten wird. Außerdem ändert sich die Strategie für das Abfüllen des Pakets automatisch in &quot;[!UICONTROL Frontload]&quot;, auch wenn sie auf &quot;[!UICONTROL even]&quot;festgelegt ist. Das bedeutet, dass 65 % des täglichen Budgets bis 11:30 Uhr EST bereitgestellt werden sollten.

>[!MORELIKETHIS]
>
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)
>* [Best Practices zum Einrichten von Leistungskampagnen](/help/dsp/optimization/campaign-best-practices-performance.md)

