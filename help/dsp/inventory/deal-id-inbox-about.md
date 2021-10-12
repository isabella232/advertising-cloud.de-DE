---
title: Über die [!UICONTROL Deal ID Inbox]
description: Erfahren Sie mehr über die [!UICONTROL Deal ID inbox]-Funktion, mit der Sie private Angebote akzeptieren können, die Sie bereits mit Herausgebern über [!DNL FreeWheel], [!DNL Google Authorized Buyers] (formerly known as [!DNL AdX]), and [!DNL Magnite DV+] (früher [!DNL Rubicon]) ausgehandelt haben.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 959ad1d4-4671-4967-9f73-ec5b0464d0cd
source-git-commit: 8046ec79ec24f47fe33e49c6097e44dbba450f1f
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# Über die [!UICONTROL Deal ID Inbox]

DSP [!UICONTROL Deal ID inbox] ermöglicht Ihnen das schnelle Einrichten von Angeboten, die Advertising Cloud DSP über angebotsseitige Plattformen (SSPs) von Herausgebern importiert hat, sodass Sie nicht jedes Geschäft manuell einrichten müssen. Sie können die garantierten und nicht garantierten privaten Inventarangebote akzeptieren, die Sie bereits mit Herausgebern über [!DNL FreeWheel], [!DNL Google Authorized Buyers] (ehemals [!DNL AdX]) und [!DNL Magnite DV+] (ehemals [!DNL Rubicon]) aus [!UICONTROL Deal ID inbox] ausgehandelt haben.

>[!NOTE]
>
>Advertising Cloud DSP ist die erste DSP, die in die [!DNL FreeWheel]-API integriert wird.

Im [!UICONTROL Deal ID inbox] können Sie die Details des Geschäfts sehen, wie sie Ihr Herausgeber sieht, die Einrichtung von Deals beschleunigen und manuelle Einstiegsfehler vermeiden.

DSP aktualisiert automatisch täglich um 4:30 Uhr EST alle Details des Angebots. Außerdem werden alle [!DNL FreeWheel]-Angebote aktualisiert und vorhandene Angebote von [!DNL Google] und [!DNL Magnite DV+] stündlich aktualisiert. Sie können die Details des Deals auch manuell aktualisieren, um jederzeit neue Angebote zu füllen.

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>Bei programmgesteuerten garantierten Angeboten über [!DNL Google Authorized Buyers] müssen Sie mindestens 90 % Ihres Budgets bereitstellen. Andernfalls verliert Ihr Konto den Zugriff auf [!DNL Google]-Angebote im [!UICONTROL Deal ID inbox].

## Implementieren von [!UICONTROL Deal ID Inbox]

Um Ihre Angebote im [!UICONTROL Deal ID inbox] zu erhalten, müssen Ihre SSP-Konten das DSP Ihrer Organisation Ihrem SSP-Konto zuordnen. DSP teilt die Kontonamen des Unternehmens mit den relevanten SSPs. Wenden Sie sich für weitere Informationen an Ihren Kundenbetreuer von Adobe.

Teilen Sie dem Herausgeber bei den Vertragsverhandlungen mit, dass er den Deal an den Käufer und nicht an das DSP übergeben soll. Die Deal-ID kann je nach SSP ein Name oder eine ID sein.

## Maßnahmen, die Sie bei Ihren Angeboten ergreifen können

* **Überprüfen Sie die** Deals, um sicherzustellen, dass die SSP den richtigen Herausgeber, die richtigen Flugdaten, CPM und andere Details zu Deals gesendet hat. Wenn der Herausgeber einen Fehler gemacht hat, kontaktieren Sie ihn außerhalb von DSP, damit er den Vorgang korrigieren und erneut versenden kann.

* **Akzeptieren Sie** Deals nach der Überprüfung, und sie werden nicht mehr in der  [!UICONTROL Deal ID inbox]angezeigt. Akzeptierte Angebote werden unter [!UICONTROL Inventory] > [!UICONTROL Deals] aufgelistet und können innerhalb der Platzierungen von Werbetreibenden gezielt ausgewählt werden.

* **Ignorieren Sie** Geschäfte, die nicht benötigt werden oder unerwünscht sind. Ignorierte Angebote werden in die Registerkarte [!UICONTROL Ignored Deals] im [!UICONTROL Deal ID inbox] verschoben, die als Archiv dient. DSP benachrichtigt keine SSPs und Herausgeber, wenn Sie Angebote ignorieren.

* **Ändern Sie die Details für bereits akzeptierte** Händler von  [!UICONTROL Inventory] >  [!UICONTROL Deals] (nicht im  [!UICONTROL Deal ID inbox]). Wenn Herausgeber Änderungen an Angeboten senden, sind Advertiser für die Implementierung dieser Änderungen in [!UICONTROL Inventory] > [!UICONTROL Deals] verantwortlich, da die [!UICONTROL Deal ID inbox] Änderungen von den SSPs nach der Einrichtung von Angeboten nicht synchronisiert.

## Welche Arten von Angeboten können nicht akzeptiert werden?

Wenn eine Liste von Angeboten kein ![Accept](/help/dsp/assets/accept.png)-Symbol oder eine [!UICONTROL Accept]-Schaltfläche enthält, können Sie sie nicht über [!UICONTROL Deal ID inbox] akzeptieren. Stattdessen können Sie [die Details der Deal-ID manuell erstellen](/help/dsp/inventory/deal-id-create.md).

Sie können die folgenden Arten von Angeboten nicht akzeptieren:

* [!DNL Google] Angebote, die nicht in USD enthalten sind.

* [!DNL Magnite DV+] Angebote, die nicht in USD enthalten sind

* [!DNL FreeWheel] Angebote, die nicht in Ihrer Kontowährung enthalten sind.

* Angebote mit einem Enddatum bis heute

* Alte [!DNL Magnite DV+]-Angebote, die als &quot;mehrere Medientypen&quot;bezeichnet wurden.

Die Details des Deals enthalten den Grund, warum das Geschäft nicht akzeptiert werden kann.

>[!MORELIKETHIS]
>
>* [Akzeptieren eines Angebots im Deal-ID-Posteingang](deal-id-inbox-accept.md)
>* [Übersicht über die Funktionen des Bestands](inventory-overview.md)

