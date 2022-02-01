---
title: Über benutzerdefinierte Berichte
description: Erfahren Sie mehr über die Optionen zum manuellen Erstellen benutzerdefinierter Berichte oder zum Verwenden vorkonfigurierter Berichtsvorlagen.
feature: DSP Custom Reports
exl-id: 59fc1894-1c9d-451d-b644-5640dd311547
source-git-commit: b40c6f08b94e546e5fc068c46b279292a4d8a14f
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---

# Über benutzerdefinierte Berichte

Mit benutzerspezifischen Berichten können Sie den Inhalt und die Bereitstellung Ihrer Berichtsdaten mithilfe der Kampagnendimensionen (wie Advertiser, Platzierung, Sites oder Geos) und den Metriken anpassen, die für Sie am wichtigsten sind. Sie haben folgende Möglichkeiten:

* Detaillierte Konfiguration der Berichte zur Kampagnenleistung.
* Wählen Sie aus vorkonfigurierten Berichtvorlagen aus und passen Sie diese optional weiter an.

Sie können Berichte einmal generieren oder planen, dass sie in der angegebenen Zeitzone täglich, wöchentlich oder monatlich um 03:00 Uhr generiert werden. Sobald ein Bericht generiert wurde, wird er an jeden angegebenen E-Mail-Empfänger oder an einen Link gesendet [Berichtsziele](/help/dsp/reports/report-destinations/report-destination-about.md) der folgenden Typen:

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* SFTP
* FTP-SSL (in der Beta-Version)

>[!NOTE]
>
>Sie können On-Demand-Daten auch auf allen Ebenen einer Kampagne anzeigen (Kampagne, Paket, Platzierung oder Anzeige) [in der entsprechenden Kampagnenverwaltungsansicht](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## Verfügbare Berichtstypen

* **[!UICONTROL Custom]:** Dieser Bericht ist eine leere Vorlage, mit der Sie Ihren eigenen benutzerspezifischen Bericht mit den meisten Dimensionen und Metriken erstellen können. [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo]und [!UICONTROL Site] -Berichte sind Varianten dieser Vorlage mit vorausgewählten Spalten und Dimensionen für die jeweiligen Anwendungsfälle.

* Vorkonfigurierte Berichtsvorlagen

   * **[!UICONTROL Billing]:** Verwenden Sie diesen Bericht, um wichtige Abrechnungsmetriken zu verstehen, wie z. B. Ausgabenmetriken für die Medienabrechnung nach Kampagne.

      >[!NOTE]
      >
      >Dieser Bericht enthält Daten zum Rechnungsstellungssegment. Wenn einem Benutzer oder Gerät eine Impression gezeigt wird, die zu mehreren Segmenten gehört, wird nur einem abrechnungsfähigen Segment die Impression gutgeschrieben.

   * **[!UICONTROL Conversion]:** Verwenden Sie diesen Bericht, um zu verstehen, wie Ihre Kampagnen auf der Grundlage von Konversionsmetriken funktionieren, die mit dem Advertising Cloud-Konversions-Tracking erfasst wurden. Dieser Bericht enthält die Mehrfachkontaktattribution.

   * **[!UICONTROL Device]:** Verwenden Sie diese vorausgefüllte Vorlage, um Schlüsselmetriken nach gerätebezogenen Dimensionen anzuzeigen.

   * **[!UICONTROL Frequency (by Impression)]:** Verwenden Sie diesen Bericht, um die Verteilung der Impressionen zu verstehen, die Unique Viewers angezeigt werden (z. B. die Anzahl der Unique Viewers, die eine Impression, zwei Impressionen, drei Impressionen usw. gesehen haben). Die Daten sind nach Platzierung oder Kampagne verfügbar.

      >[!NOTE]
      >
      >* Daten sind nach dem 1. März 2019 verfügbar.
      >* Die Häufigkeit wird anhand einer Datenstichprobe geschätzt.
      >* Für einige Bestände übermitteln Herausgeber keine Geräte-ID, was das Frequenztracking verhindert. Dieser Bericht enthält nur Impressionen, für die eine Geräte-ID verfügbar war.


   * **[!UICONTROL Frequency (by App/Site)]:** Verwenden Sie diesen Bericht, um zu verstehen, wie viele Unique Users über die App oder die Site erreicht wurden. Sie können auch sehen, wie viele Unique Users nur über eine bestimmte App oder Site erreicht wurden (&quot;Unique Users&quot;).

      >[!NOTE]
      >
      >* Daten sind nach dem 15. November 2018 verfügbar.
      >* Bei einigen privaten Beständen geben Herausgeber keine Geräte-ID weiter, was die Frequenzverfolgung verhindert.


   * **[!UICONTROL Geo]**: Verwenden Sie diese vorausgefüllte Vorlage, um Schlüsselmetriken nach geografischen Dimensionen anzuzeigen.

   * **[!UICONTROL Margin]:** Verwenden Sie diesen Bericht, um wichtige Metriken wie Marge, Gewinn und andere Ausgabenmetriken nach Kampagne oder Platzierung anzuzeigen.

   * **[!UICONTROL Segment]:** Verwenden Sie diese vorausgefüllte Vorlage, um Schlüsselmetriken nach Segment anzuzeigen.

      >[!NOTE]
      >
      >* Dieser Bericht soll zeigen, wie unterschiedliche Zielsegmente funktionieren. Es verwendet Daten zur Segmentmitgliedschaft. Wenn eine Impression einer Person oder einem Gerät bereitgestellt wird, die zu zwei oder mehr Zielsegmenten gehört, enthält dieser Bericht für jedes Segment eine Zeile. Aus diesem Grund stimmen die Summen in diesem Bericht möglicherweise nicht mit dem tatsächlichen Versand überein.
      >* Konversionsmetriken und benutzerdefinierte Zieldaten für Segmente sind nach dem 2. August 2019 verfügbar. Alle anderen Daten für Segmente sind ab dem 1. Juni 2018 verfügbar.


   * **[!UICONTROL Site]:** Standardmäßig enthält Standardmetriken, die Gesamtnettoausgaben der Medien und die gesamten abrechnungsfähigen Nettoausgaben pro Site.

## Kontoübergreifende Berichterstellung {#cross-account-reporting}

Jede Organisation mit mehreren DSP-Konten kann je nach den Anforderungen der Organisation in benutzerdefinierten Berichten optional kontoübergreifende Daten aktivieren. Sie können beispielsweise Konto A Zugriff auf die Daten von Konto B gewähren und Konto B Zugriff auf die Daten von Konto C gewähren (jedoch nicht auf Konto As). Wenden Sie sich zur Aktivierung und Konfiguration dieser Funktion an Ihren [!DNL Adobe] Account-Team.

Sobald die Funktion für Ihre Organisation aktiviert wurde, können Sie [filter](report-settings.md) einen der folgenden Berichtstypen nach Konto:  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)]und [!UICONTROL Conversion].

Ihre Kontoeinstellungen unter [!UICONTROL Settings] > [!UICONTROL Account] a) die anderen Konten, deren Daten für Ihr Konto verfügbar sind, und b) die anderen Konten, die auf die Daten Ihres Kontos zugreifen können.

>[!MORELIKETHIS]
>
>* [Benutzerspezifischen Bericht erstellen](/help/dsp/reports/report-create.md)
>* [Benutzerdefinierte Berichtseinstellungen](/help/dsp/reports/report-settings.md)
>* [Über In-Platform-Berichte](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [Verfügbare Berichtsspalten](/help/dsp/reports/report-columns.md)
>* [Info [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)

