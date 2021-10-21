---
title: Über die [!UICONTROL Deal ID Inbox]
description: Erfahren Sie mehr über die [!UICONTROL Deal ID inbox] -Funktion, mit der Sie private Angebote akzeptieren können, über die Sie bereits mit Herausgebern verhandelt haben [!DNL FreeWheel], [!DNL Google Authorized Buyers] (formerly known as [!DNL AdX]), and [!DNL Magnite DV+] (früher [!DNL Rubicon]).
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 959ad1d4-4671-4967-9f73-ec5b0464d0cd
source-git-commit: 2539d9b8ec7de7202dd6c3400dda85aa133853e3
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# Über die [!UICONTROL Deal ID Inbox]

DSP [!UICONTROL Deal ID inbox] ermöglicht Ihnen das schnelle Einrichten von Angeboten, die Advertising Cloud DSP über angebotsseitige Plattformen (SSPs) von Herausgebern importiert hat, sodass Sie nicht jedes Geschäft manuell einrichten müssen. Sie können die garantierten und nicht garantierten privaten Inventarangebote akzeptieren, die Sie bereits mit Herausgebern über [!DNL FreeWheel], [!DNL Google Authorized Buyers] (früher bekannt als [!DNL AdX]) und [!DNL Magnite DV+] (früher [!DNL Rubicon]) aus dem [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>Advertising Cloud DSP ist die erste DSP, die in die [!DNL FreeWheel] API.

Im [!UICONTROL Deal ID inbox], können Sie die Details des Deals sehen, wie Ihr Herausgeber sie sieht, Ihre Deal-Einrichtung beschleunigen und manuelle Einstiegsfehler vermeiden.

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.
   
You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSP aktualisiert automatisch täglich um 4:30 Uhr EST alle Details des Angebots. Außerdem werden alle [!DNL FreeWheel] Angebote und aktuelle Angebote aus [!DNL Google] und [!DNL Magnite DV+] stündlich. Sie können die Details des Deals auch manuell aktualisieren, um jederzeit neue Angebote zu füllen.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>Für programmgesteuerte garantierte Angebote durch [!DNL Google Authorized Buyers]müssen Sie mindestens 90 % Ihres Budgets einsetzen, sonst verliert Ihr Konto den Zugriff auf [!DNL Google] Angebote in [!UICONTROL Deal ID inbox].

## Implementieren der [!UICONTROL Deal ID Inbox]

So erhalten Sie Ihre Angebote im [!UICONTROL Deal ID inbox]müssen Ihre SSP-Konten das DSP Ihres Unternehmens Ihrem SSP-Konto zuordnen. DSP teilt die Kontonamen des Unternehmens mit den relevanten SSPs. Wenden Sie sich an [!DNL Adobe] Kundenbetreuer für Anweisungen.

Teilen Sie dem Herausgeber bei den Vertragsverhandlungen mit, dass er den Deal an den Käufer und nicht an das DSP übergeben soll. Die Deal-ID kann je nach SSP ein Name oder eine ID sein.

## Maßnahmen, die Sie bei Ihren Angeboten ergreifen können

* **Überprüfungstermine** , um zu überprüfen, ob die SSP den richtigen Herausgeber, die richtigen Flugdaten, CPM und andere Details zu Geschäften gesendet hat. Wenn der Herausgeber einen Fehler gemacht hat, kontaktieren Sie ihn außerhalb von DSP, damit er den Vorgang korrigieren und erneut versenden kann.

* **Accept-Angebote** nach der Überprüfung und sie werden nicht mehr im [!UICONTROL Deal ID inbox]. Akzeptierte Angebote sind in [!UICONTROL Inventory] > [!UICONTROL Deals] und sind bereit, innerhalb der Platzierungen von Werbetreibenden Targeting durchzuführen.

* **Ignorieren von Geschäften** die nicht benötigt werden oder unerwünscht sind. Ignorierte Angebote werden in die [!UICONTROL Ignored Deals] innerhalb der [!UICONTROL Deal ID inbox], das als Archiv dient. DSP benachrichtigt keine SSPs und Herausgeber, wenn Sie Angebote ignorieren.

* **Ändern von Details für bereits akzeptierte Angebote** von [!UICONTROL Inventory] > [!UICONTROL Deals] (nicht im [!UICONTROL Deal ID inbox]). Wenn Herausgeber Änderungen an Angeboten senden, sind Advertiser für die Implementierung dieser Änderungen in [!UICONTROL Inventory] > [!UICONTROL Deals] weil die [!UICONTROL Deal ID inbox] synchronisiert keine Änderungen von den SSPs, nachdem Angebote eingerichtet wurden.

## Welche Arten von Angeboten können nicht akzeptiert werden?

Wenn eine Liste von Angeboten keine ![Accept](/help/dsp/assets/accept.png) oder [!UICONTROL Accept] -Schaltfläche, können Sie sie nicht über [!UICONTROL Deal ID inbox]. Stattdessen können Sie [Manuelles Erstellen der Details der Deal-ID](/help/dsp/inventory/deal-id-create.md).

Sie können die folgenden Arten von Angeboten nicht akzeptieren:

* [!DNL Google] Angebote, die nicht in USD enthalten sind.

* [!DNL Magnite DV+] Angebote, die nicht in USD enthalten sind

* [!DNL FreeWheel] Angebote, die nicht in Ihrer Kontowährung enthalten sind.

* Angebote mit einem Enddatum bis heute

* Old [!DNL Magnite DV+] Angebote, die als &quot;mehrere Medientypen&quot;bezeichnet wurden.

Die Details des Deals enthalten den Grund, warum das Geschäft nicht akzeptiert werden kann.

>[!MORELIKETHIS]
>
>* [Akzeptieren eines Angebots im Deal-ID-Posteingang](deal-id-inbox-accept.md)
>* [Übersicht über die Funktionen des Bestands](inventory-overview.md)

