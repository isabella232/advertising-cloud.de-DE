---
title: Adobe Advertising-Unterstützung für die Datenschutz-Grundverordnung
description: Erfahren Sie mehr über die unterstützten Datenanforderungstypen, die erforderliche Einrichtung und Feldwerte sowie Beispiele für API-Zugriffsanfragen mit alten Produkt-IDs und zurückgegebenen Datenfeldern
feature: GDPR
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '1034'
ht-degree: 0%

---

# Adobe Advertising-Unterstützung für die Datenschutz-Grundverordnung

*Für [!DNL Adobe Advertising Search]; Adobe Advertising DSP Adobe Advertising Creative; und Adobe Advertising DCO*

>[!IMPORTANT]
>
>Der Inhalt dieses Dokuments ist keine Rechtsberatung und soll keine Rechtsberatung ersetzen. Wenden Sie sich an Ihren Rechtsbeistand, um Ratschläge zur Datenschutz-Grundverordnung zu erhalten.

Die Datenschutz-Grundverordnung (DSGVO), ein Gesetz, das am 25. Mai 2018 in Kraft trat, gibt allen Personen (betroffenen Personen) innerhalb der Grenzen der Europäischen Union (EU) die Kontrolle über ihre personenbezogenen Daten und vereinfacht das Regelungsumfeld für internationale Geschäfte. Dieses Gesetz gilt für alle Unternehmen (Datenverantwortliche), die zum Zeitpunkt der Verarbeitung ihrer personenbezogenen Daten Waren oder Dienstleistungen anbieten, das Verhalten von Personen überwachen oder personenbezogene Daten von Personen innerhalb der Grenzen der EU erfassen, unabhängig vom Geschäftsort des Datenverantwortlichen.

Adobe Experience Cloud fungiert als Datenverarbeiter für alle personenbezogenen Daten, die es im Namen seiner Kunden empfängt und speichert. Als Datenverantwortlicher legen Sie fest, welche personenbezogenen Daten Adobe Experience Cloud in Ihrem Namen verarbeitet und speichert.

In diesem Dokument wird beschrieben, wie [!DNL Advertising Search]; Werbegestaltung; DSP (Demand Side Platform) und [!DNL Advertising DCO] Unterstützung der DSGVO-Datenzugriffs- und -Löschungsrechte der betroffenen Personen mithilfe der Adobe Experience Platform Privacy Service-API und der Privacy Service-Benutzeroberfläche.

Weitere Informationen darüber, was die DSGVO für Ihr Unternehmen bedeutet, finden Sie unter [DSGVO und Ihr Unternehmen](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Unterstützte Datenanforderungstypen für Adobe Advertising

Adobe Experience Platform bietet Unternehmen die Möglichkeit, die folgenden Aufgaben auszuführen:

* Greifen Sie auf die Daten auf Cookie-Ebene oder Daten auf Geräte-ID-Ebene (für Anzeigen in mobilen Apps) eines Datensubjekts innerhalb von zu [!DNL Search], [!DNL Creative], [!DNL DSP]oder [!DNL DCO].
* Löschen Sie die in gespeicherten Daten auf Cookie-Ebene. [!DNL Search], [!DNL Creative], [!DNL DSP]oder [!DNL DCO] bei Datensubjekten, die einen Browser verwenden; oder löschen in gespeicherte Daten auf ID-Ebene [!DNL DSP] für Datensubjekte, die Apps auf Mobilgeräten verwenden.
* Überprüfen Sie den Status einer oder aller vorhandenen Anforderungen.

## Erforderliche Einrichtung zum Senden von Anfragen für Adobe Advertising

Um Anfragen zum Zugreifen auf und Löschen von Daten für Adobe Advertising zu stellen, müssen Sie:

1. Stellen Sie eine JavaScript-Bibliothek bereit, um Cookies Ihrer Datensubjekte abzurufen und zu entfernen. Dieselbe Bibliothek, `AdobePrivacy.js`, wird für alle Adobe Experience Cloud-Lösungen verwendet.

   >[!IMPORTANT]
   >
   >Für Anforderungen an einige Adobe Experience Cloud-Lösungen ist keine JavaScript-Bibliothek erforderlich, für Anfragen an Adobe Advertising ist dies jedoch erforderlich.

   Sie sollten die Bibliothek auf der Webseite bereitstellen, von der aus die betroffenen Personen Zugriffs- und Löschanfragen senden können, z. B. das Datenschutzportal Ihres Unternehmens. Die Bibliothek hilft Ihnen beim Abrufen von Adobe-Cookies (Namespace-ID: `gsurferID`), damit Sie diese Identitäten als Teil von Zugriffs- und Löschanfragen über die Adobe Experience Platform Privacy Service-API senden können.

   Wenn die betroffene Person die Löschung personenbezogener Daten verlangt, löscht die Bibliothek auch das Cookie der betroffenen Person aus dem Browser der betroffenen Person.

   >[!NOTE]
   >
   >Das Löschen personenbezogener Daten unterscheidet sich vom Opt-out-Verfahren, das die Zielgruppenbestimmung eines Endbenutzers mit Zielgruppensegmenten stoppt. Wenn eine betroffene Person jedoch die Löschung personenbezogener Daten aus [!DNL Creative], [!DNL DSP]oder [!DNL DCO]gesendet, sendet die Bibliothek auch eine Anfrage an Adobe Advertising, um die betroffene Person vom Segment-Targeting abzuwählen. Für Advertiser mit [!DNL Search], empfehlen wir, den betroffenen Personen einen Link zu [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html), der erklärt, wie Sie das Zielgruppensegment-Targeting deaktivieren können.

1. Identifizieren Sie Ihre Experience Cloud-Organisations-ID und stellen Sie sicher, dass sie mit Ihren Adobe Advertising-Konten verknüpft ist.

   Eine Experience Cloud-Organisations-ID ist eine 24-stellige alphanumerische Zeichenfolge, die an &quot;@AdobeOrg&quot;angehängt wird. Den meisten Experience Cloud-Kunden wurde eine Organisations-ID zugewiesen. Wenn Ihr Marketing-Team oder Ihr Systemadministrator Ihrer Adobe Ihre Organisations-ID nicht kennen oder nicht sicher ist, ob die ID bereitgestellt wurde, wenden Sie sich an die Kundenunterstützung von Adobe unter gdprsupport@adobe.com. Sie benötigen die Organisations-ID, um Anfragen über die `imsOrgID` Namespace.

   >[!IMPORTANT]
   >
   >Wenden Sie sich an den Adobe Advertising-Support-Mitarbeiter Ihres Unternehmens, um zu bestätigen, dass alle Adobe Advertising-Konten Ihres Unternehmens, einschließlich [!DNL DSP] Konten oder Advertiser, [!DNL Search] Konten und [!DNL Creative] oder [!DNL DCO] -Konten - sind mit Ihrer Experience Cloud-Organisations-ID verknüpft.

1. Verwenden Sie entweder [Adobe Experience Platform Privacy Service-API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (für automatisierte Anfragen) oder [Privacy Service-Benutzeroberfläche](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) (für Ad-hoc-Anfragen), um Zugriffs- und Löschanfragen an Adobe Advertising im Namen der betroffenen Personen zu senden und den Status bestehender Anfragen zu überprüfen.

   Für Advertiser, die über eine mobile App verfügen, um mit Datensubjekten zu interagieren und Kampagnen mit DSP zu starten, müssen Sie die datenschutzbereiten Mobile SDKs zum Experience Cloud herunterladen. Die Mobile SDK ermöglichen es Datenverantwortlichen, Opt-out-Status-Flags festzulegen und die Geräte-ID des Datensubjekts abzurufen (Namespace-ID: deviceID) und Senden von Anfragen an die Privacy Service-API. Für Ihre Mobile App ist die SDK-Version 4.15.0 oder höher erforderlich.

   Wenn Sie die Zugriffsanfrage eines Datensubjekts senden, gibt die Privacy Service-API die Informationen des Datensubjekts basierend auf dem angegebenen Cookie oder der angegebenen Geräte-ID zurück, die Sie dann an das Datensubjekt zurückgeben müssen.

   Wenn Sie die Löschanfrage eines Datensubjekts senden, werden die Cookie-ID oder Geräte-ID sowie alle mit dem Cookie verbundenen Kosten-, Klick- und Umsatzdaten vom Server gelöscht.

   >[!NOTE]
   Wenn Ihr Unternehmen über mehrere Experience Cloud-Organisations-IDs verfügt, müssen Sie für jede Datei separate API-Anfragen senden. Sie können jedoch eine API-Anfrage an mehrere Adobe Advertising-Unterlösungen ([!DNL Search], [!DNL Creative], [!DNL DSP]und [!DNL DCO]), mit einem Konto pro Unterlösung.

Alle diese Schritte sind für die Adobe Advertising erforderlich. Weitere Informationen zu diesen und anderen damit zusammenhängenden Aufgaben, die Sie mit der Adobe Experience Platform Privacy Service ausführen müssen, sowie dazu, wo Sie die benötigten Elemente finden können, finden Sie unter [www.adobe.io/apis/cloudplatform/gdpr.html](https://www.adobe.io/apis/experienceplatform/gdpr.html).

## Erforderliche Feldwerte in Adobe Advertising JSON-Anforderungen

&quot;&quot;company context&quot;:

* `"namespace": **imsOrgID**`
* `"value":` &lt;*Ihren IMS-Organisations-ID-Wert*>

`"users":`

* `"key":` &lt;*gewöhnlich den Namen des Datensubjekts*>

* `"action":` entweder `**access**` oder `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (die angibt, dass [!DNL adcloud] Cookie-Leerzeichen)

   * `"value":` &lt;*der Cookie-ID-Wert des Datensubjekts, der von abgerufen wurde`AdobePrivacy.js`*>

* `"include": **adCloud**` (das Adobe-Produkt, das für die Anfrage gilt)

* `"regulation": **gdpr**` (die Datenschutzverordnung, die für die Anfrage gilt)

## Beispiel einer Anfrage, die von einer betroffenen Person unter Verwendung einer Adobe Advertising User ID gesendet wurde, abgerufen von `AdobePrivacy.js`

```
{
"companyContexts":[
      {
         "namespace":"imsOrgID",
         "value":"5AB13068374019BC@AdobeOrg"
      }
   ],
   "users": [
{
 "key": "John Doe",
 "action":["access"],
  "userIDs":[
      {
         "namespace":"411",
         "value":"Wqersioejr-wdg",
         "type":"namespaceId",
         "deletedClientSide":false
      }
   ]
}
],
"include":[
      "adCloud"
   ],
    "regulation":"gdpr"
}
}
```

## Datenfelder, die für Zugriffsanfragen zurückgegeben werden

Im Folgenden finden Sie ein Beispiel für eine Zugriffsantwort für Adobe Advertising.

```
{
    "jobId":"12345AD43E",
    "action":"access",
    "product":"adCloud",
    "status":"complete",
    "results":{
        "userIDs":[
            {
                "namespace":"411",
                "userID":" Wqersioejr-wdg "
            }
        ],
        "receiptData":{
            "impressionCount":"100",
            "clickCount":5,
            "geo":[
                "United States of America",
                "San Francisco CA"
            ],
            "profile":[
                {
                    "pixelid":"111",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                },
                {
                    "pixelid":"123",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                }
            ],
            "matchingSegments":[
                {
                    "segmentName":"AP4 - Art/Culture - In-Market",
                    "segmentID":"kV1mPa2aqPNWKSNtf325",
                    "serviceProvider":"Adobe"
                },
                {
                    "segmentName":"EMEA - UK - Health Food Buyers",
                    "segmentID":"eP2oJ2UPsfsDVDhvlGewx",
                    "serviceProvider":"BlueKai"
                }
            ]
        }
    }
}
```
