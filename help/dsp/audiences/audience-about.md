---
title: Über Zielgruppen-Management in Advertising Cloud DSP
description: Erfahren Sie mehr über die Funktionen des Zielgruppen-Managements.
feature: Audiences, Segments
exl-id: 624d2211-59a2-4791-b8f1-a9a5cecd0b8e
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 0%

---

# Über Zielgruppen-Management in Advertising Cloud DSP

In Advertising Cloud DSP können Sie Zielgruppensegmente und Zielgruppensätze erstellen und verwalten, die Sie als Ziele für Ihre Platzierungen verwenden können:

* Sie können Ihre eigenen Erstanbieter-Zielgruppendaten erfassen, indem Sie Segmente erstellen und implementieren. Sie können später Benutzer im Segment mit Anzeigen erneut ansprechen oder verhindern, dass Benutzer im Segment Anzeigen empfangen. Sie können die folgenden Segmenttypen erstellen:

   * [Benutzerdefinierte ](/help/dsp/audiences/custom-segment-create.md) Segmente zur Verfolgung a) Benutzer, die Anzeigen von Desktop-, Mobil- und CTV-Geräten erhalten, und b) Benutzer, die bestimmte Webseiten besuchen.

   * [CCPA-Opt-out-of-Sale-](/help/dsp/audiences/ccpa-opt-out-segment-create.md) Segmente zur Verfolgung der Benutzer-IDs aus Opt-out-Kaufanfragen von Verbrauchern auf Ihrer Website gemäß dem California Consumer Privacy Act (CCPA). Sie können monatliche Berichte über die Benutzer-IDs aus Opt-out-Kaufanfragen abrufen.

      Weitere Informationen zur Advertising Cloud-Unterstützung für CCPA-Opt-out-of-Sale-Anfragen finden Sie unter [Adobe Advertising Cloud-Unterstützung für den California Consumer Privacy Act: Unterstützung für Opt-out für Verbraucher](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html).

* Sie können eine Zielgruppenbibliothek von [wiederverwendbaren Zielgruppen](/help/dsp/audiences/reusable-audience-create.md) erstellen. Gespeicherte Zielgruppen bestehen aus einem Ihrer verfügbaren Zielgruppensegmente und einer Ihrer anderen gespeicherten Zielgruppen. Alle Änderungen, die Sie an einer gespeicherten Zielgruppe vornehmen, werden automatisch auf alle Platzierungen angewendet, die die Zielgruppe als Ziel angeben oder ausschließen, sowie auf alle anderen Zielgruppen, die die gespeicherte Zielgruppe enthalten.

   Gespeicherte Zielgruppen ermöglichen es Medienplanern, Zielgruppen nach Bedarf zu gruppieren, indem mehrere Segmente mithilfe einer komplexen booleschen Logik einbezogen und ausgeschlossen werden. Die Größe jedes einzelnen Segments und die gesamte Zielgruppengröße werden beim Erstellen einer Zielgruppe angegeben. Kampagnenausführer können dann eine oder mehrere gespeicherte Zielgruppen als Platzierungsziele auswählen, anstatt Zielgruppenziele für jede Platzierung manuell zu konfigurieren.

Für das Platzierungs-Targeting stehen auch zusätzliche Zielgruppentypen zur Verfügung.

## Importieren von Erstanbieter- und Drittanbieter-Datensegmenten

Advertising Cloud DSP kann Ihre eigenen Erstanbieter-Datensegmente aus Ihrer Datenverwaltungsplattform (DMP) importieren und bei Bedarf für beliebige Advertiser bereitstellen.

Advertising Cloud DSP kann auch benutzerdefinierte Drittanbietersegmente importieren, einschließlich komplexer Kombinationen aus Drittanbietersegmenten. Sie können die Segmente nach Bedarf für beliebige Advertiser bereitstellen.

Weitere Informationen erhalten Sie von Ihrem Kundenbetreuer.

## Als Platzierungsziele verfügbare Zielgruppen

Sie können Ihre Platzierungen auf alle der folgenden Arten von Zielgruppen ausrichten.

* Alle vom Benutzer erstellten Zielgruppensätze, die in Advertising Cloud DSP gespeichert wurden.

* Alle vom Benutzer erstellten Zielgruppensegmente, die in Advertising Cloud DSP erstellt wurden:

   * Benutzerdefinierte Segmente für Benutzer, die bestimmte Webseiten besucht haben, und Benutzer, die Impressionen bestimmter Anzeigen ausgesetzt sind.

   * CCPA-Opt-out-of-Sale-Zielgruppensegmente für Benutzer, die Opt-out-Kaufanfragen auf Ihrer Website eingereicht haben, gemäß dem California Consumer Privacy Act (CCPA).

* Alle Ihre importierten Erstanbieter-Datensegmente.

* Alle von Ihnen importierten benutzerdefinierten Drittanbieter-Datensegmente.

* (Nur für die USA bestimmte Platzierungen) [Alle Datensegmente von Drittanbietern, die für Advertising Cloud DSP-Kunden von über 30 Anbietern verfügbar sind](/help/dsp/audiences/third-party-data-providers.md), einschließlich [!DNL Acxiom], [!DNL Datalogix], [!DNL eXelate] ([!DNL Nielsen]), [!DNL Lotame], [!DNL Oracle], [!DNL Quantcast] und vieles mehr.

   Sie können bestimmte Segmente als Ziel für Benutzer auswählen, die auf Zielgruppendaten basieren (z. B. Benutzer mit bestimmten demografischen Daten, Interessen oder Intents und/oder Verhaltensprofilen). Sie können nach Datenanbieter und Kategorie suchen, nach Segmenten nach Name oder Segment-ID suchen oder die Ergebnisse nach Datenanbieter, Gesamtgröße des Segments, Anzahl der Webbrowser oder Anzahl der Geräte filtern.

   Für Drittanbietersegmente fallen zusätzliche Gebühren an, die neben jedem Segmentnamen angegeben werden.

* (Werbetreibende mit Adobe Experience Cloud, Adobe Audience Manager oder Adobe Analytics, die nur JavaScript-Konversions-Tags von Advertising Cloud verwenden) Alle verfügbaren Erst-, Zweit- oder Drittanbieter-Zielgruppensegmente, die in Adobe Experience Cloud erstellt, in Audience Manager erstellt oder aus Audience Manager oder [!DNL Analytics] in Adobe Experience Cloud veröffentlicht wurden.

   Die Preise für die Verwendung der Segmente werden vorverhandelt und sind in Advertising Cloud nicht sichtbar.  <!-- Verify -->

   Segmente aus Adobe Experience Cloud sind etwa eine Stunde nach der Erstellung oder Veröffentlichung in Adobe Experience Cloud verfügbar. Segmente, die direkt von Audience Manager kommen, stehen etwa 24 Stunden nach ihrer Erstellung zur Verfügung. <!-- Verify all -->

   >[!NOTE]
   >
   >Informationen zum Einrichten und Erfassen von Daten für Segmente in diesen Lösungen finden Sie in der Dokumentation für [Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html), [Analytics](https://experienceleague.adobe.com/docs/analytics/landing/home.html) und [Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/audiences/audience-library.html) .

## Zielgruppengrößendaten

In den gespeicherten Zielgruppeneinstellungen und Platzierungseinstellungen können Sie detaillierte Daten zur Zielgruppengröße anzeigen:

* Die gesamte und die aktive deduplizierte Zielgruppengröße für alle ausgewählten Segmente und gespeicherten Zielgruppen wird angezeigt. Details können nach Gerätetyp (Browser, Mobilgerät oder vernetztes TV) angezeigt werden.

   ![die kombinierte Zielgruppengröße](/help/dsp/assets/audience-size.png)

* Für einzelne Segmente und gespeicherte Zielgruppen werden die Gesamtgröße der Zielgruppe und der CPM (falls zutreffend) neben dem Segmentnamen angezeigt. Sie können weitere Details zum Segment anzeigen, einschließlich der Größe nach Gerätetyp (Browser, Mobilgerät oder vernetztes TV). Bei gespeicherten Zielgruppen entspricht die Gesamtgröße dem deduplizierten Gesamtwert.

   ![die individuelle Segmentgröße](/help/dsp/assets/audience-size-segment.png)

## Ansichten der Zielgruppen

### Ansicht &quot;Alle Zielgruppen&quot;

In der [!UICONTROL All Audiences]-Ansicht oder in der Zielgruppenbibliothek können Sie wiederverwendbare Zielgruppen speichern und verwalten, zu denen auch Gruppen von Zielgruppensegmenten und sogar andere gespeicherte Zielgruppen gehören. Sie können Zielgruppen als Ziele für mehrere Platzierungen verwenden. Die Anzahl der Platzierungen, in denen jede Zielgruppe verwendet wird, wird neben dem Platzierungsnamen angezeigt.

Sie können beliebige Zielgruppen bearbeiten, klonen, löschen, exportieren oder freigeben.

### Die Segmentansicht

In der [!UICONTROL Segments]-Ansicht können alle Benutzer zusätzliche benutzerdefinierte Segmente erstellen.

Die Ansicht [!UICONTROL Segments] listet auch die folgenden Segmenttypen auf:

* Alle vom Benutzer erstellten benutzerdefinierten Segmente, die für den Benutzer verfügbar sind.

   Sie können Tracking-Tags für jedes der von Ihnen erstellten benutzerdefinierten Segmente anzeigen und diese Segmente für andere Benutzer freigeben. Sie können auch die von Ihnen erstellten benutzerdefinierten Segmente bearbeiten oder löschen.

   Sie können keine benutzerdefinierten Segmente bearbeiten oder freigeben, die andere Benutzer für Sie freigegeben haben.

* Alle importierten Erstanbietersegmente, die für den Benutzer verfügbar sind.

   Sie können keine Erstanbietersegmente bearbeiten oder freigeben, die für Sie freigegeben wurden. Wenden Sie sich an Ihren Kundenbetreuer, wenn Sie Erstanbietersegmente für zusätzliche Benutzer freigeben müssen.

* Alle benutzerdefinierten Drittanbietersegmente, die für den Benutzer verfügbar sind.

   Sie können keine Segmente von Drittanbietern bearbeiten oder freigeben, die für Sie freigegeben wurden. Wenden Sie sich an Ihren Kundenbetreuer, wenn Sie Segmente von Drittanbietern für weitere Benutzer freigeben möchten.

>[!MORELIKETHIS]
>
>* [Wiederverwendbare Zielgruppe erstellen](reusable-audience-create.md)
>* [Zielgruppeneinstellungen](audience-settings.md)
>* [Syntax für Zielgruppensegmentlogik](audience-segment-logic-syntax.md)
>* [Erstellen und Implementieren eines benutzerdefinierten Segments](custom-segment-create.md)
>* [Erstellen und Implementieren eines  [!UICONTROL CCPA Opt-Out-of-Sale] Segments](ccpa-opt-out-segment-create.md)
>* [Verfügbare Drittanbieter von Daten](third-party-data-providers.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)

