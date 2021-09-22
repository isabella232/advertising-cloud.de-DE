---
title: Über [!UICONTROL CCPA Opt-out-of-Sale] Segmente und Berichte
description: Erfahren Sie mehr über das Erstellen von Segmenten zur Verfolgung von IDs aus CCPA-Opt-out-Kaufanfragen und das Abrufen von Berichten über die IDs.
feature: CCPA, DSP Segments
exl-id: 9256d34e-d0dd-4abf-bc96-2b599caf2a8e
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# Über [!UICONTROL CCPA Opt-out-of-Sale] Segmente und Berichte

Sie können Benutzer-IDs aus Opt-out-Kaufanfragen von Verbrauchern auf Ihrer Website gemäß dem California Consumer Privacy Act (CCPA) verfolgen, indem Sie [ein CCPA-Opt-out-Kaufsegment](ccpa-opt-out-segment-create.md) erstellen und implementieren. Benutzer bleiben unbegrenzt in CCPA-Opt-out-Segmenten.

Sobald das Segment-Pixel-Tag implementiert ist, beginnt Advertising Cloud mit der Erfassung eines Pools von IDs im Namen des Advertisers.

## Opt-out-of-Sale-Berichte für Verbraucher

Advertising Cloud erstellt monatliche Berichte mit IDs, die Kunden für Opt-out-Kaufanfragen für das Konto gesendet haben. Die Daten konsolidieren Anforderungen, die mithilfe von CCPA-Opt-out-Kaufsegmenten erfasst wurden, die in Advertising Cloud DSP erstellt wurden, sowie alle über die Privacy Service-API durchgeführten Übermittlungen.  Die Berichte werden am ersten eines jeden Monats für den Vormonat erstellt. Beispielsweise ist die monatliche Benutzerliste für Juni am 1. Juli verfügbar.

Jeder Bericht ist als tabulatorgetrennte Textdatei verfügbar, die in das GZIP-Format komprimiert ist. In CCPA-Opt-out-Verkaufssegmenten erfasste Benutzer-IDs werden nach Segment und Advertiser identifiziert.

Sie können [Links zu den monatlichen Berichten](ccpa-opt-out-segment-report-retrieve.md) abrufen, die in den letzten drei Monaten erstellt wurden, entweder aus Advertising Cloud DSP oder über die Advertising Cloud [!DNL Trafficking API]. Jeder Link ist sieben Tage lang gültig, wird jedoch jedes Mal aktualisiert, wenn ein Kunde versucht, ihn abzurufen.

>[!MORELIKETHIS]
>
>* [Adobe Advertising Cloud-Unterstützung für den California Consumer Privacy Act: Opt-out-Support für Verbraucher](https://experienceleague.adobe.com/docs/advertising-cloud/privacy/ad-cloud-ccpa-opt-out-of-sale.html)
>* [Erstellen und Implementieren eines  [!UICONTROL CCPA Opt-Out-of-Sale] Segments](ccpa-opt-out-segment-create.md)
>* [Abruf von Kundenabmeldeberichten](ccpa-opt-out-segment-report-retrieve.md)
>* [Über Zielgruppen-Management](audience-about.md)

