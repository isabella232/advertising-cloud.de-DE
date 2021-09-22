---
title: Manuelle Deal-ID-Einstellungen
description: Siehe Beschreibungen der Einstellungen für manuell eingegebene Angebots-IDs.
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 0cd5e9e8-2b13-4b1e-a2e0-b8b492f75acf
source-git-commit: d10e1c24ee7c93eaab3fd4fefe853860226cc8e2
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 0%

---

# Manuelle Deal-ID-Einstellungen

| Abschnitt | Parameter | Beschreibung | Erforderlich | Bearbeitbar |
|---------|-----------|-------------|----------|----------|
| [Details zum Geschäft] | [!UICONTROL Deal name] | Der Name, der Ihre [!UICONTROL Deal ID] in Advertising Cloud DSP kennzeichnet. Geben Sie einen Namen ein oder wählen Sie [!UICONTROL Auto-name] aus, damit Advertising Cloud einen Namen basierend auf den Geschäftsdetails generieren kann.<br><br>Beispiel eines automatisch generierten Namens:  [!DNL *DEAL_ID*  - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private] | Ja | Ja |
|  | [!UICONTROL External deal ID] | Die ID, die von Ihrem Herausgeber und der SSP zur Identifizierung dieses Geschäfts verwendet wird. | Ja | Nein |
|  | [!UICONTROL Publisher] | Der Name des Herausgebers, der diesen Bestand verkauft. | Ja | Nein |
|  | [!UICONTROL SSP] | Die angebotsseitige Plattform (Supply Side Platform, SSP), über die diese Vereinbarung durchgeführt wird. | Ja | Nein |
|  | [!UICONTROL Media type] | Die Art der Medien, die durch diesen Deal gekauft werden: [!UICONTROL Desktop video], [!UICONTROL Mobile video], [!UICONTROL Connected TV], [!UICONTROL Display] oder [!UICONTROL Audio]. Die Optionen variieren je nach SSP. | Ja | Nein |
|  | [!UICONTROL Deal type] | Die Deal-Zusage und die Preisstruktur:<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*: Sie und der Herausgeber haben keine feste Anzahl von Impressions-Sendungen durchgeführt. In der Vereinbarung wird der Mindestpreis für das Inventar festgelegt, obwohl der CPM je nach Marktbedingungen schwanken und steigen kann.</li><li>*[!UICONTROL Non guaranteed (fixed)]*: Sie und der Herausgeber haben keine feste Anzahl von Impressions-Sendungen durchgeführt. Die Preisfestsetzung erfolgt zu einem vereinbarten Festpreis.</li><li>*[!UICONTROL Guaranteed (fixed)]*: Sie und der Herausgeber haben eine vordefinierte Anzahl von Impressionen, Targeting, Flugdaten und Festpreisen vereinbart.<br><br><b>Hinweis:</b> Für garantierte Angebote sind Flugdaten und eine bestimmte Anzahl von Impressionen im  [!UICONTROL Tracking] Abschnitt erforderlich. Sie müssen außerdem eine standardmäßige programmgarantierte Platzierung (PG) für das Angebot erstellen und optional das Angebot für andere Platzierungen verwenden.</li></ul> | Ja | Nein |
|  | [!UICONTROL CPM] | Die ausgehandelten Kosten pro Tausend Impressionen (CPM). | Ja | Ja |
|  | [Währung] | Die Währung für das Geschäft.<br><br>Alle SSPs akzeptieren Angebote in USD. Wenn der SSP die Währung für Ihr DSP-Konto akzeptiert, ist diese Währung ebenfalls verfügbar. | Ja | Nein |
|  | [!UICONTROL Billing method] | Alle Deal-IDs sind [!DNL Adobe]-finanziert und -fakturiert. Advertising Cloud zahlt alle verfügbaren Medienanbieter basierend auf der Nutzung, verwaltet Diskrepanzen mit den Anbietern und sendet eine konsolidierte Rechnung an das Konto. Für diese Option fallen zusätzliche Gebühren an, wie auf der Kreditkarte des Kontos angegeben. | Ja | Nein |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | Die E-Mail-Adresse für das Benutzerkonto, das auf den Deal zugreifen kann. | Nein | Ja |
|  | [!UICONTROL Advertisers that can access this deal] | Die spezifischen Advertiser im Konto, die auf diesen Deal zugreifen können.<br><br><b>Hinweis:</b> Sie können den Deal für Advertiser in zusätzlichen Konten aus der  [!UICONTROL Deals] Ansicht freigeben. Klicken Sie in der Zeile &quot;Deal&quot;auf **[!UICONTROL #]**, klicken Sie auf **[!UICONTROL share]** und geben Sie dann den Deal für eine E-Mail-Adresse frei. | Ja | Ja |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | Die Start- und Enddaten für Traffic, der diesen Deal verwendet. Diese Datumsangaben dienen nur zu Tracking-Zwecken und wirken sich nicht auf die Anzeigenbereitstellung aus.<br><br><b>Tipp:</b> In der  [!UICONTROL Inventory] Ansicht  [!UICONTROL Deals] > zeigt die  [!UICONTROL Pacing & Budget] Spalte, wie der Deal zum festgelegten Flugdatum und Impressionsziel gelangt. Wenn der Versand zu kurz oder zu schnell verläuft, wenden Sie sich an Ihren Herausgeber, um die Menge anzupassen, die durch den Deal gesendet wird. | Garantierte Angebote: Ja<br>Nicht garantierte Angebote: Nein | Ja |
|  | [!UICONTROL Impressions] | (Optional für nicht garantierte Angebote) Die geschätzte Anzahl der Impressionen, die Sie mit diesem Deal erwarten. Dieser Wert dient nur zu Tracking-Zwecken. der Herausgeber steuert die Anzeigenbereitstellung. | Garantierte Angebote: Ja<br>Nicht garantierte Angebote: Nein | Ja |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Manuelles Erstellen von Details zur Angebots-ID](deal-id-create.md)
>* [SSP-Partner](ssp-partners.md)

<!-- >* [About Private Inventory](private-inventory-about.md) -->
