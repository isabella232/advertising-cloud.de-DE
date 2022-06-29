---
title: Manuelle Deal-ID-Einstellungen
description: Siehe Beschreibungen der Einstellungen für manuell eingegebene Angebots-IDs.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 0cd5e9e8-2b13-4b1e-a2e0-b8b492f75acf
source-git-commit: 39f491a39bdc9d8dd820eb4c69594dda71d8b3c2
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# Manuelle Deal-ID-Einstellungen

| Abschnitt | Parameter | Beschreibung | Erforderlich | Bearbeitbar |
|---------|-----------|-------------|----------|----------|
| [Details zum Geschäft] | [!UICONTROL Deal name] | Der Name zur Identifizierung Ihrer [!UICONTROL Deal ID] in Advertising Cloud DSP. Geben Sie einen Namen ein oder wählen Sie **[!UICONTROL Auto-name]** , damit Advertising Cloud einen Namen basierend auf den Geschäftsdetails generieren kann.<br><br>Beispiel eines automatisch generierten Namens: `[!DNL 24159708 - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private]` | Ja | Ja |
|  | [!UICONTROL External deal ID] | Die ID, die von Ihrem Herausgeber und der SSP zur Identifizierung dieses Geschäfts verwendet wird. | Ja | Nein |
|  | [!UICONTROL Publisher] | Der Name des Herausgebers, der diesen Bestand verkauft. | Ja | Nein |
|  | [!UICONTROL SSP] | Die angebotsseitige Plattform (Supply Side Platform, SSP), über die diese Transaktion läuft. | Ja | Nein |
|  | [!UICONTROL Media type] | Die Art der Medien, die im Rahmen dieses Geschäfts gekauft wurden: *[!UICONTROL Desktop video]*, *[!UICONTROL Mobile video]*, *[!UICONTROL Connected TV]*, *[!UICONTROL Display]* oder *[!UICONTROL Audio]*. Die Optionen variieren je nach SSP.<br><br> Wenn das Geschäft mehrere Medientypen zulässt, wählen Sie beim Erstellen des Geschäfts den Medientyp für die Standardplatzierung aus. Später können Sie den Wert ändern, oder Sie können [eine neue Platzierung mit dem zusätzlichen Medientyp anhängen](deal-id-attach-placements.md).<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | Ja | Nein |
|  | [!UICONTROL Deal type] | Die Vereinbarung und Preisstruktur:<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*: Sie und der Herausgeber haben keine feste Anzahl von Impressions-Sendungen durchgeführt. In der Vereinbarung wird der Mindestpreis für das Inventar festgelegt, obwohl der CPM je nach Marktbedingungen schwanken und steigen kann.</li><li>*[!UICONTROL Non guaranteed (fixed)]*: Sie und der Herausgeber haben keine feste Anzahl von Impressions-Sendungen durchgeführt. Die Preisfestsetzung erfolgt zu einem vereinbarten Festpreis.</li><li>*[!UICONTROL Guaranteed (fixed)]*: Sie und der Herausgeber haben eine vordefinierte Anzahl von Impressionen, Targeting, Flugdaten und Festpreisen vereinbart.<br><br><b>Hinweis:</b> Garantierte Angebote erfordern Flugdaten und eine bestimmte Anzahl von Impressionen in der [!UICONTROL Tracking] Abschnitt. Sie müssen außerdem eine standardmäßige Platzierung mit programmgesteuerter Garantie (PG) für den Deal erstellen, und Sie können den Deal optional für andere Platzierungen verwenden.</li></ul> | Ja | Nein |
|  | [!UICONTROL CPM] | Die ausgehandelten Kosten pro 1000 Impressionen (CPM). | Ja | Ja |
|  | [Währung] | Die Währung für das Geschäft.<br><br>Alle SSPs akzeptieren Angebote in USD. Wenn der SSP die Währung für Ihr DSP-Konto akzeptiert, ist diese Währung ebenfalls verfügbar. | Ja | Nein |
|  | [!UICONTROL Billing method] | Alle Deal-IDs sind [!DNL Adobe]-finanziert und fakturiert. Advertising Cloud zahlt alle verfügbaren Medienanbieter basierend auf der Nutzung, verwaltet Diskrepanzen mit den Anbietern und sendet eine konsolidierte Rechnung an das Konto. Für diese Option fallen zusätzliche Gebühren an, wie auf der Kreditkarte des Kontos angegeben. | Ja | Nein |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | Die E-Mail-Adresse für das Benutzerkonto, das auf den Deal zugreifen kann. | Nein | Ja |
|  | [!UICONTROL Advertisers that can access this deal] | Die spezifischen Advertiser im Konto, die auf diesen Deal zugreifen können.<br><br><b>Hinweis:</b> Sie können den Deal für Advertiser in zusätzlichen Konten über die [!UICONTROL Deals] anzeigen. Klicken Sie in der Zeile &quot;Deal&quot;auf **[!UICONTROL #]** klicken **[!UICONTROL share]** und geben Sie dann den Deal für eine E-Mail-Adresse frei. | Ja | Ja |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | Die Start- und Enddaten für Traffic, der diesen Deal verwendet. Diese Daten dienen nur zu Tracking-Zwecken und wirken sich nicht auf die Anzeigenbereitstellung aus.<br><br><b>Tipp:</b> Im [!UICONTROL Inventory] > [!UICONTROL Deals] Ansicht, die [!UICONTROL Pacing & Budget] zeigt an, wie der Deal zum festgelegten Flugdatum und Impressionsziel gelangt. Wenn der Versand zu kurz oder zu schnell verläuft, wenden Sie sich an Ihren Herausgeber, um die Menge anzupassen, die durch den Deal gesendet wird. | Garantierte Angebote: Ja<br>Nicht garantierte Angebote: Nein | Ja |
|  | [!UICONTROL Impressions] | (Optional für nicht garantierte Angebote) Die geschätzte Anzahl der Impressionen, die Sie mit diesem Deal erwarten. Dieser Wert dient nur zu Tracking-Zwecken. der Herausgeber steuert die Anzeigenbereitstellung. | Garantierte Angebote: Ja<br>Nicht garantierte Angebote: Nein | Ja |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Manuelles Erstellen von Details zur Angebots-ID](deal-id-create.md)
>* [SSP-Partner](ssp-partners.md)
>* [Über privates Inventar](private-inventory-about.md)

