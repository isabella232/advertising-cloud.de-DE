---
title: Über benutzerdefinierte Ziele
description: Erfahren Sie mehr über benutzerdefinierte Ziele, um Ihre Erfolgsereignisse in Paketen zu definieren, die für den niedrigsten CPA oder den höchsten ROAS optimiert sind.
feature: DSP Optimization
exl-id: 623cb1ef-85ab-4535-aa3a-8e6ec8ae15ee
source-git-commit: ad4ab8b9b0a4b5b1cc4aab540900363d2fe671c2
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---

# Über benutzerdefinierte Ziele

Benutzerdefinierte Ziele definieren die Erfolgsereignisse, die ein Advertiser benötigt, um seine Geschäftsziele zu erreichen. Jedes Paket, das die Optimierungsziele verwendet &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot; oder &quot;[!UICONTROL Lowest CPA - Custom Goal]&quot; muss ein benutzerdefiniertes Ziel enthalten, das dazu beiträgt, das allgemeine Optimierungsziel zu erreichen. Sie können benutzerdefinierte Ziele als *Ziele* in [!DNL Adobe Advertising Search].

![benutzerdefinierte Ziele](/help/dsp/assets/objective-goals.png)

Jedes benutzerdefinierte Ziel besteht aus einer oder mehreren Metriken oder *Transaktionseigenschaften* und die relative Gewichtung dieser Transaktionseigenschaften. Die verfügbaren Transaktionseigenschaften umfassen alle Metriken, die mit dem Adobe Advertising Conversion-Pixel und über Adobe Analytics verfolgt werden.

>[!NOTE]
>
>* [!DNL Analytics] -Dimensionen und -segmente stehen nicht zur Adobe Advertising-Optimierung zur Verfügung.
>* Wenn Sie Analytics-Ereignisse in DSP verwenden möchten, arbeiten Sie mit Ihrem [!DNL Adobe] Account-Team , um eine Integration auf Advertiser-Ebene zu konfigurieren.
>* [!DNL Analytics] Benutzerdefinierte Ereignisse folgen dieser Benennungskonvention: `custom_event_[*event #*]_[*Analytics report suite ID*]`. Beispiel: `custom_event_16_examplersid`


Angenommen, drei Metriken (Transaktionseigenschaften) sind für ein bestimmtes Paket in einer Ihrer Kampagnen relevant: &quot;PDF Download&quot; im Wert von 20 USD, &quot;E-Mail-Anmeldung&quot; im Wert von 30 USD und &quot;Auftragsbestätigung&quot; im Wert von 40 USD. Wenn Sie Gewichtung gemäß dem einmaligen Geldwert der Kundenaktion geben möchten, beträgt das relative Gewicht der Eigenschaften 1, 2 und 1.5.

Siehe [Best Practices zum Erstellen benutzerdefinierter Ziele](custom-goal-best-practices.md) Tipps zur Konfiguration Ihrer benutzerdefinierten Ziele.

Einmal [Erstellen eines benutzerdefinierten Ziels](custom-goal-create.md)können Sie [Zuweisen zu einem Paket](/help/dsp/campaign-management/packages/package-settings.md) für die Berichterstellung und algorithmische Optimierung mit Adobe Sensei.

>[!MORELIKETHIS]
>
>* [Benutzerdefiniertes Ziel erstellen](custom-goal-create.md)
>* [Best Practices zum Erstellen eines benutzerdefinierten Ziels](custom-goal-best-practices.md)
>* [Optimierungsziele und Verwendung](optimization-goals.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
> * [Wie DSP Ihre Kampagnen optimiert](optimization-how-dsp-optimizes-campaigns.md)

