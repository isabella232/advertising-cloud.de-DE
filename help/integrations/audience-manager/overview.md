---
title: Advertising Cloud-Integrationen mit Adobe Audience Manager
description: Erfahren Sie mehr über die verschiedenen Möglichkeiten, wie Advertising Cloud Daten mit Adobe Audience Manager austauschen kann.
feature: Integration with Adobe Audience Manager
source-git-commit: c761c96b32171bcfba12ed4a39235e6e8b6f6d34
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---

# Advertising Cloud-Integrationen mit Adobe Audience Manager

Sie können Advertising Cloud auf folgende Weise mit Audience Manager integrieren.

## Audience Manager und andere synchronisieren [!DNL Adobe] Segmente für Anzeigen-Targeting

Advertising Cloud Search und Advertising Cloud DSP können Metadaten, Hierarchie-Daten und eindeutige Zielgruppendaten für den gesamten Audience Manager eines Advertisers oder einer Agentur und andere abrufen [!DNL Adobe] Zielgruppen. Diese eindeutige Verbindung steht nur Marketing-Experten zur Verfügung, die Advertising Cloud verwenden. Siehe[Importieren von Adobe Audience Manager-Segmenten für Anzeigen-Targeting](/help/integrations/audience-manager/import-audiences.md).&quot;

### Audience Manager und andere verwenden [!DNL Adobe] Zu erstellende Segmente [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*Opt-in-Advertiser mit [!DNL Advertising Cloud Search] only*

Within [!DNL Search], können Sie [!DNL Google Ads] Google-Kundenabgleich von Zielgruppen aus Benutzer-IDs mithilfe Ihrer bestehenden Audience Manager-Segmente mit [!UICONTROL Adobe Media Optimizer (HTTP)] und [!UICONTROL Adobe Media Optimizer Batch Destination] als Ziele. ([!DNL Media Optimizer] ist ein früherer Name für Advertising Cloud Search.) Dazu gehören Adobe Analytics-Segmente, die in Adobe Experience Cloud veröffentlicht werden, und Segmente, die in Adobe Experience Cloud mithilfe der [!DNL People core service]. Weitere Informationen finden Sie in der produktinternen Hilfe unter [!DNL Search].

[Kundenabgleich von Zielgruppen aus Benutzer-IDs](https://support.google.com/google-ads/answer/9199250) funktioniert wie Website-Tag-basierte Zielgruppen, aber eindeutige Vorteile gegenüber standardmäßigen Kunden-Übereinstimmungen und Website-Tag-basierten Zielgruppen werden eindeutigen Zielgruppenmitgliedern eine Nicht-PII-ID zugewiesen.

Um die erforderlichen Benutzer-IDs zu erstellen, müssen Sie ein Advertising Cloud JavaScript-Tag verwenden <!-- with a user ID parameter -->auf Ihren Websites. Weitere Informationen erhalten Sie von Ihrem Advertising Cloud Search-Kundenbetreuungsteam.

![Segmenterstellungsvorgang](/help/integrations/assets/ad_search_user_id_pic.png)

Nachdem Sie die Zielgruppen erstellt haben, können Sie sie in [!DNL Google Ads] Kampagnen als [Ziele oder Ausschlüsse auf Kampagnenebene oder Anzeigengruppenebene](#audience-manager-targets).

### Verwenden Sie Audience Manager und andere [!DNL Adobe] Segmente in Target oder Ausschließen von Anzeigen {#audience-manager-targets}

* (Opt-in-Advertiser mit [!DNL Search]) Sie können jede [!DNL Google Ads] Zielgruppen, die [erstellt mit [!DNL Adobe] Segmente](#audience-manager-google-audiences) als Ziele oder Ausschlüsse auf Kampagnenebene oder Anzeigengruppenebene in Ihrem [!DNL Google Ads] Kampagnen.

* (Werbetreibende mit Advertising Cloud DSP) Sie können Ihre vorhandenen [!DNL Adobe] Segmente als Ziele für Ihre Anzeigenplatzierungen. Optional können Sie die Segmente in wiederverwendbare Zielgruppen einbeziehen, die Sie als Ziele oder Ausschlüsse für mehrere Platzierungen verwenden können.

* (Werbetreibende mit Advertising Cloud Creative) Sie können Ihre vorhandenen [!DNL Adobe] Segmente als Ziele für bestimmte Kreativinhalte in Ihren Anzeigenerlebnissen.

>[!NOTE]
>
>Weitere Informationen zum Erstellen von Zielgruppen in Audience Manager und Experience Cloud [!DNL Audience Library] Schnittstellen und gängige Anwendungsfälle für verschiedene Zielgruppentypen finden Sie unter[Optionen zur Zielgruppenerstellung](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html).&quot;

## Senden DSP Medien-Belichtungsdaten an den Audience Manager

*Advertiser nur mit DSP*

Advertising Cloud DSP-Kunden mit Adobe Audience Manager können Daten aus Anzeigenkampagnen mithilfe von Pixelaufrufen an Audience Manager erfassen. Anschließend können Sie die Kampagnendaten zur Erstellung regelbasierter Eigenschaften verwenden, mit denen Sie neue Segmente definieren können, um verschiedene Anwendungsfälle zu ermöglichen, wie z. B. erweiterte Segmentierung, Frequenzverwaltung, Marketing-Analyse und Einblicke in Berichte und Berichte.

Siehe[Übersicht über das Senden von DSP-Exposure-Daten an Adobe Audience Manager](/help/integrations/audience-manager/media-data-integration/overview.md)&quot;.

## Mit Audience Analytics erhalten Sie umfassendere Einblicke in die Site-Aktivität.

Advertising Cloud-Kunden mit [[!DNL Adobe][!DNL Audience Analytics]](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html) kann sowohl von Advertising Cloud verfolgte Daten als auch Audience Manager-Segmente an senden [!DNL Analytics] für erweiterte Einblicke in die Site-Aktivität.

Weitere Informationen finden Sie unter &quot;[[!DNL Adobe][!DNL Audience Analytics] für Advertising Cloud-Kunden](/help/integrations/audience-manager/audience-analytics.md).&quot;
