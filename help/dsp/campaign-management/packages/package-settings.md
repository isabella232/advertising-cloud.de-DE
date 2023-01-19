---
title: Paketeinstellungen
description: Siehe Beschreibungen der verfügbaren Paketeinstellungen.
feature: DSP Packages
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 0%

---

# Paketeinstellungen

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** Der Paketname. Die maximale Länge beträgt 60 Zeichen.

**[!UICONTROL Description]:** (Optional) Eine Beschreibung des Pakets.

**[!UICONTROL 3rd Party Billed Fees]:** (Optional) Eine statische Drittanbietergebühr, die als nicht abrechnungsfähige Kosten verfolgt werden soll:

>[!NOTE]
>
>Abrechenbare Gebühren werden im [!UICONTROL Net CPM] Metrik.
* **[!UICONTROL CPM]:** Die Kosten pro 1000 Impressionen (CPM).

* **[!UICONTROL CPM Description]:** Beschreibung der CPM-Gebühr.

Sie können die Einstellung auf Paketebene auf der [Platzierungsebene](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** (Schreibgeschützt für vorhandene Pakete) Auf welcher Ebene Platzierungen im Paket platziert und begrenzt werden sollen:

* **[!UICONTROL Package level pacing]:** Diese Schrittstrategie funktioniert durch Geschwindigkeit und Begrenzung aller enthaltenen Platzierungen als *Gruppe*. Diese Strategie stellt sicher, dass alle Platzierungen innerhalb eines Pakets ganzheitlich optimiert werden, indem die Ausgaben auf der Grundlage von Leistung und Skalierung auf ausgewählte KPIs (Key Performance Indicators) verteilt werden.

* **[!UICONTROL Placement level pacing]:**  Diese Schrittstrategie funktioniert durch Geschwindigkeit und Begrenzung aller enthaltenen Platzierungen *einzeln*. Die Best Practice ist, diese Strategie nur zu verwenden, um garantierte private Marktplatzierungen auszuführen.

**[!UICONTROL Flight Dates]:** Das Start- und Enddatum des Pakets.

Um optional nicht gerade Geschwindigkeitsflüge für das Paket zu erstellen, wählen Sie *[!UICONTROL *Activate Custom Flighting]** und richten benutzerdefinierte Flüge im [!UICONTROL Flighting] unten. Nachdem Sie die benutzerdefinierte Beleuchtung aktiviert und das Paket gespeichert haben, können Sie die benutzerdefinierte Beleuchtung nicht deaktivieren.

>[!NOTE]
>
>* Die Flugdaten müssen innerhalb der Flugdaten der Kampagne angegeben werden. Darüber hinaus müssen die Flugdaten für alle Platzierungen, die diesem Package zugewiesen werden, innerhalb dieser Daten enthalten sein.
> * Sie können das Startdatum des Pakets nicht bearbeiten, wenn die benutzerdefinierte Beleuchtung aktiviert ist.


**[!UICONTROL Budget]:** (Nur Pakete mit Geschwindigkeit auf Paketebene) Die Obergrenze des Bruttobudgets und das Budgetintervall.

Bei Paketen mit benutzerdefiniertem Flight ist das Budgetintervall immer *[!UICONTROL All time]*. Geben Sie für Pakete ohne benutzerdefinierte Beleuchtung das Budgetintervall an: *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* oder *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** (Nur Pakete mit Geschwindigkeit auf Paketebene und dynamischem Margenmanagement) Die Bruttobudgetsobergrenze für die Dauer des Pakets.

**[!UICONTROL Optimization Goal]:** (Nur Pakete mit Geschwindigkeit auf Paketebene) Das Optimierungsziel für das Paket. Beschreibungen der einzelnen Optimierungsziele finden Sie unter [Optimierungsziele und Verwendung](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goals]:** (Nur Pakete mit benutzerdefinierten Optimierungszielen) Die [benutzerdefiniertes Ziel](/help/dsp/optimization/custom-goal-about.md) für das Paket. Weitere Informationen zu Best Practices für benutzerdefinierte Ziele und Kampagnen, die sie verwenden, finden Sie unter  [Best Practices zum Erstellen eines benutzerdefinierten Ziels](/help/dsp/optimization/custom-goal-best-practices.md) und [Best Practices zum Einrichten von Leistungskampagnen](/help/dsp/optimization/campaign-best-practices-performance.md).

**[!UICONTROL Package Goal Type]:** (Nur Pakete mit benutzerdefinierten Optimierungszielen) Der Zweck des Pakets. Diese Einstellung hilft bei der Bestimmung, wie das Paket optimiert werden kann:

* *[!UICONTROL Prospecting]:* Interessante Pakete konzentrieren sich auf die Akquise neuer Kunden.

* *[!UICONTROL Retargeting]:* Retargeting-Pakete konzentrieren sich auf die Wiederbelebung früherer Besucher oder Kunden.

* *[!UICONTROL Other]:* Alle anderen Zwecke.

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** (Nur Pakete mit benutzerdefinierten Optimierungszielen) Ein weiteres Paket, dessen historische Daten als Eingabe für die Optimierung des Pakets verwendet werden.

**[!UICONTROL Target]:** (Nur Pakete mit Geschwindigkeit auf Paketebene) Das Zielziel, das zum Tracking der Leistung verwendet wird.

>[!NOTE]
>
>Dieses Feld ist nur ein Benchmark und wird nicht für die Entscheidungsfindung verwendet.

**[!UICONTROL Frequency Cap]:** (Nur Pakete mit Geschwindigkeit auf Paketebene) Die Häufigkeit, mit der ein eindeutiges Gerät oder eine eindeutige Person (abhängig von der angegebenen [!UICONTROL Cross Device Level] für die Kampagne) können Anzeigen aus dem Paket bereitgestellt werden. Optionen umfassen *[!UICONTROL Unlimited]* oder einen bestimmten Betrag pro Tag, Woche oder Monat.

>[!NOTE]
>
>* Sie können Frequenzobergrenzen auf Kampagnen-, Paket- und Platzierungsebene festlegen. DSP respektiert die strengste Frequenzgrenze in der Kampagnenhierarchie.
>* Die Best Practice besteht darin, Frequenzobergrenzen für die Prospektion und Retargeting auf Paketebene festzulegen.
> * Höhere Frequenzobergrenzen führen zu höheren Ausgaben und Impressionen, aber geringerer Reichweite. Niedrigere Frequenzobergrenzen führen zu geringeren Ausgaben und Impressionen, aber zu höherer Reichweite.


**[!UICONTROL Pace on]:** (Nur Pakete mit Pacing auf Paketebene) Worauf basiert:

* *[!UICONTROL Budget]:* (Standard) Diese Option liefert so viele Impressionen wie möglich innerhalb des zugewiesenen Package-Budgets.

* *[!UICONTROL Impressions]:* Diese Option liefert Impressionen, bis eine angegebene Menge innerhalb eines bestimmten Intervalls erreicht wird. Wenn Sie diese Option auswählen, geben Sie die Anzahl der Impressionen und das Intervall an: *Ganzzeit,* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* oder *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]:** (Nur Pakete mit Geschwindigkeit auf Paketebene) So beschleunigen Sie die Bereitstellung von Anzeigen über den gesamten Flug:

* *[!UICONTROL Even]:* Ermöglicht die gleichmäßige Bereitstellung während jedes Fluges mit einer Zielvorgabe von 50 % des Versands in der ersten Hälfte des Fluges.

* *[!UICONTROL Slightly Ahead]:* (Standardeinstellung) Beschleunigt den Versand, sodass er 55-65 % vollständig während der gesamten Flugdauer ist.

* *[!UICONTROL Frontload]:* Beschleunigen Sie den Versand, sodass er 65-75 % vollständig während des Fluges ist.

* *[!UICONTROL Aggressive Frontload]:* Beschleunigt den Versand, sodass 75-85 % des gesamten Fluges vollständig sind.

**[!UICONTROL Intraday pacing]:** (Nur Pakete mit Geschwindigkeit auf Paketebene) So beschleunigen Sie die Bereitstellung von Anzeigen über jeden Tag innerhalb des Fluges:

* *[!UICONTROL Even]:* (Standard) Skaliert die Bereitstellung auf der Grundlage der Lagerverfügbarkeit. Im Allgemeinen werden pro Stunde mehr Anzeigen zur Verfügung gestellt, wenn das Auktionsvolumen höher ist, und morgens und abends weniger Anzeigen geliefert.

* *[!UICONTROL ASAP]:* Beschleunigt die Bereitstellung auf die doppelte Geschwindigkeit von *Sogar*.

   >[!CAUTION]
   >
   >Diese Option kann sich negativ auf die Leistung auswirken. Verwenden Sie diese Option nur, wenn Sie die Bereitstellung vollständig priorisieren und die Leistungsoptimierung vorziehen.

## [!UICONTROL Flighting]

(Pakete mit Geschwindigkeit auf Paketebene und mit &quot;[!UICONTROL Activate Custom Flighting]&quot; aktiviert) Benutzerdefinierte Flugzeiträume innerhalb der Gesamtanzahl [!UICONTROL Flight Dates] im [!UICONTROL Goals & Budget] Abschnitt.

Geben Sie für jeden Flug das Startdatum, das Enddatum und die Zielanzahl der Impressionen an. Um einen weiteren Flug hinzuzufügen, klicken Sie auf **[!UICONTROL Add Flight]**.

>[!MORELIKETHIS]
>
>* [Über Package Management](package-about.md)
>* [Erstellen eines Pakets](package-create.md)
>* [Bearbeiten eines Pakets](package-edit.md)
>* [Platzierung an ein Paket anhängen](package-attach-placement.md)
>* [Anzeigen des Änderungsprotokolls für ein Paket](package-change-log.md)
>* [Häufig gestellte Fragen zu Campaign Management](/help/dsp/campaign-management/campaign-management-faq.md)

