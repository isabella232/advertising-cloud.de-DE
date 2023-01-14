---
title: Verwenden der [!DNL Last Event Service] JavaScript-Bibliothek mit [!DNL Web SDK]
description: Erfahren Sie, wie Sie mit dem [!DNL Analytics] [!DNL visitorAPI] -Bibliothek [!DNL Experience Platform] [!DNL Web SDK] Bibliothek für Ihre [!DNL Analytics for Advertising] Implementierung.
feature: Integration with Adobe Analytics
exl-id: 96537244-1c5c-4d9a-a44e-ba7fcea9381d
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# Verwenden der [!DNL Last Event Service] JavaScript-Bibliothek mit Adobe Experience Platform [!DNL Web SDK]

*Werbetreibende mit nur einer Adobe Advertising-Adobe Analytics-Integration*

Wenn Ihr Unternehmen die veraltete Adobe Analytics verwendet `visitorAPI.js` -Bibliothek für die Datenerfassung können Sie optional zur Verwendung der [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) Bibliothek (`alloy.js`), die Ihnen die Interaktion mit den verschiedenen Experience Cloud-Diensten über die [!DNL Edge Network].

Die [!DNL Analytics for Advertising] [!DNL Last Event Service] Die JavaScript-Bibliothek zeichnet im Istzustand Durchsichts- und Clickthrough-Ereignisse auf und ordnet sie mithilfe einer zusätzlichen ID (`SDID`). Die [!DNL Web SDK] -Bibliothek bietet jedoch keine [!DNL stitch ID]. So verwenden Sie die [!DNL Web SDK] für [!DNL Analytics for Advertising], müssen Sie 1) der Variablen [!DNL Last Event Service] Tag, das Sie auf Ihren Webseiten verwenden, und 2) Ihre [!DNL Web SDK] `sendEvent` -Befehle entsprechend.

## Schritt 1: Bearbeiten Sie Ihre [!DNL Last Event Service] Tag zum Generieren eines `[!DNL StitchID]`

Im [!DNL Analytics for Advertising] [!DNL Last Event Service] Tag, das Sie auf Ihren Webseiten verwenden, fügen Sie Code hinzu, um die `[!DNL StitchID]` mit dem zufälligen ID-Generator, der in der Bibliothek gebündelt ist.

**Legacy-Tag:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          AdCloudEvent('IMS ORG Id');
</script>
```

**Neues Tag:**

```
<script>
     if("undefined" != typeof AdCloudEvent) 
          stitchId = AdCloudEvent('IMS ORG Id').generateRandomId();
</script>
```

## Schritt 2: Verwendung [!DNL Web SDK] , um [!DNL StitchID] als XDM-Daten für [!DNL Analytics]

Fügen Sie die folgende Eigenschaft in Ihre [!DNL Web SDK] `sendEvent` -Befehl zum Senden der [!DNL StitchID] nach [!DNL Experience Edge] as [!DNL Experience Data Model] (XDM)-Daten für [!DNL Analytics].<!-- The library will send the StitchID to [!DNL Experience Edge] as `[_adcloud.advertisingStitchID](https://github.com/adobe/xdm/blob/master/docs/reference/adobe/experience/adcloud/stitch.schema.md)`. --> [!DNL Analytics] verwendet den Wert als `SDID`.

**Eigenschaft zum Hinzufügen:**

```
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
```

**Beispiel:**

```
<script>
  alloy("sendEvent", {
    "xdm": {
      "commerce": {
        "order": {
                ………
        }
     },
     "_adcloud": {
       "advertisingStitchID": stitchId
     }
    }
  });
</script>
```

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising]](overview.md)
>* [JavaScript-Code für [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)

