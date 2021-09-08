---
title: Adobe Advertising Cloud-Unterstützung für den California Consumer Privacy Act &#58; Unterstützung für Opt-out-of-Sale für Verbraucher
description: Erfahren Sie mehr über die Unterstützung für die Erfassung von Opt-out-Anfragen von Verbrauchern.
feature: CCPA, CCPA Opt-out-of-sale Segments
exl-id: 2c0cd4f5-798f-479a-99cd-f555cd676766
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '1036'
ht-degree: 0%

---

# Adobe Advertising Cloud-Unterstützung für den California Consumer Privacy Act: Abmeldung von der Verkaufsunterstützung durch Verbraucher

*Für Adobe Advertising Cloud-Demand Side Platform*

>[!IMPORTANT]
>
>Der Inhalt dieses Dokuments ist keine Rechtsberatung und soll keine Rechtsberatung ersetzen. Wenden Sie sich an Ihren Rechtsbeistand, um Ratschläge zum California Consumer Privacy Act zu erhalten.

Der California Consumer Privacy Act (CCPA) ist das neue kalifornische Datenschutzgesetz, das am 1. Januar 2020 in Kraft tritt. Der CCPA gibt in Kalifornien ansässigen Personen neue Rechte in Bezug auf ihre personenbezogenen Daten und verpflichtet bestimmte in Kalifornien tätige Unternehmen zur Einhaltung von Datenschutzvorschriften. Der CCPA bietet Verbrauchern das Recht, auf ihre Daten zuzugreifen und sie zu löschen sowie bestimmte Aktivitäten, die als &quot;Verkauf&quot;personenbezogener Daten an Dritte gelten, abzuwählen.

Als Unternehmen legen Sie fest, welche personenbezogenen Daten Adobe Experience Cloud in Ihrem Namen verarbeitet und speichert.

Adobe Advertising Cloud unterstützt Ihr Unternehmen als Ihren Dienstleister bei der Erfüllung seiner CCPA-Verpflichtungen, die für die Verwendung von Advertising Cloud-Produkten und -Diensten gelten, einschließlich der Verwaltung von Anfragen von Verbrauchern zum Zugriff auf und zur Löschung personenbezogener Daten und der Verwaltung von Verbraucheranfragen, mit denen der Verkauf personenbezogener Daten abgelehnt werden soll.

In diesem Dokument wird beschrieben, wie Adobe Advertising Cloud Demand Side Platform (DSP) als Dienstleister das Verbraucherrecht unterstützt, sich vom &quot;Verkauf&quot;von &quot;personenbezogenen Daten&quot;abzumelden, da jeder Begriff vom CCPA definiert wird. Er enthält Informationen dazu, wie Sie Advertising Cloud Opt-out-Kaufanfragen mitteilen und Berichte zu den Opt-out-Kaufanfragen Ihres Unternehmens abrufen können.

Informationen dazu, wie Advertising Cloud Search, Advertising Cloud Creative, Advertising Cloud DSP (Demand Side Platform) und Media Optimizer DCO die Zugriffs- und Löschungsrechte von Verbrauchern für personenbezogene Daten unterstützen, finden Sie unter [Adobe Advertising Cloud-Unterstützung für den California Consumer Privacy Act: Unterstützung für Zugriff auf und Löschen von Verbraucherdaten](/help/privacy/ad-cloud-ccpa-access-delete.md).

Weitere Informationen zu den Adobe Privacy Services für CCPA finden Sie im [Adobe Privacy Center](https://www.adobe.com/privacy/ccpa.html).

## Übermittlung von Opt-out-Anfragen von Verbrauchern an Advertising Cloud

Sie können Verbraucher-Opt-out-Anfragen für den Verkauf über eine der folgenden Methoden kommunizieren:

* ein in Advertising Cloud DSP erstelltes CCPA-Opt-out-Kaufsegment
* die Adobe Experience Platform Privacy Service-API

### Methode 1: Kommunizieren von CCPA-Opt-out-of-Sale-Anfragen mithilfe eines [!UICONTROL CCPA Opt-Out-of-Sale]-Segments in Advertising Cloud DSP

>[!NOTE]
>
>Benutzer bleiben unbegrenzt in CCPA-Opt-out-Segmenten.

1. Melden Sie sich unter [https://advertising.adobe.com/](https://advertising.adobe.com/) beim Advertiser-Konto in Advertising Cloud DSP an.
1. [Erstellen Sie ein CCPA-Opt-out-Kaufsegment und implementieren Sie das Segmentpixel, um die Opt-out-Anfragen](/help/dsp/audiences/ccpa-opt-out-segment-create.md) zu erfassen.

### Methode 2: CCPA-Opt-out-of-Sale-Anfragen mithilfe der Adobe Experience Platform Privacy Service-API kommunizieren

*Werbetreibende, denen nur eine Experience Cloud-Organisations-ID (IMS-Organisations-ID) zugewiesen wurde*

1. Stellen Sie eine JavaScript-Bibliothek bereit, um die Cookies Ihrer Kunden abzurufen. Dieselbe Bibliothek `AdobePrivacy.js` wird für alle Adobe Experience Cloud-Lösungen verwendet.

   >[!IMPORTANT]
   >
   >Für Anforderungen an einige Adobe Experience Cloud-Lösungen ist keine JavaScript-Bibliothek erforderlich, für Anfragen an Advertising Cloud ist dies jedoch erforderlich.

   Sie sollten die Bibliothek auf der Webseite bereitstellen, von der aus Ihre Kunden Opt-out-Kaufanfragen senden können, z. B. das Datenschutzportal Ihres Unternehmens. Die Bibliothek hilft Ihnen beim Abrufen von Adobe-Cookies (Namespace-ID: `gsurferID`), damit Sie diese Identitäten als Teil von Opt-out-Kaufanfragen über die Adobe Experience Platform Privacy Service-API senden können.

1. Identifizieren Sie Ihre IMS-Organisations-ID und stellen Sie sicher, dass sie mit Ihren Advertising Cloud-Konten verknüpft ist.

   Eine IMS-Organisations-ID ist eine 24-stellige alphanumerische Zeichenfolge, die an @AdobeOrg angehängt wird. Den meisten Adobe Experience Cloud-Kunden wurde eine IMS-Organisations-ID zugewiesen. Wenn Ihr Marketing-Team oder der Systemadministrator Ihrer Adobe die IMS-Organisations-ID Ihres Unternehmens nicht kennen oder nicht sicher ist, ob die Kennung bereitgestellt wurde, wenden Sie sich an die Kundenunterstützung von Adobe unter gdprsupport@adobe.com. Sie benötigen die IMS-Organisations-ID, um Anfragen an die Datenschutz-API zu senden.

   >[!IMPORTANT]
   >
   >Wenden Sie sich an den Advertising Cloud-Support-Mitarbeiter Ihres Unternehmens, um zu bestätigen, dass alle Advertising Cloud-Konten Ihres Unternehmens - einschließlich [!DNL DSP]-Konten oder -Advertiser, [!DNL Search]-Konten und [!DNL Creative]- oder [!DNL DCO]-Konten - mit Ihrer IMS-Organisations-ID verknüpft sind.

1. Verwenden Sie die Adobe Experience Platform Privacy Service-API, um [Opt-out-of-Sale-Anfragen](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) im Namen von Verbrauchern an Advertising Cloud zu senden und den Status vorhandener Anfragen zu überprüfen.

   Im folgenden Anhang finden Sie ein Beispiel für eine Opt-out-Kaufanfrage.

   >[!NOTE]
   Wenn Ihr Unternehmen über mehrere Adobe Experience Cloud Identity Management Service-Organisations-IDs (IMS-Organisations-IDs) verfügt, müssen Sie für jede einzelne API-Anfrage separate API-Anfragen senden. Sie können jedoch eine API-Anfrage an mehrere Advertising Cloud-Unterlösungen ([!DNL Search], [!DNL Creative], [!DNL DSP] und [!DNL DCO]) mit einem Konto pro Unterlösung richten.

Alle diese Schritte sind erforderlich, um Unterstützung von Advertising Cloud zu erhalten. Weitere Informationen zu diesen und anderen zugehörigen Aufgaben, die Sie mit der Adobe Experience Platform Privacy Service ausführen müssen, sowie dazu, wo Sie die benötigten Elemente finden können, finden Sie unter [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Abrufen von Berichten von Verbrauchern, die Opt-out-Kaufanfragen eingereicht haben

Advertising Cloud erstellt monatliche Berichte mit IDs, die Kunden für Opt-out-Kaufanfragen für das Konto gesendet haben. Jeder Bericht ist als tabulatorgetrennte Textdatei verfügbar, die in das GZIP-Format komprimiert ist. Die Daten konsolidieren Anforderungen, die mithilfe von CCPA-Opt-out-Kaufsegmenten erfasst wurden, die in Advertising Cloud DSP erstellt wurden, sowie alle über die Privacy Service-API durchgeführten Übermittlungen. In CCPA-Opt-out-Verkaufssegmenten erfasste Benutzer-IDs werden nach Segment und Advertiser identifiziert. Die Berichte werden am ersten eines jeden Monats für den Vormonat erstellt. Beispielsweise ist die monatliche Benutzerliste für Juni am 1. Juli verfügbar.

Sie können Links zu den monatlichen Berichten abrufen, die in den letzten drei Monaten erstellt wurden, entweder aus Advertising Cloud DSP oder über die Advertising Cloud [!DNL Trafficking API]. Jeder Link ist sieben Tage lang gültig, wird jedoch jedes Mal aktualisiert, wenn ein Kunde versucht, ihn abzurufen.

### Methode 1: Abrufen von Kundenabmeldeberichten in Advertising Cloud DSP

1. Melden Sie sich unter [https://advertising.adobe.com/](https://advertising.adobe.com/) beim Advertiser-Konto in Advertising Cloud DSP an.
1. [Rufen Sie die Berichte](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md) ab.

### Methode 2: Abrufen von Kundenabmeldeberichten mit Advertising Cloud [!DNL Trafficking API]

Diese Funktion steht Unternehmen zur Verfügung, die [!DNL Trafficking API] verwenden. Weitere Informationen finden Sie in der Dokumentation für [!DNL Trafficking API] .

Wenn Ihr Unternehmen die [!DNL Trafficking API] nicht verwendet, aber an weiteren Informationen interessiert ist, wenden Sie sich an Ihren Kundenbetreuer von Adobe.

## Anhang: Beispiel [!UICONTROL CCPA Opt-Out-of-Sale] Anforderung für Privacy Service-API-Benutzer

```
curl -X POST \
  https://platform.adobe.io/data/privacy/gdpr/ \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'Content-Type: application/json' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -d '{
    "companyContexts": [
      {
        "namespace": "imsOrgID",
        "value": "{IMS_ORG}"
      }
    ],
    "users": [
      {
        "key": "DavidSmith",
        "action": ["opt-out-of-sale"],
        "userIDs": [
          {
            "namespace": "email",
            "value": "dsmith@acme.com",
            "type": "standard"
          },
          {
            "namespace": "AdCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["AdCloud"],
    "regulation": "ccpa"
}'
```

wobei:

* `"namespace": "AdCloud"` gibt den  `AdCloud` Cookie-Bereich an und der entsprechende Wert ist die Cookie-ID des Kunden, wie sie von abgerufen wird.  `AdobePrivacy.js`
* `"include": ["AdCloud"]` gibt an, dass die Anforderung für Advertising Cloud gilt
