---
type: Documentation
cloud: Experience Cloud
solution: Advertising Cloud
product: advertising cloud
title: Über Listen auf Kontoebene und auf Advertiser-Ebene für blockierte Sites
description: Über Listen auf Kontoebene und auf Advertiser-Ebene für blockierte Sites
source-git-commit: ac35677ef4832177b7a7e735bbbbf24454371496
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# Über Listen auf Kontoebene und auf Advertiser-Ebene für blockierte Sites

<!-- Can you just add domains for your acct profile or advertiser to which you have access? It doesn't look like you can remove or edit any existing domains. Or can you with a specific syntax? -->

<!-- For domains, sub-domains,...? Specify what is valid. -->
Sie können die Liste der gesperrten Sites bearbeiten, die für das gesamte Advertising Cloud-Konto verwendet wird, sowie zusätzliche Listen für einzelne Advertiser im Konto.

Blockierte Sites definieren Zielgruppen, die für Ihre Platzierungen ausgeschlossen werden sollen. Jede Liste kann aus Top-Level-Website-Domänen und beliebigen Ebenen bestehen <!--- verify --> von Subdomains (z. B. beispiel.com, my.example.com oder my.new.example.com) und App-Namen (z. B. ???)<!-- package names/app IDs, the full URL in Google Play/iTunes? Specify what is valid. -->.

Listen auf Advertiser-Ebene überschreiben Listen auf Kontoebene.

>[!NOTE]
>
>* Zusätzlich zur Advertising Cloud DSP werden auf Kontoebene und auf Advertiser-Ebene blockierte Site-Listen angewendet [global gesperrte Site-Liste](/help/dsp/introduction/features/brand-safety-media-quality.md), die Sites enthalten, die für Anzeigen als unsicher gelten.
>* Benutzer können auch Targeting-Sites zu jeder Platzierung hinzufügen.
>* Listen blockierter Sites überschreiben immer Listen zielgerichteter Sites. Wenn durch eine Platzierung dieselbe Zielgruppe für eine Anzeige ausgeschlossen und einbezogen wird, wird die Zielgruppe ausgeschlossen. <!-- Verify -->


>[!MORELIKETHIS]
<!--
>* [Edit an Account-level or Advertiser-level Blocked Site List](/help/dsp/admin/blocked-sites-list-edit.md)
[Brand Safety and Media Quality](/help/dsp/introduction/features/brand-safety-media-quality.md)
>* [Placement Settings](/help/dsp/campaign-management/placements/placement-settings.md)
-->
