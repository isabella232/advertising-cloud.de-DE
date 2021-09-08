---
title: Adobe Advertising Cloud-Unterstützung für die Datenschutz-Grundverordnung
description: Erfahren Sie mehr über die unterstützten Datenanforderungstypen, die erforderliche Einrichtung und Feldwerte sowie Beispiele für API-Zugriffsanfragen mit alten Produkt-IDs und zurückgegebenen Datenfeldern
feature: GDPR
exl-id: 304d88d0-d63d-4b32-8d4d-c61ba2409adc
source-git-commit: 56ac178bf10d8c934297521ca3075783e1bc2c36
workflow-type: tm+mt
source-wordcount: '1058'
ht-degree: 0%

---

# Adobe Advertising Cloud-Unterstützung für die Datenschutz-Grundverordnung

*Für Adobe Advertising Cloud Search, Adobe Advertising Cloud Creative, Adobe Advertising Cloud DSP und Adobe Media Optimizer DCO*

>[!IMPORTANT]
>
>Der Inhalt dieses Dokuments ist keine Rechtsberatung und soll keine Rechtsberatung ersetzen. Wenden Sie sich an Ihren Rechtsbeistand, um Ratschläge zur Datenschutz-Grundverordnung zu erhalten.

Die Datenschutz-Grundverordnung (DSGVO), ein Gesetz, das am 25. Mai 2018 in Kraft trat, gibt allen Personen (betroffenen Personen) innerhalb der Grenzen der Europäischen Union (EU) die Kontrolle über ihre personenbezogenen Daten und vereinfacht das Regelungsumfeld für internationale Geschäfte. Dieses Gesetz gilt für alle Unternehmen (Datenverantwortliche), die zum Zeitpunkt der Verarbeitung ihrer personenbezogenen Daten Waren oder Dienstleistungen anbieten, das Verhalten von Personen überwachen oder personenbezogene Daten von Personen innerhalb der Grenzen der EU erfassen, unabhängig vom Geschäftsort des Datenverantwortlichen.

Adobe Experience Cloud fungiert als Datenverarbeiter für alle personenbezogenen Daten, die es im Namen seiner Kunden empfängt und speichert. Als Datenverantwortlicher legen Sie fest, welche personenbezogenen Daten Adobe Experience Cloud in Ihrem Namen verarbeitet und speichert.

In diesem Dokument wird beschrieben, wie Advertising Cloud Search, Advertising Cloud Creative, Advertising Cloud DSP (Demand Side Platform) und Media Optimizer DCO die DSGVO-Datenzugriffs- und -Löschungsrechte der betroffenen Personen mithilfe der Adobe Experience Platform Privacy Service-API und der Privacy Service-Benutzeroberfläche unterstützen.

Weitere Informationen dazu, was die DSGVO für Ihr Unternehmen bedeutet, finden Sie unter [DSGVO und Ihr Unternehmen](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Unterstützte Datentypen für Advertising Cloud

Adobe Experience Platform bietet Unternehmen die Möglichkeit, die folgenden Aufgaben auszuführen:

* Greifen Sie auf Daten auf Cookie-Ebene oder Daten auf Geräte-ID-Ebene (für Anzeigen in mobilen Apps) innerhalb von [!DNL Search], [!DNL Creative], [!DNL DSP] oder [!DNL DCO] zu.
* Löschen Sie Daten auf Cookie-Ebene, die in [!DNL Search], [!DNL Creative], [!DNL DSP] oder [!DNL DCO] für Datensubjekte gespeichert sind, die einen Browser verwenden. oder löschen Sie in [!DNL DSP] gespeicherte Daten auf ID-Ebene für Datensubjekte, die Apps auf Mobilgeräten verwenden.
* Überprüfen Sie den Status einer oder aller vorhandenen Anforderungen.

## Erforderliche Einrichtung zum Senden von Anforderungen an Advertising Cloud

Um Anfragen zum Zugreifen auf und Löschen von Daten für Advertising Cloud zu stellen, müssen Sie:

1. Stellen Sie eine JavaScript-Bibliothek bereit, um Cookies Ihrer Datensubjekte abzurufen und zu entfernen. Dieselbe Bibliothek `AdobePrivacy.js` wird für alle Adobe Experience Cloud-Lösungen verwendet.

   >[!IMPORTANT]
   >
   >Für Anforderungen an einige Adobe Experience Cloud-Lösungen ist keine JavaScript-Bibliothek erforderlich, für Anfragen an Advertising Cloud ist dies jedoch erforderlich.

   Sie sollten die Bibliothek auf der Webseite bereitstellen, von der aus die betroffenen Personen Zugriffs- und Löschanfragen senden können, z. B. das Datenschutzportal Ihres Unternehmens. Die Bibliothek hilft Ihnen beim Abrufen von Adobe-Cookies (Namespace-ID: `gsurferID`), damit Sie diese Identitäten im Rahmen von Zugriffs- und Löschanfragen über die Adobe Experience Platform Privacy Service-API senden können.

   Wenn die betroffene Person die Löschung personenbezogener Daten verlangt, löscht die Bibliothek auch das Cookie der betroffenen Person aus dem Browser der betroffenen Person.

   >[!NOTE]
   >
   >Das Löschen personenbezogener Daten unterscheidet sich vom Opt-out-Verfahren, das die Zielgruppenbestimmung eines Endbenutzers mit Zielgruppensegmenten stoppt. Wenn ein Datensubjekt jedoch fragt, ob er personenbezogene Daten aus [!DNL Creative], [!DNL DSP] oder [!DNL DCO] löschen möchte, sendet die Bibliothek auch eine Anfrage an Advertising Cloud, die betroffene Person vom Segment-Targeting abzumelden. Für Advertiser mit [!DNL Search] empfehlen wir, den betroffenen Personen einen Link zu [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html) bereitzustellen, der erklärt, wie sie sich vom Zielgruppensegment-Targeting abmelden können.

1. Identifizieren Sie Ihre IMS-Organisations-ID und stellen Sie sicher, dass sie mit Ihren Advertising Cloud-Konten verknüpft ist.

   Eine IMS-Organisations-ID ist eine 24-stellige alphanumerische Zeichenfolge, die an @AdobeOrg angehängt wird. Den meisten Adobe Experience Cloud-Kunden wurde eine IMS-Organisations-ID zugewiesen. Wenn Ihr Marketing-Team oder der Systemadministrator Ihrer Adobe die IMS-Organisations-ID Ihres Unternehmens nicht kennen oder nicht sicher ist, ob die Kennung bereitgestellt wurde, wenden Sie sich an die Kundenunterstützung von Adobe unter gdprsupport@adobe.com. Sie benötigen die IMS-Organisations-ID, um Anfragen an die Datenschutz-API zu senden.

   >[!IMPORTANT]
   >
   >Wenden Sie sich an den Advertising Cloud-Support-Mitarbeiter Ihres Unternehmens, um zu bestätigen, dass alle Advertising Cloud-Konten Ihres Unternehmens - einschließlich [!DNL DSP]-Konten oder -Advertiser, [!DNL Search]-Konten und [!DNL Creative]- oder [!DNL DCO]-Konten - mit Ihrer IMS-Organisations-ID verknüpft sind.

1. Verwenden Sie entweder die [Adobe Experience Platform Privacy Service-API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (für automatisierte Anfragen) oder die [Privacy Service-Benutzeroberfläche](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) (für Ad-hoc-Anfragen), um Zugriffs- und Löschanfragen an Advertising Cloud im Namen der betroffenen Personen zu senden und den Status vorhandener Anfragen zu überprüfen.

   Für Advertiser, die über eine mobile App verfügen, um mit Datensubjekten zu interagieren und Kampagnen mit der DSP zu starten, müssen Sie die datenschutzbereiten Mobile SDKs zum Experience Cloud herunterladen. Die Mobile SDK ermöglichen es Datenverantwortlichen, Opt-out-Status-Flags festzulegen und die Geräte-ID des Datensubjekts abzurufen (Namespace-ID: deviceID) und Senden von Anfragen an die Privacy Service-API. Für Ihre Mobile App ist die SDK-Version 4.15.0 oder höher erforderlich.

   Wenn Sie die Zugriffsanfrage eines Datensubjekts senden, gibt die Privacy Service-API die Informationen des Datensubjekts basierend auf dem angegebenen Cookie oder der angegebenen Geräte-ID zurück, die Sie dann an das Datensubjekt zurückgeben müssen.

   Wenn Sie die Löschanfrage eines Datensubjekts senden, werden die Cookie-ID oder Geräte-ID sowie alle mit dem Cookie verbundenen Kosten-, Klick- und Umsatzdaten vom Server gelöscht.

   >[!NOTE]
   Wenn Ihr Unternehmen über mehrere Adobe Experience Cloud Identity Management Service-Organisations-IDs (IMS-Organisations-IDs) verfügt, müssen Sie für jede einzelne API separate Anfragen senden. Sie können jedoch eine API-Anfrage an mehrere Advertising Cloud-Unterlösungen ([!DNL Search], [!DNL Creative], [!DNL DSP] und [!DNL DCO]) mit einem Konto pro Unterlösung richten.

Alle diese Schritte sind für Advertising Cloud erforderlich. Weitere Informationen zu diesen und anderen zugehörigen Aufgaben, die Sie mit der Adobe Experience Platform Privacy Service ausführen müssen, sowie dazu, wo Sie die benötigten Elemente finden können, finden Sie unter [www.adobe.io/apis/cloudplatform/gdpr.html](https://www.adobe.io/apis/experienceplatform/gdpr.html).

## Erforderliche Feldwerte in Advertising Cloud-JSON-Anforderungen

&quot;&quot;company context&quot;:

* `"namespace": **imsOrgID**`
* `"value":` &lt;>IMS-Organisations-ID-Wert *>*

`"users":`

* `"key":` &lt;>gewöhnlich den Namen des Datensubjekts *>*

* `"action":` entweder  `**access**` oder  `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (was den  [!DNL adcloud] Cookie-Bereich angibt)

   * `"value":` &lt;>der Cookie-ID-Wert des Datensubjekts, der von  `AdobePrivacy.js`*> abgerufen wurde.*

* `"include": **adCloud**` (das Adobe-Produkt, das für die Anfrage gilt)

* `"regulation": **gdpr**` (die Datenschutzverordnung, die für die Anfrage gilt)

## Beispiel einer Anfrage, die von einer betroffenen Person unter Verwendung einer Advertising Cloud-Benutzer-ID gesendet wurde, abgerufen von `AdobePrivacy.js`

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

Im Folgenden finden Sie ein Beispiel für eine Zugriffsantwort für Advertising Cloud.

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
