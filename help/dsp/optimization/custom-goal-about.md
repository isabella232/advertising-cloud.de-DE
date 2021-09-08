---
title: Über benutzerdefinierte Ziele
description: Erfahren Sie mehr über benutzerdefinierte Ziele, um Ihre Erfolgsereignisse in Paketen zu definieren, die für den niedrigsten CPA oder den höchsten ROAS optimiert sind.
feature: Optimization
exl-id: 623cb1ef-85ab-4535-aa3a-8e6ec8ae15ee
source-git-commit: 0f0a2e907d39900968b29c3b59c8034b604911ce
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# Über benutzerdefinierte Ziele

Benutzerdefinierte Ziele definieren die Erfolgsereignisse, die ein Advertiser benötigt, um seine Geschäftsziele zu erreichen. Jedes Paket, das die Optimierungsziele &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot;oder &quot;[!UICONTROL Lowest CPA - Custom Goal]&quot;verwendet, muss ein benutzerdefiniertes Ziel enthalten, das dazu beiträgt, das Gesamtoptimierungsziel zu erreichen. Sie können benutzerdefinierte Ziele als *Ziele* in Advertising Cloud Search erstellen.

![benutzerdefinierte Ziele](/help/dsp/assets/objective-goals.png)

Jedes benutzerdefinierte Ziel besteht aus einer oder mehreren Metriken oder *Transaktionseigenschaften* und den relativen Gewichtungen dieser Transaktionseigenschaften. Zu den verfügbaren Transaktionseigenschaften gehören alle Metriken, die mit dem Advertising Cloud-Konversionspol und über Adobe Analytics verfolgt werden.

>[!NOTE]
>
>* [!DNL Analytics] -Dimensionen und -segmente stehen nicht zur Advertising Cloud-Optimierung zur Verfügung.
>* Um Analytics-Ereignisse in DSP zu verwenden, konfigurieren Sie mit Ihrem Adobe-Kundenbetreuer eine Integration auf Advertiser-Ebene.
>* [!DNL Analytics] Benutzerdefinierte Ereignisse folgen dieser Benennungskonvention:  `custom_event_[*event #*]_[*Analytics report suite ID*]`. Beispiel: `custom_event_16_examplersid`


Angenommen, drei Metriken (Transaktionseigenschaften) sind für ein bestimmtes Paket in einer Ihrer Kampagnen relevant: &quot;PDF Download&quot; im Wert von 20 USD, &quot;E-Mail-Anmeldung&quot; im Wert von 30 USD und &quot;Auftragsbestätigung&quot; im Wert von 40 USD. Wenn Sie Gewichtung gemäß dem einmaligen Geldwert der Kundenaktion geben möchten, beträgt das relative Gewicht der Eigenschaften 1, 2 und 1.5.

Tipps zur Konfiguration Ihrer benutzerdefinierten Ziele finden Sie in den [Best Practices zum Erstellen benutzerdefinierter Ziele](custom-goal-best-practices.md) .

Nachdem Sie [ein benutzerdefiniertes Ziel](custom-goal-create.md) erstellt haben, können Sie [es einem Paket](/help/dsp/campaign-management/packages/package-settings.md) zuweisen, um Berichte und algorithmische Optimierungen mit Adobe Sensei zu erstellen.

>[!MORELIKETHIS]
>
>* [Benutzerdefiniertes Ziel erstellen](custom-goal-create.md)
>* [Best Practices zum Erstellen eines benutzerdefinierten Ziels](custom-goal-best-practices.md)
>* [Optimierungsziele und Verwendung](optimization-goals.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
> * [Wie DSP Ihre Kampagnen optimiert](optimization-how-dsp-optimizes-campaigns.md)

