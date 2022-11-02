---
title: Anhängen [!DNL Analytics for Advertising Cloud] Makros zu [!DNL Flashtalking] Anzeigen-Tags
description: Erfahren Sie, warum und wie Sie [!DNL Analytics for Advertising Cloud] Makros für Ihre [!DNL Flashtalking] Anzeigen-Tags
feature: Integration with Adobe Analytics
exl-id: 4b060668-723c-4cd2-b70e-409501ec67de
source-git-commit: ae516c1947d2b163ebd97dd05fb4e2870a1450d2
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# Anhängen [!DNL Analytics for Advertising Cloud] Makros zu [!DNL Flashtalking] Anzeigen-Tags

*Werbetreibende, die nur über eine Advertising Cloud-Adobe Analytics-Integration verfügen*

*Gilt nur für Advertising Cloud DSP*

Wenn Sie Anzeigen-Tags aus [!DNL Flashtalking] Fügen Sie für Ihre Advertising Cloud DSP-Anzeigen Analytics für Advertising Cloud-Parameter an Ihre Landingpage-URLs an. Der Parameterdatensatz `s_kwcid` und `ef_id` Abfragezeichenfolgenparameter in der Landingpage-URL, sodass Advertising Cloud Klickdaten für die Anzeigen an Adobe Analytics senden kann.

Verwenden Sie Makros für [!DNL Flashtalking] Anzeigen und Videoanzeigen für die folgenden Typen [!DNL Analytics for Advertising Cloud] Implementierungen:

* **Werbetreibende mit [!DNL Adobe] [!DNL Analytics for Advertising Cloud] Auf ihren Websites implementierter JavaScript-Code**: Der JavaScript-Code zeichnet bereits die `s_kwcid` und `ef_id` Abfragezeichenfolgenparameter. Durch die Verwendung von Makros wird das Tracking jedoch auch auf klickbasierte Konversionen erweitert, wenn Drittanbieter-Cookies nicht unterstützt werden. Es empfiehlt sich, die Makros in den folgenden Abschnitten zu Ihren Anzeigen-Tags hinzuzufügen, um zusätzliche Clickthrough-Daten zu erfassen, die nicht über den JavaScript-Code erfasst werden.

>[!NOTE]
>
>Der JavaScript-Code ist eine Lösung für Klick-Tracking, während Cookies weiterhin verfügbar sind. Sobald Cookies beendet sind, ist die Implementierung der folgenden Makros erforderlich.

* **Advertiser, deren Websites die [!DNL Analytics for Advertising Cloud] JavaScript-Code verwenden und stattdessen auf [!DNL Analytics] Serverseitige Weiterleitung nur für Clickthrough-Daten** (ohne Durchsichtsdaten): Die folgenden Makros sind erforderlich, um Klick-Aktivitäten vor Ort über Anzeigen zu melden, die Sie über Advertising Cloud kaufen.

## Anzeigen-Tags

Innerhalb der [!DNL Flashtalking] Fügen Sie das folgende Makro an das Ende der Clickthrough-URL in der `Clicktag` -Feld:

```html
?[ftqs:[AdobeAMO]]
```

Beispiel:  `https://www.adobe.com/products/photoshop?[ftqs:[AdobeAMO]]`

![Beispiel für [!DNL Flashtalking] Adtag-Einstellungen](/help/integrations/assets/macro-flashtalking-display-ad.png)

## Videoanzeigen-Tags

Innerhalb der [!DNL Flashtalking] Fügen Sie das folgende Makro an das Ende der Clickthrough-URL in der `Clicktag` -Feld:

```html
?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]
```

Beispiel:  `https://www.adobe.com/products/photoshop?[%EL:param['AdobeAMO']%]&s_kwcid=[%EL:param['s_kwcid']%]`

![Beispiel für [!DNL Flashtalking] Adtag-Einstellungen](/help/integrations/assets/macro-flashtalking-video-ad.png)

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Von verwendete Advertising Cloud IDs [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Anhängen [!DNL Analytics for Advertising Cloud] Makros zu [!DNL Google Campaign Manager 360] Anzeigen-Tags](/help/integrations/analytics/macros-google-campaign-manager.md)

