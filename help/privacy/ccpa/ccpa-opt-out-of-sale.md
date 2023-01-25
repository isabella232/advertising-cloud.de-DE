---
title: 'Adobe Advertising-Unterstützung für den California Consumer Privacy Act : Unterstützung für Opt-out-of-Sale für Verbraucher'
description: Erfahren Sie mehr über die Unterstützung für die Erfassung von Opt-out-Anfragen von Verbrauchern.
feature: CCPA
exl-id: df2b8679-8a1c-4cd7-b867-cd2f53c76c8f
source-git-commit: e9d9d51302d32b06af805917db2f46e5f6daee62
workflow-type: tm+mt
source-wordcount: '1003'
ht-degree: 0%

---

# Adobe Advertising Support für den California Consumer Privacy Act: Abmeldung von der Verkaufsunterstützung durch Verbraucher

*Für Adobe Advertising Demand Side Platform (DSP)*

>[!IMPORTANT]
>
>Der Inhalt dieses Dokuments ist keine Rechtsberatung und soll keine Rechtsberatung ersetzen. Wenden Sie sich an Ihren Rechtsbeistand, um Ratschläge zum California Consumer Privacy Act zu erhalten.

Der California Consumer Privacy Act (CCPA) ist das neue kalifornische Datenschutzgesetz, das am 1. Januar 2020 in Kraft tritt. Der CCPA gibt in Kalifornien ansässigen Personen neue Rechte in Bezug auf ihre personenbezogenen Daten und verpflichtet bestimmte in Kalifornien tätige Unternehmen zur Einhaltung von Datenschutzvorschriften. Der CCPA bietet Verbrauchern das Recht, auf ihre Daten zuzugreifen und sie zu löschen sowie bestimmte Aktivitäten, die als &quot;Verkauf&quot;personenbezogener Daten an Dritte gelten, abzuwählen.

Als Unternehmen legen Sie fest, welche personenbezogenen Daten Adobe Experience Cloud in Ihrem Namen verarbeitet und speichert.

Als Dienstleister unterstützt Adobe Advertising Ihr Unternehmen bei der Erfüllung seiner CCPA-Verpflichtungen, die für die Verwendung von Adobe Advertising-Produkten und -Dienstleistungen gelten. Dazu gehört die Verwaltung von Anfragen von  zum Zugriff auf und zur Löschung personenbezogener Daten sowie die Verwaltung von Anfragen von Verbrauchern, sich vom Verkauf personenbezogener Daten abzumelden.

In diesem Dokument wird beschrieben, wie Adobe Advertising Demand Side Platform (DSP) als Dienstleister das Verbraucherrecht unterstützt, sich vom &quot;Verkauf&quot;von &quot;personenbezogenen Daten&quot;abzumelden, da jeder Begriff vom CCPA definiert wird. Er enthält Informationen dazu, wie Sie Opt-out-Kaufanfragen an Adobe Advertising weiterleiten und wie Sie Berichte über die Opt-out-Kaufanfragen Ihres Unternehmens abrufen können.

Informationen zum [!DNL Advertising Search]; Werbegestaltung; und [!DNL Advertising DCO] Unterstützung der Zugriffs- und Löschungsrechte für personenbezogene Daten von Verbrauchern, siehe [Adobe Advertising Support für den California Consumer Privacy Act: Unterstützung für Zugriff auf Kundendaten und Löschung](/help/privacy/ccpa/ccpa-access-delete.md).

Weitere Informationen zu den Adobe Privacy Services für CCPA finden Sie im Abschnitt [Datenschutzzentrum für Adoben](https://www.adobe.com/privacy/ccpa.html).

## Übermittlung von Opt-out-of-Sale-Anfragen an Adobe Advertising

Sie können Verbraucher-Opt-out-Anfragen für den Verkauf über eine der folgenden Methoden kommunizieren:

* ein CCPA-Opt-out-Kaufsegment, das in Advertising DSP erstellt wurde
* die Adobe Experience Platform Privacy Service-API

### Methode 1: Kommunizieren von CCPA-Opt-out-of-Sale-Anfragen mithilfe eines [!UICONTROL CCPA Opt-Out-of-Sale] Segment in Advertising DSP

>[!NOTE]
>
>Benutzer bleiben unbegrenzt in CCPA-Opt-out-Segmenten.

1. Melden Sie sich im Advertising DSP unter dem Advertising-Konto an. [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Erstellen Sie ein CCPA-Opt-out-Kaufsegment und implementieren Sie das Segmentpixel, um die Opt-out-Anfragen zu erfassen.](/help/dsp/audiences/ccpa-opt-out-segment-create.md).

### Methode 2: CCPA-Opt-out-of-Sale-Anfragen mithilfe der Adobe Experience Platform Privacy Service-API kommunizieren

*Werbetreibende, denen nur eine Adobe Experience Cloud-Organisations-ID zugewiesen wurde*

1. Stellen Sie eine JavaScript-Bibliothek bereit, um die Cookies Ihrer Kunden abzurufen. Dieselbe Bibliothek, `AdobePrivacy.js`, wird für alle Adobe Experience Cloud-Lösungen verwendet.

   >[!IMPORTANT]
   >
   >Für Anforderungen an einige Adobe Experience Cloud-Lösungen ist keine JavaScript-Bibliothek erforderlich, für Anfragen an Adobe Advertising ist dies jedoch erforderlich.

   Sie sollten die Bibliothek auf der Webseite bereitstellen, von der aus Ihre Kunden Opt-out-Kaufanfragen senden können, z. B. das Datenschutzportal Ihres Unternehmens. Die Bibliothek hilft Ihnen beim Abrufen von Adobe-Cookies (Namespace-ID: `gsurferID`), damit Sie diese Identitäten als Teil von Opt-out-Kaufanfragen über die Adobe Experience Platform Privacy Service-API senden können.

1. Identifizieren Sie Ihre Experience Cloud-Organisations-ID und stellen Sie sicher, dass sie mit Ihren Adobe Advertising-Konten verknüpft ist.

   Eine Experience Cloud-Organisations-ID ist eine 24-stellige alphanumerische Zeichenfolge, die an &quot;@AdobeOrg&quot;angehängt wird. Den meisten Experience Cloud-Kunden wurde eine Organisations-ID zugewiesen. Wenn Ihr Marketing-Team oder Ihr Systemadministrator Ihrer Adobe Ihre Organisations-ID nicht kennen oder nicht sicher ist, ob die ID bereitgestellt wurde, wenden Sie sich an die Kundenunterstützung von Adobe unter gdprsupport@adobe.com. Sie benötigen die Organisations-ID, um Anfragen über die `imsOrgID` Namespace.

   >[!IMPORTANT]
   >
   >Wenden Sie sich an den Adobe Advertising-Support-Mitarbeiter Ihres Unternehmens, um zu bestätigen, dass alle Adobe Advertising-Konten Ihres Unternehmens, einschließlich [!DNL DSP] Konten oder Advertiser, [!DNL Search] Konten und [!DNL Creative] oder [!DNL DCO] -Konten - sind mit Ihrer Experience Cloud-Organisations-ID verknüpft.

1. Verwenden Sie die Adobe Experience Platform Privacy Service-API, um [Opt-out-of-Sale-Anfragen einreichen](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) Adobe Advertising im Namen der Verbraucher und Überprüfung des Status bestehender Anfragen.

   Im folgenden Anhang finden Sie ein Beispiel für eine Opt-out-Kaufanfrage.

   >[!NOTE]
   Wenn Ihr Unternehmen über mehrere Experience Cloud-Organisations-IDs verfügt, müssen Sie jeweils separate API-Anfragen senden. Sie können jedoch eine API-Anfrage an mehrere Adobe Advertising-Unterlösungen ([!DNL Search], [!DNL Creative], [!DNL DSP]und [!DNL DCO]), mit einem Konto pro Unterlösung.

Alle diese Schritte sind erforderlich, um Unterstützung von Adobe Advertising zu erhalten. Weitere Informationen zu diesen und anderen damit zusammenhängenden Aufgaben, die Sie mit der Adobe Experience Platform Privacy Service ausführen müssen, sowie dazu, wo Sie die benötigten Elemente finden können, finden Sie unter [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Abrufen von Berichten von Verbrauchern, die Opt-out-Kaufanfragen eingereicht haben

Adobe Advertising generiert monatliche Berichte über IDs, die Kunden für Opt-out-Kaufanfragen für das Konto gesendet haben. Jeder Bericht ist als tabulatorgetrennte Textdatei verfügbar, die in das GZIP-Format komprimiert ist. Die Daten konsolidieren Anforderungen, die mithilfe von CCPA-Opt-out-Kaufsegmenten erfasst wurden, die in Advertising DSP erstellt wurden, sowie alle über die Privacy Service-API durchgeführten Übermittlungen. In CCPA-Opt-out-Verkaufssegmenten erfasste Benutzer-IDs werden nach Segment und Advertiser identifiziert. Die Berichte werden am ersten eines jeden Monats für den Vormonat erstellt. Beispielsweise ist die monatliche Benutzerliste für Juni am 1. Juli verfügbar.

Sie können Links zu den monatlichen Berichten abrufen, die in den letzten drei Monaten erstellt wurden, entweder aus dem Advertising DSP oder mithilfe des Advertising DSP [!DNL Trafficking API]. Jeder Link ist sieben Tage lang gültig, wird jedoch jedes Mal aktualisiert, wenn ein Kunde versucht, ihn abzurufen.

### Methode 1: Abrufen von Opt-out-Berichten von Verbrauchern in Advertising DSP

1. Melden Sie sich im Advertising DSP unter dem Advertising-Konto an. [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [Berichte abrufen](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### Methode 2: Abrufen von Kundenabmeldeberichten mithilfe des Advertising-DSP [!DNL Trafficking API]

Diese Funktion steht Unternehmen zur Verfügung, die die [!DNL Trafficking API]. Die Dokumentation finden Sie in der [!DNL Trafficking API] für weitere Informationen.

Wenn Ihr Unternehmen die [!DNL Trafficking API] aber an weiteren Informationen interessiert ist, kontaktieren Sie bitte Ihre [!DNL Adobe] Account-Team.

## Anhang: Beispiel [!UICONTROL CCPA Opt-Out-of-Sale] Anfrage für Privacy Service-API-Benutzer

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

* `"namespace": "AdCloud"` gibt die `AdCloud` Cookie-Platzierung und der entsprechende Wert ist die Cookie-ID des Kunden, wie sie von abgerufen wird. `AdobePrivacy.js`
* `"include": ["AdCloud"]` weist darauf hin, dass die Anforderung für die Adobe Advertising gilt
