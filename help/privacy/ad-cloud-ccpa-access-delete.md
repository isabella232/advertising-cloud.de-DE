---
title: 'Adobe Advertising Cloud-Unterstützung für den California Consumer Privacy Act : Unterstützung für Zugriff auf Kundendaten und Löschung'
description: Erfahren Sie mehr über die unterstützten Datenanforderungstypen, die erforderliche Einrichtung und Feldwerte sowie Beispiele für API-Zugriffsanfragen mit veralteten Produkt-IDs und zurückgegebenen Datenfeldern.
feature: CCPA
exl-id: 1330da6c-a944-4bb5-8539-488d97f56175
source-git-commit: 2e0395dc1e5aa52adc83c1aaea49793fd5555390
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Adobe Advertising Cloud-Unterstützung für den California Consumer Privacy Act: Unterstützung für Zugriff auf Kundendaten und Löschung

*Für Adobe Advertising Cloud Search, Adobe Advertising Cloud Creative, Adobe Advertising Cloud DSP und Adobe[!DNL Media Optimizer DCO]*

>[!IMPORTANT]
>
>Der Inhalt dieses Dokuments ist keine Rechtsberatung und soll keine Rechtsberatung ersetzen. Wenden Sie sich an Ihren Rechtsbeistand, um Ratschläge zum California Consumer Privacy Act zu erhalten.

Der California Consumer Privacy Act (CCPA) ist das neue kalifornische Datenschutzgesetz, das am 1. Januar 2020 in Kraft tritt. Der CCPA gibt in Kalifornien ansässigen Personen neue Rechte in Bezug auf ihre personenbezogenen Daten und verpflichtet bestimmte in Kalifornien tätige Unternehmen zur Einhaltung von Datenschutzvorschriften. Der CCPA bietet Verbrauchern das Recht, auf ihre personenbezogenen Daten zuzugreifen und sie zu löschen sowie das Recht, sich von bestimmten Aktivitäten abzumelden, die als &quot;Verkauf&quot;personenbezogener Daten an Dritte gelten.

Als Unternehmen legen Sie fest, welche personenbezogenen Daten Adobe Experience Cloud in Ihrem Namen verarbeitet und speichert.

Als Ihr Dienstleister unterstützt Adobe Advertising Cloud Ihr Unternehmen bei der Erfüllung seiner CCPA-Verpflichtungen, die für die Verwendung von Advertising Cloud-Produkten und -Diensten gelten, einschließlich der Verwaltung von Zugriffs- und Löschanfragen sowie der Verwaltung von Opt-out-Anfragen für den Verkauf personenbezogener Daten.

In diesem Dokument wird beschrieben, wie Advertising Cloud Search, Advertising Cloud Creative, Advertising Cloud DSP (Demand Side Platform) und [!DNL Media Optimizer DCO] - als Dienstleister - Unterstützung der Verbraucherrechte beim Zugang zu und bei der Löschung personenbezogener Daten mithilfe der Adobe [!DNL Experience Platform Privacy Service API] und [!DNL Privacy Service UI].

Informationen darüber, wie Advertising Cloud DSP das Verbraucherrecht unterstützt, sich vom Verkauf personenbezogener Daten abzumelden, finden Sie unter [Adobe Advertising Cloud-Unterstützung für den California Consumer Privacy Act: Opt-out-Support für Verbraucher](/help/privacy/ad-cloud-ccpa-opt-out-of-sale.md).

Weitere Informationen zu den Adobe Privacy Services für CCPA finden Sie im Abschnitt [Datenschutzzentrum für Adoben](https://www.adobe.com/privacy/ccpa.html).

## Unterstützte Datentypen für Advertising Cloud

Adobe Experience Platform bietet Unternehmen die Möglichkeit, die folgenden Aufgaben auszuführen:

* Greifen Sie auf die Daten auf Cookie-Ebene eines Kunden oder auf Geräte-ID-Ebene (für Anzeigen in mobilen Apps) in [!DNL Search], [!DNL Creative], [!DNL DSP]oder [!DNL DCO].
* Löschen Sie die in gespeicherten Daten auf Cookie-Ebene. [!DNL Search], [!DNL Creative], [!DNL DSP]oder [!DNL DCO] für Verbraucher, die einen Browser verwenden; oder löschen in gespeicherte Daten auf ID-Ebene [!DNL DSP] für Verbraucher, die Apps auf Mobilgeräten verwenden.
* Überprüfen Sie den Status einer oder aller vorhandenen Anforderungen.

## Erforderliche Einrichtung zum Senden von Anforderungen an Advertising Cloud

Um Anfragen zum Zugriff auf personenbezogene Daten von Verbrauchern und deren Löschung aus Advertising Cloud zu stellen, müssen Sie:

1. Stellen Sie eine JavaScript-Bibliothek bereit, um die Cookies Ihres Kunden abzurufen und zu entfernen. Dieselbe Bibliothek, `AdobePrivacy.js`, wird für alle Adobe Experience Cloud-Lösungen verwendet.

   >[!IMPORTANT]
   >
   >Für Anforderungen an einige Experience Cloud-Lösungen ist keine JavaScript-Bibliothek erforderlich, für Anfragen an Advertising Cloud ist dies jedoch erforderlich.

   Sie sollten die Bibliothek auf der Webseite bereitstellen, von der aus Ihre Kunden Zugriffs- und Löschanfragen senden können, z. B. das Datenschutzportal Ihres Unternehmens. Die Bibliothek hilft Ihnen beim Abrufen von Adobe-Cookies (Namespace-ID: `gsurferID`), damit Sie diese Identitäten als Teil von Zugriffs- und Löschanfragen über die [!DNL  Adobe Experience Platform Privacy Service API].

   Wenn der Kunde zum Löschen personenbezogener Daten auffordert, löscht die Bibliothek auch das Cookie des Kunden aus dem Browser des Kunden.

   >[!NOTE]
   >
   >Das Löschen personenbezogener Daten unterscheidet sich vom Opt-out-Verfahren, das die Zielgruppenbestimmung eines Endbenutzers mit Zielgruppensegmenten stoppt. Wenn ein Verbraucher jedoch die Löschung personenbezogener Daten aus [!DNL Creative], [!DNL DSP]oder [!DNL DCO]gesendet, sendet die Bibliothek auch eine Anfrage an Advertising Cloud, um den Kunden vom Segment-Targeting abzuwählen. Für Advertiser mit [!DNL Search], empfehlen wir Ihnen, Ihren Kunden einen Link zu [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse), der erklärt, wie Sie das Zielgruppensegment-Targeting deaktivieren können.

1. Identifizieren Sie Ihre Experience Cloud-Organisations-ID und stellen Sie sicher, dass sie mit Ihren Advertising Cloud-Konten verknüpft ist.

   Eine Experience Cloud-Organisations-ID ist eine 24-stellige alphanumerische Zeichenfolge, die an &quot;@AdobeOrg&quot;angehängt wird. Den meisten Experience Cloud-Kunden wurde eine Organisations-ID zugewiesen. Wenn Ihr Marketing-Team oder Ihr Systemadministrator Ihrer Adobe Ihre Organisations-ID nicht kennen oder nicht sicher ist, ob die ID bereitgestellt wurde, wenden Sie sich an die Kundenunterstützung von Adobe unter gdprsupport@adobe.com. Sie benötigen die Organisations-ID, um Anfragen über die `imsOrgID` Namespace.

   >[!IMPORTANT]
   >
   >Wenden Sie sich an den Advertising Cloud-Support-Mitarbeiter Ihres Unternehmens, um zu bestätigen, dass alle Advertising Cloud-Konten Ihres Unternehmens, einschließlich [!DNL DSP] Konten oder Advertiser, [!DNL Search] Konten und [!DNL Creative] oder [!DNL DCO] -Konten - sind mit Ihrer Experience Cloud-Organisations-ID verknüpft.

1. Verwenden Sie entweder [Adobe Experience Platform Privacy Service-API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) (für automatisierte Anfragen) oder [Privacy Service-Benutzeroberfläche](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html) (für Ad-hoc-Anfragen), um im Namen von Verbrauchern Anfragen zum Zugriff auf und zur Löschung personenbezogener Daten an Advertising Cloud zu stellen und den Status bestehender Anfragen zu überprüfen.

   Für Werbetreibende, die über eine mobile App verfügen, um mit Kunden zu interagieren und Kampagnen mit [!DNL DSP]müssen Sie zum Experience Cloud die datenschutzbereiten Mobile SDKs herunterladen. Die Mobile SDK ermöglichen es Unternehmen, Opt-out-Status-Flags festzulegen und die Geräte-ID des Kunden abzurufen (Namespace-ID: `deviceID`) und senden Sie Anfragen an die Privacy Service-API. Für Ihre Mobile App ist die SDK-Version 4.15.0 oder höher erforderlich.

   Wenn Sie eine Zugriffsanfrage an einen Verbraucher senden, gibt die Privacy Service-API die Informationen eines Verbrauchers basierend auf dem angegebenen Cookie oder der angegebenen Geräte-ID zurück, die Sie dann an den Verbraucher zurückgeben müssen.

   Wenn Sie eine Kundenlöschanfrage senden, werden die Cookie-ID oder Geräte-ID sowie alle mit dem Cookie verbundenen Kosten-, Klick- und Umsatzdaten vom Server gelöscht.

   >[!NOTE]
   Wenn Ihr Unternehmen über mehrere Experience Cloud-Organisations-IDs verfügt, müssen Sie jeweils separate API-Anfragen senden. Sie können jedoch eine API-Anfrage an mehrere Advertising Cloud-Unterlösungen richten ([!DNL Search], [!DNL Creative], [!DNL DSP]und [!DNL DCO]), mit einem Konto pro Unterlösung.

Alle diese Schritte sind erforderlich, um Unterstützung von Advertising Cloud zu erhalten. Weitere Informationen zu diesen und anderen damit zusammenhängenden Aufgaben, die Sie mit der Adobe Experience Platform Privacy Service ausführen müssen, sowie dazu, wo Sie die benötigten Elemente finden können, finden Sie unter [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Erforderliche Feldwerte in Advertising Cloud-JSON-Anforderungen

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*Ihre Experience Cloud-Organisations-ID*>

&quot;users&quot;:

* `"key":` &lt;*gewöhnlich den Namen des Kunden*>

* `"action":` entweder `**access**` oder `**delete**`

* `"user IDs":`

   * `"namespace": **411**` (was den Adcloud-Cookie-Bereich angibt)

   * `"value":` &lt;*der tatsächliche Cookie-ID-Wert des Kunden, der von abgerufen wurde`AdobePrivacy.js`*>

* `"include": **adCloud**` (das Adobe-Produkt, das für die Anfrage gilt)

* `"regulation": **ccpa**` (die Datenschutzverordnung, die für die Anfrage gilt)

## Beispiel einer von einem Kunden mit einer Advertising Cloud-Benutzer-ID gesendeten Anfrage, die von AdobePrivacy.js abgerufen wurde

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
    "regulation":"ccpa"
}
}
```

## Datenfelder, die für Zugriffsanfragen zurückgegeben werden

Im Folgenden finden Sie ein Beispiel für eine Antwort auf den Zugriff auf personenbezogene Daten für Advertising Cloud.

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
