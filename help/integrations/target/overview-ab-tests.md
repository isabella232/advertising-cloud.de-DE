---
title: Konfigurieren von A/B-Tests für Adobe Advertising Ads in Adobe Target
description: Erfahren Sie, wie Sie einen A/B-Test einrichten in [!DNL Target] für Ihre DSP und [!DNL Search] Anzeigen.
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '1647'
ht-degree: 0%

---

# Konfigurieren von A/B-Tests in Adobe Target für Advertising DSP und [!DNL Advertising Search] Anzeigen

<!-- Add [!UICONTROL and [!DNL tags throughout as needed. -->

<!-- Break into sub-files, or just leave as one? -->

*Advertiser nur mit Advertising DSP*

Adobe Advertising und Adobe Target erleichtern Marketingexperten die Bereitstellung eines personalisierten und vernetzten Erlebnisses über Paid Media und On-site-Messaging hinweg. Durch die Freigabe von Signalen zwischen den Produkten können Sie:

* Verringern Sie die Site-Durchfallraten, indem Sie die Anzeigenbelichtung von Kunden aus DSP Kampagnen mit ihren Vor-Ort-Erlebnissen verknüpfen.

* Richten Sie A/B-Tests ein, indem Sie On-site-Erlebnisse mit Werbe-Messaging unter Verwendung von Adobe Audience Manager-Belichtungsdaten und Target-Zielgruppen mit Klick-zu-Feed-Zugriff spiegeln.

* Messen Sie die Auswirkungen von einheitlichem Messaging auf eine objektive Steigerung vor Ort mit einfachen Visualisierungen in Adobe Analytics für [!DNL Target].

In den folgenden Abschnitten finden Sie die Voraussetzungen und Anweisungen zum Einrichten von Clickthrough- und Durchsichtsverfolgung, Implementieren der Signalfreigabe zwischen DSP und [!DNL Target] und eine A/B-Test-Aktivität einrichten und [!DNL Analytics] Analysis Workspace zum Anzeigen der Testdaten.

Wenn Sie weitere Fragen haben, wenden Sie sich an adcloud_support@adobe.com.

## Voraussetzungen

Für dieses Anwendungsbeispiel sind die folgenden Produkte und Integrationen erforderlich:

* [!DNL Target]

* [[!DNL Analytics] für Werbung](/help/integrations/analytics/overview.md) Integration<!-- necessary for testing view-throughs, which most advertisers want to do -->

* [[!DNL Analytics] für [!DNL Target]](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) Integration

* Audience Manager (nur für Durchsichtstests erforderlich)

## Schritt 1: Einrichten des Clickthrough-Frameworks {#click-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![Clickthrough-Framework](/help/integrations/assets/target-ct-framework.png)

Wenn Sie DSP Makros zu einer Clickthrough-URL hinzufügen (die URL, die angezeigt wird, wenn ein Benutzer auf eine Anzeige klickt und die Landingpage erreicht), erfasst DSP automatisch den Platzierungsschlüssel, indem ```${TM_PLACEMENT_ID}``` in der Clickthrough-URL. Dieses Makro erfasst den alphanumerischen Platzierungsschlüssel und nicht die numerische Platzierungs-ID.

![An die Landingpage-URL angehängte Clickthrough-URL](/help/integrations/assets/target-ct-url.jpg)

### (Nur DSP) Hinzufügen von DSP Makros zu Ihren Clickthrough-URLS

<!-- If we ever write instructions for ads on other ad servers (such as Sizmek ads in DCO), then work that into the following section. -->

Aktualisieren Sie im Flash-Gespräch oder in Google Campaign Manager 360 die Clickthrough-URL für jede Anzeige manuell, um die Makros einzuschließen, die zum Erfassen von AMO-ID-Variablen erforderlich sind. Die AMO-ID-Variablen werden verwendet, um Klickdaten an Adobe Analytics zu senden und Platzierungsschlüssel für A/B-Tests freizugeben. Anweisungen finden Sie auf den folgenden Seiten:

* [Anhängen [!DNL Analytics for Advertising] Makros zu [!DNL Flashtalking] Anzeigen-Tags](/help/integrations/analytics/macros-flashtalking.md)

* [Anhängen [!DNL Analytics for Advertising] Makros zu [!DNL Google Campaign Manager 360] Anzeigen-Tags](/help/integrations/analytics/macros-google-campaign-manager.md)

Wenden Sie sich an Ihr DSP Account-Team und die Advertising Solutions Group (aac-advertising-solutions-group@adobe.com), um den erforderlichen Platzierungsschlüssel abzurufen und das Setup abzuschließen und sicherzustellen, dass jede Clickthrough-URL mit dem Platzierungsschlüssel ausgefüllt wird.

## Schritt 2: Einrichten des Durchsichts-Frameworks mit dem Audience Manager {#view-through-framework}

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

![Durchsicht-Framework](/help/integrations/assets/targetr-vt-framework.png)

Durch Hinzufügen eines Audience Manager-Impressionsereignis-Pixels zu Ihren Anzeigen-Tags und Platzierungseinstellungen können Sie ein Testsegment erstellen, um weitere Ansichtsdurchsatztestmöglichkeiten zu erhalten.

1. Implementieren Sie ein Impressionsereignis-Pixel für Audience Manager in Ihre Anzeigen-Tags und DSP Platzierungseinstellungen.

   Weitere Informationen finden Sie unter &quot;[Erfassen von Medienbelichtungsdaten aus Werbekampagnen DSP](/help/integrations/audience-manager/media-data-integration/collect.md).&quot;

   Stellen Sie sicher, dass [DSP Makros](/help/dsp/campaign-management/macros.md) zum Erfassen aller Daten, die das Impressionsereignis-Pixel zurückgeben soll, einschließlich `${TM_PLACEMENT_ID_NUM}` für die numerische Platzierungs-ID.

   >[!NOTE]
   >
   >Klick-Tracking-URLs enthalten die `${TM_PLACEMENT_ID}` Makro für den alphanumerischen Platzierungsschlüssel anstelle von `${TM_PLACEMENT_ID_NUM}` für die numerische Platzierungs-ID.

1. Konfigurieren Sie ein Audience Manager-Segment aus DSP Impressionsdaten:

   1. Navigieren Sie zu **Audience Manager** > **Zielgruppendaten** > **Signale** und wählen Sie anschließend die **Suche** Registerkarte oben links.

   1. Geben Sie die **Schlüssel** und **Wert** für das Signal, das bestimmt, auf welcher Ebene die Segmentbenutzer gruppiert werden. Verwenden Sie eine [unterstützter Schlüssel](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html?lang=en) mit einem Wert, der einem Makro entspricht, das Sie dem Impressionsereignis-Pixel des Audience Managers hinzugefügt haben.

      Um beispielsweise Benutzer für eine bestimmte Platzierung zu gruppieren, verwenden Sie die `d_placement` Schlüssel. Verwenden Sie für den Wert eine tatsächliche numerische Platzierungs-ID (z. B. 2501853 im obigen Screenshot), die vom DSP erfasst wird. `${TM_PLACEMENT_ID_NUM}`. <!-- Explain where to find the placement ID, other than in a custom report. -->

      Wenn im Feld Gesamtanzahl die Benutzerzahlen für das Schlüssel-Wert-Paar angezeigt werden, was bedeutet, dass das Pixel korrekt platziert wurde und Daten fließen, können Sie mit dem nächsten Schritt fortfahren.
   ![Suchsignale](/help/integrations/assets/target-am-signals.png)

1. [Regelbasierte Eigenschaft erstellen](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) für die Segmenterstellung in Audience Manager.

   1. Benennen Sie die Eigenschaft so, dass sie in Testaktivitäten leicht identifiziert werden kann. Speichern Sie die Eigenschaft in dem Ordner, den Sie bevorzugen.

   1. Aus dem **Datenquelle** Dropdown-Menü auswählen **Ad Cloud**.

   1. Fügen Sie im Ausdrucksgenerator ```d_event``` im Feld Schlüssel und ```imp``` im **Wert** Feld, wählen Sie **Regel hinzufügen** und speichern Sie dann die Eigenschaft.

   ![Screenshot einer regelbasierten Eigenschaft](/help/integrations/assets/target-am-trait.png)

1. Richten Sie ein Testsegment in Audience Manager ein:

   1. Navigieren Sie oben auf der Seite zu **Zielgruppendaten** > **Eigenschaften** und suchen Sie nach dem vollständigen Eigenschaftsnamen. Aktivieren Sie das Kontrollkästchen neben dem Eigenschaftsnamen und klicken Sie auf **Segment erstellen**.

   1. Benennen Sie das Segment, wählen Sie `Ad Cloud` als **Datenquelle** und speichern Sie das Segment.

      Audience Manager teilt das Segment automatisch in eine Kontrollgruppe auf, die das standardmäßige Landingpage-Erlebnis erhält, und in eine Testgruppe, die ein personalisiertes Onsite-Erlebnis erhalten hat.
   ![Screenshot eines Testsegments](/help/integrations/assets/target-am-segment.png)

## Schritt 3: Einrichten einer A/B-Test-Aktivität in Target

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

In den folgenden Anweisungen werden Informationen zum DSP Anwendungsfall hervorgehoben. Eine vollständige Anleitung finden Sie unter &quot;[Erstellen eines A/B-Tests](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html.&quot;

1. [Bei Adobe Target anmelden](https://experienceleague.adobe.com/docs/target/using/introduction/target-access-from-mac.html).

1. Aus dem **Tätigkeiten** Liste, klicken Sie auf **Aktivität erstellen** > **A/B-Test**.

   ![Erstellen einer A/B-Test-Aktivität](/help/integrations/assets/target-create-ab.png)

1. Im **Aktivitäts-URL eingeben*** ein, geben Sie die URL der Landingpage für den Test ein.

   ![Feld &quot;Aktivitäts-URL&quot;](/help/integrations/assets/target-create-ab-url.png)

   >[!NOTE]
   >
   >Sie können mehrere URLs verwenden, um den Viewthrough-Site-Einstieg zu testen. Weitere Informationen finden Sie unter &quot;[Mehrseitige Aktivität](https://experienceleague.adobe.com/docs/target/using/experiences/vec/multipage-activity.html).&quot; Sie können die Top-Einträge einfach anhand der Seiten-URL identifizieren, indem Sie eine [Site-Einstiegsbericht](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/integrations/ad-cloud/create-advertising-cloud-site-entry-reports.html) in Analytics.

1. Im **Ziel** geben Sie die Erfolgsmetrik für den Test ein.

   >[!NOTE]
   >
   >Stellen Sie sicher, dass [!DNL Analytics] als Datenquelle in [!DNL Target]und dass die richtige Report Suite ausgewählt ist.

1. Legen Sie die **Priorität** nach `High` oder `999` um Konflikte zu vermeiden, wenn Benutzer im Testsegment ein falsches On-site-Erlebnis erhalten.

1. Within **Berichtseinstellungen**, wählen Sie die **Firmenname** und **Report Suite** mit Ihrem DSP-Konto verbunden.

   Weitere Tipps zur Berichterstellung finden Sie unter[Best Practices und Fehlerbehebung für die Berichterstellung](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/report-troubleshooting.html).&quot;

1. Im **Datumsbereich** geben Sie das entsprechende Start- und Enddatum für den Test ein.

1. Fügen Sie der Aktivität Zielgruppen hinzu:

   1. Wählen Sie die [Segment, das Sie zuvor in Audience Manager erstellt haben, um Durchsichtszielgruppen zu testen](#view-through-framework).

      ![Zielgruppen zur Aktivität hinzufügen](/help/integrations/assets/target-create-ab-audiences.png)

   1. Auswählen **Seiten der Site** > **Landingpage** > **Abfrage** und geben Sie den DSP Platzierungsschlüssel in die **Wert** -Feld, um die Target-Abfragezeichenfolgenparameter für Clickthrough-Zielgruppen zu verwenden.

      ![Screenshot einer Zielklick-Zielgruppe](/help/integrations/assets/target-click-audience.jpg)

1. Für **Traffic-Zuordnungsmethode** auswählen **Manuell (Standard)** und teilen Sie die Zielgruppe 50/50 auf.

1. Speichern Sie die Aktivität.

1. Verwendung [!DNL Target] [Visual Experience Composer](https://experienceleague.adobe.com/docs/target/using/activities/abtest/create/test-create-ab.html) , um Designänderungen an der Landingpage-Vorlage für A/B-Tests vorzunehmen.

   * Erlebnis A: Bearbeiten Sie nicht, da dies das standardmäßige/steuerbare Landingpage-Erlebnis ohne Personalisierung ist.

   * Erlebnis B: Verwenden Sie die [!DNL Target] -Benutzeroberfläche, um die Landingpage-Vorlage auf der Grundlage der im Test enthaltenen Assets anzupassen (z. B. Überschriften, Kopien, Schaltflächenplatzierung und Kreativinhalte).
   >[!NOTE]
   >
   >Wenden Sie sich beispielsweise bei kreativen Tests an Ihr Account-Team.

## Schritt 4: Richten Sie Ihre [!DNL Analytics for Target] Analysis Workspace in [!DNL Analytics]

<!-- [If separate page, add "Adobe" before first-use of product names.] -->

[!DNL Analytics for Target] (A4T) ist eine lösungsübergreifende Integration, mit der Advertiser Inhalte erstellen können. [!DNL Target] Aktivitäten, die auf [!DNL Analytics] Konversionsmetriken und Zielgruppensegmente verwenden und dann die Ergebnisse mit [!DNL Analytics] als Berichtsquelle. Alle Berichte und Segmentierungen für diese Aktivität basieren auf [!DNL Analytics] Datenerfassung.

Weitere Informationen finden Sie unter [!DNL Analytics for Target], einschließlich eines Links zu Implementierungsanweisungen, siehe[Adobe Analytics als Berichtsquelle für Adobe Target (A4T)](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html)&quot;.

### Richten Sie die [!DNL Analytics for Target] Bedienfeld

Konfigurieren Sie in Analysis Workspace die [!DNL Analytics for Target panel] , um Ihre [!DNL Target] Aktivitäten und Erlebnisse. Beachten Sie die folgenden wichtigen Hinweise und Informationen zu Ihren Berichten.

#### Metriken

* Erstellen Sie innerhalb des Arbeitsbereichs einen Bereich, der spezifisch für die Adobe Advertising-Kampagne, das -Paket oder die Platzierung ist, für die der Test ausgeführt wurde. Verwenden Sie Zusammenfassende Visualisierungen, um Adobe Advertising-Metriken im selben Bericht wie die Target-Testleistung anzuzeigen.

* Priorisieren Sie die Verwendung von On-site-Metriken (z. B. Besuche und Konversionen), um die Leistung zu messen.

* Beachten Sie, dass aggregierte Medienmetriken aus Adobe Advertising (wie Impressionen, Klicks und Kosten) nicht mit Target-Metriken übereinstimmen können.

#### Dimensionen

Die folgenden Dimensionen beziehen sich auf [!DNL Analytics for Target]:

* **Target Activities**: Name des A/B-Tests

* **Target-Erlebnisse**: Namen der in der Aktivität verwendeten Landingpage-Erlebnisse

* **Target-Aktivität** > **Erlebnis**: Aktivitäts- und Erlebnisname in derselben Zeile

### Fehlerbehebung in Analytics für [!DNL Target] Daten

Wenn Sie in Analysis Workspace feststellen, dass die Daten zu Aktivitäten und Erlebnissen minimal sind oder nicht ausgefüllt werden, führen Sie die folgenden Schritte aus:

* Stellen Sie sicher, dass für Target und Analytics dieselbe zusätzliche Daten-ID (SDID) verwendet wird. Sie können die SDID-Werte mithilfe der [Adobe Experience Cloud Debugger](https://experienceleague.adobe.com/docs/target-learn/tutorials/troubleshooting/troubleshoot-with-the-experience-cloud-debugger.html) auf der Landingpage, zu der die Kampagne Benutzer steuert.

[Zusätzliche Daten-ID-Werte (SDID) in Adobe Debugger](/help/integrations/assets/target-troubleshooting-sdid.png)

* Vergewissern Sie sich auf derselben Landingpage, dass a) der im Adobe Debugger unter &quot;Lösungen&quot;> &quot;Ziel&quot;angezeigte Hostname mit b) dem in [!DNL Target] für die Aktivität (unter Ziele und Einstellungen > Berichtseinstellungen).

   [!DNL Analytics For Target] erfordert [!DNL Analytics] Tracking-Server, der bei Aufrufen von [!DNL Target] der [!DNL Modstats] Datenerfassungsserver für Analytics.&lt;!— nur &quot;zu Analytics?&quot;>

[Hostnamenwert in Adobe Debugger](/help/integrations/assets/target-troubleshooting-hostname.png)

[Tracking-Server-Wert in Target](/help/integrations/assets/target-troubleshooting-tracking-server.png)

## Weitere Informationen

* [Integration von Target in Analytics](https://experienceleague.adobe.com/docs/target-learn/tutorials/integrations/3.2-target-analytics.html)- Erklärt, wie Sie Target-Berichte in Analysis Workspace einrichten.
* [Überblick über A/B-Tests](https://experienceleague.adobe.com/docs/target/using/activities/abtest/test-ab.html) - Beschreibt A/B-Test-Aktivitäten, die Sie mit DSP Anzeigen verwenden können.
* [Erlebnisse und Angebote](https://experienceleague.adobe.com/docs/target/using/experiences/experiences.html) - Erläuterung [!DNL Target] Tools zur Bestimmung der On-site-Inhalte, denen DSP Testbenutzer ausgesetzt sind.
* [Signale, Eigenschaften und Segmente](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/signal-trait-segment.html) - Definiert einige der Audience Manager-Tools, die beim DSP Durchsichtstest helfen können.
* [Übersicht über Analytics für Advertising](/help/integrations/analytics/overview.md) - Einführung in Analytics for Advertising, mit dem Sie Clickthrough- und Durchsichts-Site-Interaktionen in Ihren Analytics-Instanzen verfolgen können.

<!-- 
>[!MORELIKETHIS]
>
>* 
-->
