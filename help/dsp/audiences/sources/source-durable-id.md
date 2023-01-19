---
title: Authentifizierte Segmente von dauerhaften ID-Partnern aktivieren
description: Erfahren Sie mehr über die Aktivierung authentifizierter Zielgruppen mithilfe einer dauerhaften ID-Lösung.
feature: DSP Audiences
source-git-commit: 3059a5b211a8a219b02930f7f5763d5ec1467b8e
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---

# Authentifizierte Segmente von dauerhaften ID-Partnern aktivieren

*Beta-Funktion*

Um authentifizierte Zielgruppen über eine dauerhafte ID-Lösung in Advertising DSP zu aktivieren, müssen Ihre Segmente in [!DNL RampIDs], die in einer bidbaren Umgebung erkennbar sind. Sie können dies erreichen, indem Sie:

* Nutzung der DSP-Integration mit der [!DNL Adobe Real-Time Customer Data Profile (CDP)] und [!DNL Adobe-LiveRamp Retrieval API].

* Manuelles Senden authentifizierter Segmente an DSP von der [!DNL LiveRamp] [!DNL Connect] Dashboard.

## Aufgaben

1. Wenden Sie sich bei beiden Optionen an `adcloud-support@adobe.com` um die folgenden Einstellungen in DSP zu aktivieren, mit denen Sie authentifizierte Segmente in DSP Kampagnen einmal als Ziel auswählen können [alle Schritte im Aktivierungs-Workflow abgeschlossen sind](source-about.md#workflow-sources):

   1. [!DNL LiveRamp] [!DNL RampID] Kampagnenkonfiguration vor der Segmentfreigabe aus [!DNL Real-Time CDP].

   1. Die Kontoebene &quot;[!UICONTROL LiveRamp segments]&quot;.

1. (Benutzer verwenden manuell authentifizierte Segmente aus [!DNL LiveRamp]) Führen Sie die folgenden Schritte im Abschnitt [!DNL LiveRamp] [!DNL Connect] Dashboard:

   1. Zielkachel aktivieren **[!DNL AAC API 1P Onboarding]**.

   1. Satz [!DNL Identifier Settings] nach **[!DNL Ramp ID]** nur.

      ![Identifizierungseinstellungen](/help/dsp/assets/liveramp-tile-settings.png)

   1. (Optional) Wenn Sie weiterhin Cookie-basierte IDs empfangen möchten, erstellen Sie eine zweite [!DNL AAC API 1P Onboarding] Zielkachel mit &quot;[!DNL Cookies], &quot;[!DNL IDFA],&quot; und &quot;[!DNL AAID]&quot;.

## Best Practices für Tests und Datenvalidierung

* **Target [!DNL RampID]-basierte Segmente und Cookie-basierte Segmente in separaten Kampagnen.**

   * In den Kampagneneinstellungen kann nur eine Kennung priorisiert werden.

   * Zurzeit [!DNL RampIDs] nicht während On-site-Ereignissen abgerufen werden können. Das bedeutet, dass bestimmte benutzerdefinierte Ziele wie der niedrigste CPA und der niedrigste ROAS bei der Verwendung authentifizierter Segmente nicht verfügbar sind. Verwenden Sie Cookie-basierte Segmente nur, wenn Sie über eine restriktive Leistungs-KPI verfügen.

* **Erstellen Sie eine Platzierung in beiden [!DNL RampID] und Cookie-basierten Kampagnen.**

   * Targeting der Segmente, die von freigegeben werden [!DNL LiveRamp] Verwendung des standardmäßigen Segmentaktivierungsprozesses.

   * Wenden Sie sich an Ihr Adobe Advertising-Support-Team, um die ordnungsgemäße Datenverteilung zu überprüfen.

Weitere Informationen zur DSP Integration mit [!DNL LiveRamp], Kontakt `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [Informationen zum Aktivieren authentifizierter Segmente aus Zielgruppen-Quellen](source-about.md)
>* [Erstellen einer Zielgruppenquelle zum Aktivieren von Erstanbieterzielgruppen](source-create.md)
>* [Einstellungen der Zielgruppenquelle](source-settings.md)
>* [Adobe Advertising DSP Connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Über Zielgruppen-Management](/help/dsp/audiences/audience-about.md)

