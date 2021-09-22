---
title: Geräteübergreifende Lösungen
description: Erfahren Sie mehr über geräteübergreifende Funktionen.
feature: DSP Introduction
exl-id: 29f8ec41-35a6-4a29-a638-82a2929a8fe6
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '1111'
ht-degree: 0%

---

# Geräteübergreifende Lösungen

Advertising Cloud DSP-Integrationen mit [!DNL LiveRamp] und [!DNL Adobe Device Co-op] ermöglichen es Ihnen, Ihre Audience auf alle bekannten Geräte einer Person zu erweitern, nicht nur auf die Geräte, die Ihre Marke verfolgt hat. Die Integrationen bieten außerdem eine Frequenzlimitierung und Attributionsmessung für alle Geräte.

Wenn Sie ein unterstütztes benutzerbasiertes Gerätediagramm verwenden, können Sie:

* Passen Sie Zielgruppen kanalübergreifend und geräteübergreifend an, um Anzeigen für Personen und Haushalte und nicht für Geräte bereitzustellen.
* Ausgewogenheit und Exposition durch Verständnis und Begrenzung der Häufigkeit einzelner Personen.
* Teststrategien, die Zielgruppen über Kanäle oder Geräte hinweg verfügbar machen oder konvertieren.

## Vorteile der einzelnen Gerätediagramme

* [!DNL Adobe Device Co-op]:
   * Bietet einen Opt-in-Pool mit deterministischen und probabilistischen Daten teilnehmender Adobe-Advertiser
   * Bietet starke Cookie-ID-Verbindungen, die von Desktop- und mobilen Webbesuchern unterstützt werden
   * Umfasst Daten vorwiegend aus den Vereinigten Staaten und Kanada
   * Keine Nutzungsgebühren

* [!DNL LiveRamp] Gerätediagramm:
   * Stellt einen deterministischen Datenpool bereit, einschließlich Offline-Kundendaten
   * Gewährt eine gleichmäßige Abdeckung zwischen Cookie-IDs und Mobilgeräte-IDs
   * Umfasst Daten vorwiegend aus den Vereinigten Staaten
   * Ist frei für Frequenzlimitierung und Attributionsmessung
   * Preiswert von 0,35 USD für erweiterte Impressionen (Impressionen, die ausschließlich über das Gerätediagramm [!DNL LiveRamp] bereitgestellt werden, anstatt über Geräte, die in Zielgruppensegmenten gefunden werden)

      Der Preis wird auf Ihrer Kreditkarte angezeigt.

## Personenbasiertes Frequenzmanagement

Mit dem personenbasierten Frequenzmanagement können Sie Frequenzobergrenzen auf der Ebene der Person und nicht des Geräts für eine echte Steuerung der Medienbelichtung festlegen.

### Benutzerbasiertes Frequenzmanagement aktivieren

* **Kampagnen:** Wenn Sie eine neue Kampagne erstellen, können Sie eine  [!UICONTROL Cross-Device Level] Einstellung festlegen. Aktivieren Sie &quot;[!UICONTROL Same Device]&quot;-> &quot;[!UICONTROL People]&quot;und wählen Sie ein Gerätediagramm aus. Das angegebene Gerätediagramm wird sowohl für geräteübergreifendes Targeting auf Platzierungsebene als auch für benutzerbasiertes Frequenzmanagement auf Kampagnen-, Paket- und Platzierungsebene verwendet. Häufigkeitsbegrenzungen gelten für alle bekannten Geräte einer Person.

Weitere Informationen finden Sie unter [Kampagneneinstellungen](/help/dsp/campaign-management/campaigns/campaign-settings.md).

Nachdem Sie eine Kampagne gespeichert haben, können Sie die Einstellung [!UICONTROL Cross Device Level] nicht mehr ändern.

* **Pakete:**  Sie können optional zusätzliche Häufigkeitsbegrenzungen auf Paketebene festlegen. DSP respektiert die strengste Frequenzgrenze in der Kampagnenhierarchie.

* **Platzierungen:** Sie können optional zusätzliche Häufigkeitsbegrenzungen auf Platzierungsebene festlegen. DSP respektiert die strengste Frequenzgrenze in der Kampagnenhierarchie.

## Personenbasiertes Targeting

Mit personenbasiertem Targeting können Sie Kunden auf dem Desktop und auf Mobilgeräten finden.

### Aktivieren von personenbasiertem Targeting

* **Kampagnen:** Wenn Sie eine neue Kampagne erstellen, können Sie eine  [!UICONTROL Cross-Device Level] Einstellung festlegen. Aktivieren Sie &quot;[!UICONTROL Same Device]&quot;-> &quot;[!UICONTROL People]&quot;und wählen Sie ein Gerätediagramm aus. Das angegebene Gerätediagramm wird sowohl für geräteübergreifendes Targeting auf Platzierungsebene als auch für benutzerbasiertes Frequenzmanagement verwendet.

Weitere Informationen finden Sie unter [Kampagneneinstellungen](/help/dsp/campaign-management/campaigns/campaign-settings.md).

* **Platzierungen:** Wenn Sie Zielgruppenziele für eine Platzierung in einer Kampagne mit einem bestimmten Gerätediagramm auswählen, können Sie mit einer  [!UICONTROL Cross-Device Targeting] Option Ihr Targeting auf alle bekannten Geräte einer Person (gemäß dem in den Kampagneneinstellungen festgelegten Gerätediagramm) erweitern, selbst auf Geräte, die nicht in den angegebenen Segmenten enthalten sind.

### Einrichten von Berichten für personenbasiertes Targeting

Sie können die folgenden Metriken in benutzerdefinierte Berichte aufnehmen:

* **Erweiterte Impressionen:** (Im  [!UICONTROL Build Your Report] Abschnitt unter  [!UICONTROL Metrics] >  [!UICONTROL Std. Metrics]) Das Volumen der inkrementellen Impressionen, die durch Nutzung eines Gerätediagramms bereitgestellt werden (und nicht in den ursprünglichen Zielgruppensegmenten gefunden werden). Diese Metrik wird auch verwendet, um die anwendbaren Gebühren für die Verwendung eines Gerätediagramms eines Drittanbieters zu berechnen.

   Um die Kosten Ihrer erweiterten Impressionen während eines Zeitraums zu ermitteln, führen Sie einen benutzerspezifischen Bericht aus, der die Spalte [!UICONTROL Extended Impressions] enthält, und multiplizieren Sie dann die Gesamtanzahl der erweiterten Impressionen mit 0,00035 USD ($0,35/1000 Impressionen).

   Die aggregierten Kosten sind auch in der Spalte [!UICONTROL Billable Other Net Spend] enthalten (unter [!UICONTROL Metrics] > [!UICONTROL Spend]), obwohl diese Metrik auch andere Kampagnengebühren enthält, die Sie möglicherweise hinzugefügt haben.

* **Gerätediagramm:** (Im  [!UICONTROL Build Your Report] Abschnitt unter  [!UICONTROL Dimensions] >  [!UICONTROL Campaign]) Das ausgewählte Gerätediagramm für eine bestimmte Kampagne, ein bestimmtes Paket oder eine bestimmte Platzierung.

## Benutzerbasierte Attributionsmessung

*Advertiser mit Advertising Cloud-Konversions-Tracking*

Mit der benutzerbezogenen Attribution können Sie Konversionen zuordnen, die auf einem anderen Gerät stattgefunden haben als auf dem Gerät, auf dem die Medienbelichtung stattgefunden hat. Die personenbasierte Zuordnungsmessung ist für Advertiser, die Advertising Cloud-Konversionspixel auf ihren Sites implementiert haben, in DSP, Advertising Cloud Search und Advertising Cloud Creative verfügbar.

### Benutzerbasierte Attributionsmessung aktivieren

Wenden Sie sich an Ihren Kundenbetreuer, wenn Sie die geräteübergreifende Zuordnungsmessung aktivieren möchten. Für [!DNL Adobe Device Co-op]-Konten müssen Sie Ihren signierten [!DNL Adobe Device Co-op]-Vertrag und Ihr Experience Cloud [!DNL Organization ID] (ehemals [!DNL IMS org ID]) angeben.

So prüfen Sie, ob ein Advertiser-Konto für die Verwendung eines Gerätediagramms für die Attributionsmessung konfiguriert ist:

1. Klicken Sie im Hauptmenü auf **[!UICONTROL Settings]>[!UICONTROL Advertiser]**.
1. Halten Sie den Cursor über die Advertiser-Zeile und klicken Sie auf **[!UICONTROL Edit]**.
1. Überprüfen Sie im Abschnitt [!UICONTROL Integrations] der Advertiser-Einstellungen, ob die Einstellung [!UICONTROL Cross-Device Attribution] aktiv ist.

   Bei aktiven Integrationen wird das Gerätediagramm angezeigt.

### Einrichten von Konversionsberichten für die geräteübergreifende Konversionszuordnung

#### Konversionsberichtseinstellungen

Wenn ein Gerätediagramm für die Attributionsmessung aktiviert ist, enthält der [!UICONTROL Conversion]-Bericht eine [!UICONTROL Cross-Device Breakout]-Einstellung, mit der Sie bis zu drei separate Spalten für jede Konversionsmetrik einbeziehen können, darunter:

* &lt;>Konversion *> [!UICONTROL (tp)]: Umfasst die Gesamtkonversionen (Personen insgesamt), die sowohl Konversionen mit demselben Gerät als auch geräteübergreifende Konversionen enthalten (falls zutreffend).* Im Bericht wird &quot;[!UICONTROL (tp)]&quot;an den Konversionsmetriknamen, den Regeltyp und die Konversionstypen im Konversionspfad angehängt (z. B. &quot;Responses(le)(tl)(tp)).

* &lt;>Konversion *> [!UICONTROL (sd)]: (Optional) Umfasst nur Konversionen, für die im Konversionspfad nur ein einzelnes Gerät verfolgt wurde.* Im Bericht wird &quot;[!UICONTROL (sd)]&quot;an den Konversionsmetriknamen, den Regeltyp und die Konversionstypen im Konversionspfad angehängt (z. B. &quot;Responses(le)(tl)(sd)).

* &lt;>Konversion *> [!UICONTROL (xd)]: (Optional) Umfasst nur Konversionen, für die im Konversionspfad mehr als ein Gerät verfolgt wurde.* Im Bericht wird &quot;[!UICONTROL (xd)]&quot;an den Konversionsmetriknamen, den Regeltyp und die Konversionstypen im Konversionspfad angehängt (z. B. &quot;Responses(le)(tl)(xd)).

#### Interpretieren des Konversionsberichts

Wenn Sie den Prozentsatz der gesamten Konversionen, die geräteübergreifend ([!UICONTROL (xd)]/[!UICONTROL (tl)]) sind, von hoch zu niedrig sortieren, verstehen Sie, was zu überdurchschnittlichen geräteübergreifenden Konversionen führt. Sie können dies verwenden, um Ihre Kreativ- oder Targeting-Strategie zu informieren, um Messaging und Kanalinvestitionen auf das Benutzerverhalten abzugleichen.

* Pakete - Ermitteln Sie, welche Pakete die meisten Konversionen erzielen und welche einen hohen Prozentsatz geräteübergreifender Konversionen aufweisen. Auf diese Weise können Sie erkennen, wo die Ausgaben konzentriert werden.

* Platzierungen - Vergleichen Sie Platzierungsleistung und Attribution (z. B. kann eine mobile Webanzeige Konversionen auf dem Desktop fördern). Ohne Gerätediagramm für die Attribution können Sie die Auswirkungen einer mobilen Webplatzierung auf die Desktop-Konversionen verpassen oder sie kann begraben werden, wenn die Mehrheit Ihrer Benutzer auf dem Desktop und nicht im mobilen Internet konvertiert.

* Anzeigen - Erfahren Sie, welche Anzeigen zu höheren Konversionen führen und deren Wert und Wirkung über Webbrowser und Mobile-App-Umgebungen hinweg quantifizieren.

* Sites - Optimieren Sie Sites, anstatt Sites manuell vollständig auszuschließen. Wenn eine Website geräteübergreifende Konvertierungen durchführt, können Sie sehen, auf welchen Geräten dieses Verhalten auftritt.

* Angebote - Verbessern Sie die manuelle Optimierung, indem Sie überprüfen, welche Inventarangebote geräteübergreifende Konversionen liefern, und dann entscheiden, ob Sie Ihr Targeting erweitern sollten, um mehr Geräte und Kanäle in diese Angebote einzubeziehen.

>[!MORELIKETHIS]
>
>* [Berichtseinstellungen](/help/dsp/reports/report-settings.md)
>* [Kampagneneinstellungen](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
>* [Platzierungseinstellungen](/help/dsp/campaign-management/placements/placement-settings.md)

