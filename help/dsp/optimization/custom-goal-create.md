---
title: Benutzerdefiniertes Ziel erstellen
description: Benutzerdefiniertes Ziel erstellen
feature: DSP Optimization
exl-id: 440ded21-92d3-41ad-839f-ebc8376aa932
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Benutzerdefiniertes Ziel erstellen

>[!TIP]
>
>Tipps zur Konfiguration Ihrer benutzerdefinierten Ziele finden Sie in den [Best Practices zum Erstellen benutzerdefinierter Ziele](custom-goal-best-practices.md) .

1. Melden Sie sich bei Advertising Cloud Search unter (US-Unternehmen) [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) oder (Unternehmen in allen anderen Ländern) [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com) an.
1. Stellen Sie sicher, dass die Metriken, die Sie in Ihr Ziel aufnehmen möchten, verfolgt wurden, im Produkt verfügbar sind und einen Anzeigenamen enthalten:
   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]**.
   1. Suchen Sie die Metrik und stellen Sie sicher, dass **[!UICONTROL Show in UI and Reports]** für die Metrik aktiviert ist.
   1. Wenn die Metrik keinen Wert in der Spalte **[!UICONTROL Display Name]** hat, klicken Sie in die Zelle, geben Sie den Anzeigenamen ein und klicken Sie dann auf **[!UICONTROL Apply].**.
1. Erstellen Sie das benutzerdefinierte Ziel als *Ziel*:
   1. Klicken Sie im Hauptmenü auf **[!UICONTROL Search]> [!UICONTROL Optimization] >[!UICONTROL Objectives]**.
   1. Klicken Sie in der Symbolleiste auf **[!UICONTROL Create objective].**
   1. Geben Sie die Zieleinstellungen ein:
      1. Geben Sie im Feld **[!UICONTROL Change Objective Name]** den Zielnamen ein.

         Der Zielname wird in der Liste [!UICONTROL Custom Goals] in den Advertising Cloud DSP-Paketeinstellungen angezeigt.

      1. Verknüpfen Sie Eigenschaften mit dem Ziel:

         >[!NOTE]
         >
         > Alle für den Advertiser verfolgten Transaktionseigenschaften sind standardmäßig in der Liste [!UICONTROL Available Properties] aufgeführt.

         * Um eine CSV-Datei mit Eigenschaften und deren Gewichtungen zu importieren, klicken Sie auf **[!UICONTROL Import]** und suchen Sie die zu importierende Datei.

            Die importierten Eigenschaften müssen bereits für den Werber vorhanden sein. Bei den Namen wird nicht zwischen Groß- und Kleinschreibung unterschieden.

            Die importierten Eigenschaften ersetzen alle angegebenen vorhandenen Eigenschaften.

         * Um die erste Eigenschaft mit der Standardgewichtung (1) manuell anzugeben, wählen Sie aus einer Liste aller für den Advertiser verfolgten Transaktionseigenschaften aus.

         * Um manuell eine weitere Eigenschaft mit der Standardgewichtung (1) hinzuzufügen, klicken Sie auf **[!UICONTROL +]** .

            >[!TIP]
            >
            > Um in der Liste nach einer Eigenschaft zu suchen, geben Sie eine Zeichenfolge an einer beliebigen Stelle im Eigenschaftsnamen ein.

         * Um mehrere Eigenschaften manuell hinzuzufügen, klicken Sie auf **[!UICONTROL Add Multiple Properties].** Klicken Sie für jede Eigenschaft, die Sie hinzufügen möchten, auf den Eigenschaftsnamen in der  [!UICONTROL Available Properties] Spalte und ziehen Sie ihn in die  [!UICONTROL Added Properties] Spalte. Wenn Sie alle Eigenschaften hinzugefügt haben, klicken Sie auf **[!UICONTROL Add]**.

            >[!TIP]
            >
            >* Um in der Liste nach einer Eigenschaft zu suchen, geben Sie eine Zeichenfolge von einer beliebigen Stelle im Eigenschaftsnamen im Eingabefeld ein.
            >* Um die Liste so zu filtern, dass Eigenschaften ausgeschlossen werden, die in Berichten ausgeschlossen sind, wählen Sie die Option **[!UICONTROL Hide properties excluded from reports].**


         * (Wenn das Ziel mehrere Eigenschaften enthält) Um die Gewichtung einer Eigenschaft in Bezug auf die anderen Eigenschaften im Ziel zu ändern, geben Sie Werte in die Felder **[!UICONTROL Weight]** ein.
      1. Klicken Sie unten in den Einstellungen auf **[!UICONTROL Save]**.


Nachdem Sie ein Ziel erstellt haben, können Sie es einem Advertising Cloud DSP-Paket als benutzerdefiniertes Ziel zuweisen, wenn das Optimierungsziel &quot;[!UICONTROL Highest ROAS - Custom Goal]&quot;oder &quot;[!UICONTROL Lowest CPA - Custom Goal]&quot;lautet.

>[!TIP]
>
>Für eine optimierte Leistung von <!-- optimum? Or optimization won't happen at all w/out it? -->müssen die kombinierten Metriken im benutzerdefinierten Ziel (Ziel) mindestens 10 Konversionen pro Tag umfassen. Andernfalls empfiehlt es sich, dem Ziel zusätzliche unterstützende Ereignisse (Transaktionseigenschaften) wie Produktseiten oder Anwendungen hinzuzufügen. Richtlinien finden Sie unter [Best Practices zum Erstellen eines benutzerdefinierten Ziels](custom-goal-best-practices.md) .

>[!MORELIKETHIS]
>
>* [Über benutzerdefinierte Ziele](custom-goal-about.md)
>* [Best Practices zum Erstellen eines benutzerdefinierten Ziels](custom-goal-best-practices.md)
>* [Optimierungsziele und Verwendung](optimization-goals.md)
>* [Paketeinstellungen](/help/dsp/campaign-management/packages/package-settings.md)
> * [Wie DSP Ihre Kampagnen optimiert](optimization-how-dsp-optimizes-campaigns.md)

