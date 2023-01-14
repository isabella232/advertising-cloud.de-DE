---
title: Best Practices zum Erstellen eines benutzerdefinierten Ziels
description: Lernen Sie die Best Practices zum Erstellen benutzerdefinierter Ziele kennen, um Ihre Erfolgsereignisse zu definieren.
feature: DSP Optimization, DSP Best Practices
exl-id: 54b16325-4b72-48a3-a2e0-4e342229211c
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# Best Practices zum Erstellen eines benutzerdefinierten Ziels

## Benutzerdefinierte Ziele mit einer einzelnen Eigenschaft

Die folgenden Beispiele zeigen, wie Sie Ziele konfigurieren können, die auf eine einzelne Eigenschaft (Metrik) abzielen.

### Beispiel für eine Kampagne mit dem[!UICONTROL Highest ROAS - Custom Goal]&quot;Optimierungsziel

Wenn Ihr Kampagnenziel Umsatz ist ([!UICONTROL Highest ROAS - Custom Goal]), dann enthält Ihr benutzerdefiniertes Ziel (Ziel) die[!UICONTROL Revenue]&quot; Eigenschaft mit einer Gewichtung von 1 (1).

![Beispiel eines benutzerdefinierten ROAS-Ziels mit einer einzelnen Eigenschaft](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] von einem entspricht einem Wert von 1 für jeden verfolgten Umsatz von 1 USD.
>
> Beispielsweise wird eine Konversion von 250 USD mit einer Gewichtung von 1 als 250 USD gemeldet. Wenn der Konversionsmetrik eine Gewichtung von 0,5 zugewiesen wird, wird die Konversion von 250 USD als 125 USD in Adobe Advertising ( 250 USD Konversion * 0,5) gemeldet. [!UICONTROL Property Weight] = 125 USD).

### Beispiel für eine Kampagne mit dem[!UICONTROL Lowest CPA - Custom Goal]&quot;Optimierungsziel

Wenn Ihr Kampagnenziel die niedrigsten Kosten pro Akquise (CPA) ist und nur ein Erfolgsereignis erforderlich ist, schließen Sie diese Metrik ein (im folgenden Beispiel &quot;Antragsversand&quot;). Als Best Practice wird empfohlen, die Gewichtung auf 1 (1) festzulegen.

![Beispiel eines benutzerdefinierten CPA-Ziels mit einer einzelnen Eigenschaft](/help/dsp/assets/custom-goal-roas.png)

>[!NOTE]
>
> A [!UICONTROL Property Weight] von eins entspricht einem Wert für jede verfolgte Konversion.
>
> Wenn z. B. 10 Konvertierungen von Antragssendungen verfolgt werden, werden 10 Konversionen von Antragsübermittlungen gemeldet.  Wenn der Konversionsmetrik eine Gewichtung von 0,5 zugewiesen wird, werden die 10 Konversionen als fünf (5) in Adobe Advertising (10 Konversionen * 0,5) gemeldet. [!UICONTROL Property Weight] = 5).

## Benutzerdefinierte Ziele mit mehreren Eigenschaften

Es gibt zwei Szenarien, in denen Sie mehrere Eigenschaften in einem benutzerdefinierten Ziel verwenden würden:

* Ihr Kampagnenziel umfasst mehrere Erfolgsereignisse. Vielleicht werben Sie beispielsweise für mehr als eine On-site-Aktion und werden alle Ihrem CPA-Ziel zugeordnet. Das folgende Beispielziel umfasst drei separate Eigenschaften (PDF Download, Kontaktaufnahme und E-Mail-Anmeldung) mit jeweils einer Gewichtung (1), die dem [!DNL Adobe Sensei] -Algorithmus, dass jede der Eigenschaften dieselbe Bedeutung hat. Wenn Sie Eigenschaften mit unterschiedlichen Kosten oder Bedeutung einbeziehen, können Sie ihre relative Gewichtung entsprechend anpassen.

   ![Beispiel eines benutzerdefinierten Ziels mit mehreren Eigenschaften](/help/dsp/assets/custom-goal-multiple-properties.png)

* Die einzelne Eigenschaft in Ihrem benutzerdefinierten Ziel erreicht nicht die Mindestanzahl von 10 Konversionen pro Tag, die für eine optimierte Leistung erforderlich sind. Dies kann durch minimale tägliche Paketausgaben oder eine begrenzte Anzahl natürlicher Konversionen geschehen. Das Hinzufügen zusätzlicher unterstützender Eigenschaften zum benutzerdefinierten Ziel kann Ihnen dabei helfen, den Schwellenwert von 10 Konversionen pro Tag zu erreichen. Zehn unterstützende Ereignisse können einem Paket helfen, die Schwelle von 10 Tagen zu erreichen, selbst wenn jede seiner Gewichtungen unter 1 liegt. Sie müssen jedoch möglicherweise nicht so viele Ereignisse hinzufügen.

   Wenn Sie einem benutzerdefinierten Ziel unterstützende Eigenschaften hinzufügen, gewichten Sie diese entsprechend ihrer relativen Bedeutung für das Haupterfolgsereignis und beachten Sie die Anzahl der Datenpunkte. Dadurch kann der Adobe Sensei-Algorithmus mehrere Eigenschaften miteinander in Einklang bringen und Ihr Ziel optimieren.

   Das folgende Beispielziel umfasst drei Eigenschaften mit jeweils unterschiedlicher Gewichtung: Application Submit = 1, Application Start = 0.1 und Advertiser Landingpage = 0.01. Das bedeutet, dass jede Application Submit-Konversion denselben Wert wie ein Durchschnitt von 10 Application Start-Konversionen und 100 Advertiser-Landingpage-Konversionen für Ihr Unternehmen hat.

   ![Beispiel eines benutzerdefinierten Ziels mit mehreren Eigenschaften](/help/dsp/assets/custom-goal-multiple-properties2.png)

   Wenn Sie stattdessen die Besuche von Landingpages gleich den Einstiegsseiten-Besuchen gewichten, könnte die natürlich höhere Anzahl von Einstiegsseitenbesuchen Ihr Ziel überfordern und zu den Einstiegsseitenbesuchen verfälschen.<!--reword-->

>[!MORELIKETHIS]
>
>* [Über benutzerdefinierte Ziele](custom-goal-about.md)
>* [Benutzerdefiniertes Ziel erstellen](custom-goal-create.md)
>* [Optimierungsziele und Verwendung](optimization-goals.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
> * [Wie DSP Ihre Kampagnen optimiert](optimization-how-dsp-optimizes-campaigns.md)

