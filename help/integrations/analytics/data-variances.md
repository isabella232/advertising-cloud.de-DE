---
title: Erwartete Datenabweichungen zwischen [!DNL Analytics] und Advertising Cloud
description: Erwartete Datenabweichungen zwischen [!DNL Analytics] und Advertising Cloud
feature: Integration with Adobe Analytics
exl-id: 34685e04-d4f9-4e27-b83e-b56164244b2b
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '3285'
ht-degree: 0%

---

# Erwartete Datenabweichungen zwischen [!DNL Analytics] und Advertising Cloud

*Werbetreibende, die nur über eine Advertising Cloud-Adobe Analytics-Integration verfügen*

Advertiser mit der Integration [!DNL Analytics for Advertising Cloud] <!-- (A4AdC) --> verfolgen bezahlte Werbung über Advertising Cloud und Adobe Analytics. Wenn Sie Medien, Kampagnen und Kanäle über mehrere Systeme verfolgen, stimmen nur selten dieselben Datensätze aus verschiedenen Systemen vollständig überein. In diesem Dokument wird erläutert, wie Sie erwarten sollten, dass Daten für Medien, die über Advertising Cloud gehandelt werden, mit Daten in den verschiedenen Systemen verglichen werden, in denen die Medien innerhalb von [!DNL Analytics] verfolgt werden.

>[!NOTE]
>
>Dieses Dokument konzentriert sich auf Advertising Cloud und Analytics, aber viele der Schlüsselpunkte können auch auf andere Tracking-Lösungen übertragen werden.

## Unterschiede bei der Zuordnung in ähnlichen Berichten

### Potenziell unterschiedliche Lookback-Fenster und Attributionsmodelle

Die Integration von [!DNL Analytics for Advertising Cloud] verwendet zwei Variablen (eVars oder rVars \[reservierte eVars]\) zum Erfassen der [EF ID und AMO ID](ids.md). Diese Variablen werden mit einem einzelnen Lookback-Fenster (dem Zeitpunkt, innerhalb dessen Clickthroughs und Durchsichten zugeordnet werden) und einem Attributionsmodell konfiguriert. Sofern nicht anders angegeben, sind die Variablen so konfiguriert, dass sie mit dem standardmäßigen Klick-Lookback-Fenster und Attributionsmodell auf Advertiser-Ebene in Advertising Cloud übereinstimmen.

Lookback-Fenster und Attributionsmodelle können jedoch sowohl in Analytics (über die eVars) als auch in Advertising Cloud konfiguriert werden. Außerdem ist das Attributionsmodell in Advertising Cloud nicht nur auf Advertiser-Ebene (zur Angebotsoptimierung), sondern auch innerhalb einzelner Datenansichten und Berichte konfigurierbar (nur zu Berichtszwecken). Ein Unternehmen könnte beispielsweise das Gleichheitsverteilungsattributionsmodell zur Optimierung verwenden, aber die Letztkontakt-Attribution für Berichte in Advertising Cloud DSP oder [!DNL Search] verwenden. Wenn Sie Attributionsmodelle ändern, ändert sich die Anzahl der zugeordneten Konversionen.

Wenn ein Reporting-Lookback-Fenster oder Attributionsmodell in einem Produkt und nicht im anderen geändert wird, zeigen dieselben Berichte aus jedem System unterschiedliche Daten an:

* **Beispiel für Diskrepanzen, die durch verschiedene Lookback-Fenster verursacht werden:**

   Angenommen, Advertising Cloud verfügt über ein 60-tägiges Klick-Lookback-Fenster und [!DNL Analytics] über ein 30-tägiges Lookback-Fenster. Angenommen, ein Benutzer besucht die Site über eine von Advertising Cloud getrackte Anzeige, verlässt die Site und kehrt dann an Tag 45 zurück und konvertiert sie. Advertising Cloud ordnet die Konversion dem ersten Besuch zu, da die Konversion innerhalb des 60-Tage-Lookback-Fensters stattgefunden hat. [!DNL Analytics]kann die Konversion jedoch nicht dem ersten Besuch zuordnen, da die Konversion erfolgte, nachdem das 30-Tage-Lookback-Fenster abgelaufen war. In diesem Beispiel würde Advertising Cloud eine höhere Anzahl von Konversionen melden als [!DNL Analytics].

   ![Beispiel einer Konvertierung, die in Advertising Cloud zugewiesen wurde, aber nicht  [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **Beispiel für Diskrepanzen, die durch verschiedene Attributionsmodelle verursacht werden:**

   Nehmen wir an, ein Benutzer interagiert mit drei verschiedenen Advertising Cloud-Anzeigen, bevor er konvertiert, wobei der Umsatz der Konversionstyp ist. Wenn ein Advertising Cloud-Bericht ein Gleichheitsverteilungsmodell für die Attribution verwendet, wird der Umsatz gleichmäßig über alle Anzeigen verteilt. Wenn [!DNL Analytics] jedoch das Attributionsmodell des letzten Kontakts verwendet, ordnet es den Umsatz der letzten Anzeige zu. Im folgenden Beispiel ordnet Advertising Cloud jeder der drei Anzeigen einen Umsatz von 10 USD des Umsatzes von 30 USD zu, während [!DNL Analytics] alle 30 USD Umsatz der letzten Anzeige zuordnet, die der Benutzer gesehen hat. Wenn Sie Berichte aus Advertising Cloud und [!DNL Analytics] vergleichen, können Sie die Auswirkungen der unterschiedlichen Attribution erwarten.

   ![Verschiedene Umsätze, die Advertising Cloud zugeordnet werden und  [!DNL Analytics] auf unterschiedlichen Attributionsmodellen basieren](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>Es empfiehlt sich, in Advertising Cloud und [!DNL Analytics] dieselben Lookback-Fenster und Attributionsmodelle zu verwenden. Arbeiten Sie bei Bedarf mit Ihrem Adobe Account Manager zusammen, um die aktuellen Einstellungen zu ermitteln und die Konfigurationen zu synchronisieren.

Diese Konzepte gelten für alle anderen Kanäle wie Kanäle, die unterschiedliche Lookback-Fenster oder Attributionsmodelle verwenden.

#### Verschiedene Lookback-Fenster für das Durchsichts-Tracking {#impression-lookback}

In Advertising Cloud basiert die Attribution auf Klicks und Impressionen und Sie können verschiedene Lookback-Fenster für Klicks und Impressionen konfigurieren. In [!DNL Analytics] basiert die Attribution jedoch auf Clickthroughs und Durchsichten und Sie haben nicht die Möglichkeit, verschiedene Attributionsfenster für Clickthroughs und Durchsichten festzulegen. Tracking für jeden beginnt beim ersten Site-Besuch. Eine Impression kann am selben Tag oder mehreren Tagen vor dem Eintreten einer Durchsicht auftreten. Dies kann sich auf den Beginn des Attributionsfensters in den einzelnen Systemen auswirken.

In der Regel treten die meisten Durchsichtskonversionen schnell genug auf, sodass beide Systeme Gutschriften zuweisen. Einige Konversionen können jedoch außerhalb des Advertising Cloud-Impression-Lookback-Fensters, aber innerhalb des [!DNL Analytics]-Lookback-Fensters auftreten. diese Konversionen werden der Durchsicht in [!DNL Analytics] zugeordnet, nicht aber der Impression in Advertising Cloud.

Im folgenden Beispiel wird angenommen, dass einem Besucher an Tag 1 eine Anzeige bereitgestellt wurde, an Tag 2 einen Durchsichtsbesuch (d. h. einen Besuch der Landingpage der Anzeige, ohne zuvor auf die Anzeige zu klicken) durchgeführt und an Tag 45 konvertiert wurde. In diesem Fall verfolgt Advertising Cloud den Benutzer von den Tagen 1 bis 14 (mit einem 14-tägigen Lookback), [!DNL Analytics] verfolgt den Benutzer von den Tagen 2 bis 61 (mit einem 60-tägigen Lookback) und die Konversion an Tag 45 wird der Anzeige innerhalb von [!DNL Analytics], jedoch nicht innerhalb von Advertising Cloud zugeordnet.

![Beispiel einer Durchsichtskonversion, die in  [!DNL Analytics] aber nicht Advertising Cloud zugeordnet wurde](/help/integrations/assets/a4adc-viewthrough-example.png)

Eine weitere Ursache für Diskrepanzen ist, dass Sie in Advertising Cloud Viewthrough-Konvertierungen eine benutzerdefinierte *Durchsichtsgewichtung* zuweisen können, die relativ zur Gewichtung ist, die einer klickbasierten Konvertierung zugeordnet ist. Die standardmäßige Durchsichtsgewichtung beträgt 40 %, d. h. eine Durchsichtskonversion wird als 40 % des Werts einer klickbasierten Konversion gezählt. [!DNL Analytics] bietet keine solche Gewichtung von Durchsichtsumrechnungen. So wird z. B. eine in [!DNL Analytics] erfasste Bestellung von 100 USD in Advertising Cloud auf 40 USD abgezinst, wenn Sie das standardmäßige Durchsichtsgewicht verwenden - eine Differenz von 60 USD.

Berücksichtigen Sie diese Unterschiede beim Vergleich von Durchsichtskonversionen zwischen Advertising Cloud- und [!DNL Analytics]-Berichten.

#### Verfügbare Attributionsmodelle

| Advertising Cloud Attribution | [!DNL Analytics] Attribution | Zuordnung von eVar/Variablen |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | Nicht zutreffend | Nicht zutreffend |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>Nicht verwenden* |
| [!UICONTROL Weight Last Event More] | Nicht zutreffend | Nicht zutreffend |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | Nicht zutreffend |
| Nicht zutreffend | [!UICONTROL J-Shaped] | Nicht zutreffend |
| Nicht zutreffend | [!UICONTROL Inverse-J] | Nicht zutreffend |
| Nicht zutreffend | [!UICONTROL Custom] | Nicht zutreffend |
| Nicht zutreffend | [!UICONTROL Participation] | Nicht zutreffend |
| Nicht zutreffend | [!UICONTROL Algorithmic] | Nicht zutreffend |

>[!NOTE]
>
>Bei der linearen Zuordnung ordnet [!DNL Analytics] Erfolgsereignisse gleichmäßig allen eVar innerhalb eines Besuchs zu. Verwenden Sie daher die lineare Zuordnung mit dem eVar &quot;Besuch&quot;. Für die Werbung führt die Verwendung der linearen Attribution jedoch zu einer Zuordnung, die nicht wirklich linear ist, und zu weniger als idealen Berichten. Wenn ein Besucher beispielsweise mit drei Anzeigen interagiert, bevor er in drei separate Besuche konvertiert, wird nur die beim letzten Besuch angezeigte Anzeige der Konversion und nicht allen drei Anzeigen zugeordnet.
>
>Darüber hinaus verhindert der Wechsel von &quot;Linear&quot;zur Umrechnungszuordnung die Anzeige von historischen Daten, was zu falsch angegebenen Daten in Berichten führen kann. Beispielsweise kann die lineare Zuordnung den Umsatz auf eine Reihe verschiedener eVar aufteilen. Wenn Sie die Zuordnung zu &quot;Zuletzt verwendet&quot;ändern, werden 100 % dieses Umsatzes mit dem letzten Einzelwert verknüpft. Dieser Zusammenhang kann zu falschen Schlüssen führen.
>
>Um Verwirrung zu vermeiden, macht [!DNL Analytics] historische Daten in der Berichterstellungsoberfläche nicht verfügbar. Sie können die Verlaufsdaten anzeigen, wenn Sie den eVar zurück zur ursprünglichen Zuordnungseinstellung ändern. Sie sollten jedoch die Zuordnungseinstellungen nicht ändern, nur um auf Verlaufsdaten zuzugreifen. Adobe empfiehlt die Verwendung einer neuen eVar, wenn Sie eine neue Zuordnungseinstellung für bereits aufgezeichnete Daten anwenden möchten, anstatt die Zuordnungseinstellungen für eine eVar zu ändern, die bereits über eine beträchtliche Menge historischer Daten verfügt.

Eine Liste der [!DNL Analytics]-Attributionsmodelle und deren Definitionen finden Sie unter [https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html).

Wenn Sie bei Advertising Cloud angemeldet sind, finden Sie eine Liste der Attributionsmodelle unter
[https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm).

#### Ereignisdatumszuordnung in Advertising Cloud

In Advertising Cloud können Sie Konversionsdaten entweder nach dem zugehörigen Klickdatum/Ereignisdatum (dem Datum des Klick- oder Impressionsereignisses) oder nach dem Transaktionsdatum (Konversionsdatum) melden. Das Konzept der Berichterstellung für Klickdaten/Ereignisdaten existiert nicht in [!DNL Analytics]. alle in [!DNL Analytics] verfolgten Konversionen werden nach Transaktionsdatum gemeldet. Daher kann dieselbe Konversion mit unterschiedlichen Daten in Advertising Cloud und [!DNL Analytics] gemeldet werden. Betrachten Sie beispielsweise einen Benutzer, der am 1. Januar auf eine Anzeige klickt und am 5. Januar konvertiert. Wenn Sie die Konversionsdaten nach Ereignisdatum in Advertising Cloud anzeigen, wird die Konversion am 1. Januar gemeldet, wenn der Klick stattgefunden hat. In [!DNL Analytics] würde dieselbe Konversion am 5. Januar gemeldet werden.

![Beispiel einer Konvertierung, die unterschiedlichen Datumsangaben zugeordnet wurde](/help/integrations/assets/a4adc-conversions-based-on.png)

## Attribution in [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/marketing-channels-admin.html) -Reporting ermöglicht Ihnen die Konfiguration von Regeln zur Identifizierung verschiedener Marketing-Kanäle basierend auf unterschiedlichen Aspekten der Trefferinformationen. Sie können von Advertising Cloud verfolgte Kanäle ([!UICONTROL Display Click Through], [!UICONTROL Display View Through] und [!UICONTROL Paid Search]) als [!DNL Marketing Channels] verfolgen, indem Sie den Abfragezeichenfolgenparameter `ef_id` verwenden, um den Kanal zu identifizieren. <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> Obwohl die  [!DNL Marketing Channels] Berichte Advertising Cloud-Kanäle verfolgen können, stimmen die Daten aus verschiedenen Gründen nicht mit den Advertising Cloud-Berichten überein. Weitere Informationen finden Sie in den folgenden Abschnitten.

>[!NOTE]
>
> Die folgenden Kernkonzepte gelten auch für jedes kanalübergreifende Tracking, das Kampagnen umfasst, die nicht in Advertising Cloud verfolgt werden, z. B. die Variable [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) (auch als &quot;Tracking-Code&quot;-Dimension oder &quot;eVar 0&quot; bezeichnet) und das benutzerdefinierte eVar-Tracking.

### Potenziell unterschiedliche Attributionsmodelle in [!DNL Marketing Channels]

Die meisten [!DNL Marketing Channels] -Berichte werden mit der [!UICONTROL Last Touch] -Attribution konfiguriert, für die dem letzten erkannten Marketing-Kanal 100 % des Konversionswerts zugewiesen werden. Die Verwendung verschiedener Attributionsmodelle für die [!DNL Marketing Channels] -Berichte und Advertising Cloud -Berichte führt zu Diskrepanzen bei den zugeordneten Konversionen.

### Ein potenziell unterschiedliches Lookback-Fenster in [!DNL Marketing Channels]

Das Lookback-Fenster für [!DNL Marketing Channels] kann angepasst werden. In Advertising Cloud ist das Klick-Lookback-Fenster konfigurierbar, obwohl es häufig ein festes 60-Tage-Fenster gibt. Wenn die beiden Produkte unterschiedliche Lookback-Fenster verwenden, können Sie Datendiskrepanzen erwarten.

### Verschiedene Kanalzuordnung in [!DNL Marketing Channels]

Advertising Cloud-Berichte erfassen nur gebührenpflichtige Medien, die über Advertising Cloud gehandelt werden (gebührenpflichtige Suche nach Advertising Cloud Search-Anzeigen und Anzeige für Advertising Cloud DSP-Anzeigen), während [!DNL Marketing Channels]-Berichte alle digitalen Kanäle verfolgen können. Dies kann zu einer Diskrepanz im Kanal führen, für den eine Konversion zugeordnet wird.

Beispielsweise haben Paid Search- und natürliche Suchkanäle oft eine symbiotische Beziehung, in der jeder Kanal den anderen unterstützt. Der Bericht [!DNL Marketing Channels] ordnet einige Konversionen der kostenlosen Suche zu, die Advertising Cloud nicht durchführt, da die kostenlose Suche nicht verfolgt wird.

Betrachten wir auch einen Kunden, der eine Display-Anzeige anzeigt, auf eine Paid-Search-Anzeige klickt, in eine E-Mail-Nachricht klickt und dann eine Bestellung von 30 USD aufgibt. Selbst wenn Advertising Cloud und [!DNL Marketing Channels] beide das Attributionsmodell des letzten Kontakts verwenden, wird die Konversion trotzdem den beiden unterschiedlich zugeordnet. Advertising Cloud hat keinen Zugriff auf den Kanal [!UICONTROL Email], daher würde die gebührenpflichtige Suche für die Konversion angerechnet. [!DNL Marketing Channels]hat jedoch Zugriff auf alle drei Kanäle, sodass die Konversion  [!UICONTROL Email] gutgeschrieben wird.

![Beispiel für eine andere Konversionszuordnung in Advertising Cloud im Vergleich  [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

Weitere Informationen dazu, warum die Metriken variieren können, finden Sie unter &quot;[Warum die Kanaldaten zwischen Advertising Cloud und [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md) variieren können&quot;.

## Datenunterschiede in Adobe Analytics [!DNL Paid Search Detection]

Mit der Funktion [legacy [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/paid-search-detection.html) in [!DNL Analytics] können Unternehmen [Regeln definieren, um gebührenpflichtigen und kostenlosen Suchverkehr](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) für bestimmte Suchmaschinen zu verfolgen. Die [!DNL Paid Search Detection]-Regeln verwenden sowohl eine Abfragezeichenfolge als auch die Referrer-Domäne, um den Traffic gebührenpflichtiger und kostenloser Suchen zu identifizieren. Die [!DNL Paid Search Detection] -Berichte sind Teil der größeren Gruppe von [Suchmethoden](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html) -Berichten, die entweder ablaufen, wenn ein bestimmtes Ereignis (z. B. ein Warenkorb zur Kasse) eintritt oder der Besuch endet.

Im Folgenden finden Sie die Benutzeroberfläche zum Erstellen eines [!DNL Paid Search Detection]-Regelsatzes:

![Beispiel für eine Regel zur Erkennung von Paid Search, die in  [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

Die resultierenden [!DNL Paid Search Detection] -Berichte umfassen die Berichte [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine] und [!UICONTROL Natural Search Keywords].

Beachten Sie die folgenden beiden Einschränkungen bei Daten in [!DNL Paid Search Detection] -Berichten:

* Die Berichte [!UICONTROL Paid Search Keywords] und [!UICONTROL Natural Search Keywords] zeigen die Suchabfragen an, die durch die verweisenden URLs identifiziert werden, nicht die Suchbegriffe, für die Benutzer Gebote abgeben. Advertising Cloud- und [!DNL Analytics]-Berichte zeigen die tatsächlichen Suchbegriffe an. Daher erwarten Sie keine Abstimmung mit den [!DNL Paid Search Detection]-Suchbegriffberichten.

* Bei der ursprünglichen Erstellung der Funktion [!DNL Paid Search Detection] war die ursprüngliche Suchabfrage (die Zeichenfolge der Zeichen, die der Benutzer in der Suchleiste der Suchmaschine eingegeben hat) für Advertiser über die verweisende URL leichter verfügbar. Heute verschleiern Suchmaschinen die Suchabfrage weitgehend, und die [!DNL Paid Search Detection]-Suchbegriffberichte sind von begrenztem Wert, da die meisten Abfragedaten unter &quot;Nicht angegeben&quot;fallen.

   Mit [!DNL Analytics for Advertising Cloud] können Advertiser weiterhin gebührenpflichtige Suchbegriffe in [!DNL Analytics] nachverfolgen. Die verweisende Domäne informiert die Suchmaschine darüber, welche Suchmaschine den Traffic verursacht hat. Da die Advertiser-spezifischen Kontoinformationen nicht an die Referrer-Domäne gebunden sind, wird der gesamte Traffic unter der Suchmaschine aufgeführt. Werbetreibende mit mehreren Konten in derselben Suchmaschine sollten für kontospezifische Berichte auf Advertising Cloud- oder [!DNL Analytics]-Berichte verweisen.

### Warum [!DNL Paid Search Detection] konfigurieren?

Die [!DNL Paid Search Detection] -Berichte ermöglichen es Ihnen, den natürlichen Suchtraffic in den [[!DNL Analytics Marketing Channels] Berichten](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/marketing-channels-admin.html) zu identifizieren. Die Trennung von Paid Search-Traffic und kostenlosem Suchverkehr ist eine hervorragende Möglichkeit, den Wert zu verstehen, den die natürliche Suche für das gesamte Marketing-Ökosystem bringt.

## Validierung von Clickthrough-Daten für [!DNL Analytics for Advertising Cloud] {#data-validation}

Für Ihre Integration sollten Sie Ihre Clickthrough-Daten validieren, um sicherzustellen, dass alle Seiten auf Ihrer Site Clickthroughs ordnungsgemäß verfolgen.

Eine der einfachsten Methoden zur Validierung der [!DNL Analytics for Advertising Cloud]-Verfolgung in [!DNL Analytics] besteht darin, Klicks mit Instanzen zu vergleichen, indem die berechnete Metrik &quot;Klicks zu AMO-ID-Instanzen&quot;verwendet wird, die wie folgt berechnet wird:

```Clicks to AMO ID Instances = (AMO ID Instances / AMO Clicks)```

[!UICONTROL AMO ID Instances] gibt an, wie oft AMO-IDs (`s_kwcid` -Parameter) auf der Site verfolgt werden. Jedes Mal, wenn auf eine Anzeige geklickt wird, wird der Landingpage-URL ein Parameter `s_kwcid` hinzugefügt. Die Anzahl von [!UICONTROL AMO ID Instances] entspricht daher der Anzahl der Klicks und kann anhand der tatsächlichen Anzeigenklicks überprüft werden. Normalerweise sehen wir eine Übereinstimmungsrate von 80 % für [!DNL Search] und eine Übereinstimmungsrate von 30 % für [!DNL DSP] Traffic (wenn gefiltert, um nur Clickthrough [!UICONTROL AMO ID Instances] einzuschließen). Der Unterschied in den Erwartungen zwischen Suche und Anzeige lässt sich durch das erwartete Traffic-Verhalten erklären. Die Suche erfasst die Absicht, und daher möchten Benutzer in der Regel auf die Suchergebnisse aus ihrer Abfrage klicken. Benutzer, die eine Anzeige oder Online-Videoanzeige sehen, klicken mit höherer Wahrscheinlichkeit unbeabsichtigt auf die Anzeige und springen dann entweder von der Site aus oder verlassen das neue Fenster, das geladen wird, bevor die Seitenaktivität verfolgt wird.

In Advertising Cloud-Berichten können Sie Klicks auf ähnliche Weise mit Instanzen vergleichen, indem Sie die Metrik &quot;[!UICONTROL ef_id_instances]&quot;anstelle von [!UICONTROL AMO ID Instances] verwenden:

```Clicks to [!UICONTROL EF ID Instances] = (ef_id_instances / Clicks)```

Obwohl Sie eine hohe Übereinstimmungsrate zwischen der AMO-ID und der EF-ID erwarten sollten, sollten Sie nicht mit einer 100-%-Parität rechnen, da AMO-ID und EF-ID grundsätzlich unterschiedliche Daten verfolgen. Dieser Unterschied kann zu leichten Unterschieden bei den Gesamtwerten [!UICONTROL AMO ID Instances] und [!UICONTROL EF ID Instances] führen. Wenn sich die Summe von [!UICONTROL AMO ID Instances] in [!DNL Analytics] um mehr als 1 % von [!UICONTROL EF ID Instances] in Advertising Cloud unterscheidet, wenden Sie sich jedoch an Ihren Kundenbetreuer für Adoben, um Hilfe zu erhalten.

Weitere Informationen zur AMO-ID und zur EF ID finden Sie unter [Von Analytics verwendete Advertising Cloud-IDs](ids.md).

Im Folgenden finden Sie ein Beispiel für einen Arbeitsbereich zum Verfolgen von Klicks zu Instanzen.

![Beispiel eines Arbeitsbereichs zum Verfolgen von Klicks zu Instanzen](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## Vergleichen von Datensätzen in [!DNL Analytics for Advertising Cloud] im Vergleich zu Advertising Cloud

Die [AMO-ID](ids.md) (Abfragezeichenfolgenparameter s_kwcid) wird für die Berichterstellung in [!DNL Analytics] verwendet und die [EF ID](ids.md) wird für die Berichterstellung in Advertising Cloud verwendet. Da es sich um unterschiedliche Werte handelt, kann ein Wert beschädigt oder nicht zur Landingpage hinzugefügt werden.

Angenommen, wir haben die folgende Landingpage:

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id`

wobei die EF ID &quot;`test_ef_id`&quot;und die AMO-ID &quot;`test_amo_id`&quot;lautet.

Wenn eine Site-seitige Umleitung erfolgt, könnte die URL wie folgt enden:

`www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag`

wobei die EF ID &quot;`test_ef_id`&quot;und die AMO-ID &quot;`test_amo_id#redirectAnchorTag`&quot;lautet.

In diesem Beispiel fügt das Hinzufügen des Anker-Tags der AMO-ID unerwartete Zeichen hinzu, was zu einem Wert führt, den Analytics nicht erkennt. Diese AMO-ID würde nicht klassifiziert und die damit verbundenen Konversionen würden unter &quot;[!UICONTROL unspecified]&quot;oder &quot;[!UICONTROL none]&quot;in [!DNL Analytics] -Berichten fallen.

Glücklicherweise sind Probleme wie dieses häufig, führen aber normalerweise nicht zu einem hohen Prozentsatz an Diskrepanzen. Wenn Sie jedoch eine große Diskrepanz zwischen AMO-IDs in [!DNL Analytics] und EF-IDs in Advertising Cloud feststellen, wenden Sie sich an Ihren Adobe-Kundenbetreuer, um Hilfe zu erhalten.

## Andere Metrikaspekte

### Unterschied zwischen Klicks und Besuchen {#clicks-vs-visits}

Sie scheinen identisch zu sein, Klicks und Besuche stellen jedoch unterschiedliche Daten dar:

* **Klicken:** [!DNL DSP] oder die Suchmaschine zeichnet einen Klick auf, wenn ein Besucher auf eine Anzeige auf der Website eines Herausgebers klickt.

* **Besuch:** [!DNL Analytics] definiert eine  [](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) Reihe von Seitenansichten eines Benutzers, die anhand eines von mehreren Kriterien enden, z. B. einer Inaktivität von 30 Minuten.

Ein Klick kann definitionsgemäß zu mehreren Besuchen führen.

Betrachten Sie das folgende Beispiel: Benutzer 1 und Benutzer 2 greifen auf eine Site zu, indem sie auf eine Advertising Cloud-Anzeige klicken. Benutzer 1 zeigt vier Seiten an und verlässt den Tag, sodass der erste Klick zu einem Besuch führt. Benutzer 2 zeigt zwei Seiten an, verlässt das Mittagessen 45 Minuten, gibt zurück, zeigt zwei weitere Seiten an und verlässt es dann. in diesem Fall führt der erste Klick zu zwei Besuchen.

![Beispiel für den Unterschied zwischen Klicks und Besuchen](/help/integrations/assets/a4adc-visits-example.png)

### Unterschied zwischen Klicks und Clickthroughs

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

Klicks und Clickthroughs sind zwei verschiedene Metriken:

* **Klicken:** [!DNL DSP] oder die Suchmaschine zeichnet einen Klick auf, wenn ein Besucher auf eine Anzeige auf der Website eines Herausgebers klickt.

* **Clickthroughs:** [!DNL Analytics] zeichnet einen Clickthrough auf, wenn der Besucher auf die Ziel-Website gelangt, die Landingpage geladen wird und die  [!DNL Analytics] Anforderung am Ende der Seite die Daten an  [!DNL Analytics]sendet.

Klicks und Clickthroughs können aufgrund versehentlicher Anzeigenklicks stark voneinander abweichen. Wir haben festgestellt, dass es sich bei den meisten Klicks auf Display-Anzeigen um versehentliche Klicks handelt. Diese versehentlichen Besucher drücken die Schaltfläche Zurück , bevor die Landingpage geladen wird. [!DNL Analytics] kann also keine Clickthrough-Raten aufzeichnen. Dies gilt insbesondere für Anzeigen, bei denen ein versehentlicher Klick wahrscheinlicher ist, wie mobile Anzeigen, Videoanzeigen und Anzeigen, die den Bildschirm ausfüllen und geschlossen werden müssen, bevor der Benutzer die Seite anzeigen kann.

Auf Mobilgeräten geladene Sites führen aufgrund niedrigerer Bandbreiten oder verfügbarer Verarbeitungsleistung auch weniger zu Clickthroughs, sodass das Laden von Landingpages länger dauert. Es ist nicht ungewöhnlich, dass 50-70 % der Klicks zu keinen Clickthroughs führen. In mobilen Umgebungen kann der Unterschied bis zu 90 % betragen, da die Kombination aus einem langsameren Browser und der höheren Wahrscheinlichkeit besteht, dass der Benutzer versehentlich auf die Anzeige klickt, während er durch die Seite scrollt oder versucht, die Anzeige zu schließen.

Die Klickdaten können auch in Umgebungen aufgezeichnet werden, in denen Clickthroughs nicht mit den aktuellen Tracking-Mechanismen aufgezeichnet werden können (z. B. Klicks in oder von einer mobilen App) oder bei denen der Advertiser nur einen Tracking-Ansatz implementiert hat (z. B. beim JavaScript-Ansichtsansatz verfolgen Browser, die Drittanbieter-Cookies blockieren, Klicks, jedoch keine Clickthroughs). Ein wichtiger Grund, warum Adobe die Bereitstellung sowohl der Klick-URL-Tracking- als auch der Durchsichts-JavaScript-Tracking-Ansätze empfiehlt, besteht darin, die Abdeckung verfolgbarer Clickthroughs zu maximieren.

### Verwenden von Advertising Cloud-Traffic-Metriken für Nicht-Advertising Cloud-Dimensionen

Advertising Cloud bietet Analytics [werbespezifische Traffic-Metriken und die zugehörigen Dimensionen aus DSP und Suche](advertising-cloud-metrics-in-analytics.md). Die von Advertising Cloud bereitgestellten Metriken gelten nur für die angegebenen Advertising Cloud-Dimensionen und Daten sind nicht für andere Dimensionen in [!DNL Analytics] verfügbar.

Wenn Sie beispielsweise die Metriken [!UICONTROL AMO Clicks] und [!UICONTROL AMO Cost] nach Konto anzeigen, die eine Advertising Cloud-Dimension sind, werden die Gesamtwerte [!UICONTROL AMO Clicks] und [!UICONTROL AMO Cost] nach Konto angezeigt.

![Beispiel für Advertising Cloud-Metriken in einem Bericht mit einer Advertising Cloud-Dimension](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

Wenn Sie die Metriken [!UICONTROL AMO Clicks] und [!UICONTROL AMO Cost] jedoch nach einer On-Page-Dimension (z. B. Seite) anzeigen, für die Advertising Cloud keine Daten bereitstellt, dann sind [!UICONTROL AMO Clicks] und [!UICONTROL AMO Cost] für jede Seite null (0).

![Beispiel für Advertising Cloud-Metriken in einem Bericht mit einer nicht unterstützten Dimension](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### Verwendung von [!UICONTROL AMO ID Instances] als Ersatz für Klicks mit Nicht-Advertising Cloud-Dimensionen

Da Sie [!UICONTROL AMO Clicks] nicht mit On-site-Dimensionen verwenden können, sollten Sie ein Äquivalent zu Klicks finden. Sie sind möglicherweise versucht, Besuche als Ersatz zu verwenden, doch sind sie nicht die beste Option, da jeder Besucher mehrere Besuche haben kann. (Siehe &quot;[Der Unterschied zwischen Klicks und Besuchen](#clicks-vs-visits)&quot;. Stattdessen empfehlen wir die Verwendung von [!UICONTROL AMO ID Instances], d. h. die Häufigkeit, mit der die AMO-ID erfasst wird. Auch wenn [!UICONTROL AMO ID Instances] nicht genau mit [!UICONTROL AMO Clicks] übereinstimmt, sind sie die beste Option zur Messung des Klick-Traffics auf der Site. Weitere Informationen finden Sie unter &quot;[Datenvalidierung für [!DNL Analytics for Advertising Cloud]](#data-validation)&quot;.

![Beispiel  [!UICONTROL AMO ID Instances] anstelle  [!UICONTROL AMO Clicks] einer nicht unterstützten Dimension](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [Übersicht über [!DNL Analytics for Advertising Cloud]](overview.md)
>* [Von verwendete Advertising Cloud IDs [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Advertising Cloud-Metriken in Analysis Workspace](/help/integrations/analytics/advertising-cloud-metrics-in-analytics.md)
>* [[!DNL Analytics] Daten in Advertising Cloud](/help/integrations/analytics/analytics-data-in-advertising-cloud.md)
>* [Wozu unterscheiden sich die Daten zwischen Advertising Cloud und [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)

