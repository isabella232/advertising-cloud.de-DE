---
title: Fehlercodes für [!DNL FreeWheel] Anzeigenübermittlungen
description: Verweisen Sie auf die Fehlercodes, die für Anzeigenübermittlungen an  [!DNL FreeWheel] zurückgegeben werden.
feature: Private Inventory, Deal IDs
exl-id: null
source-git-commit: 185fc7d79798a0a3a9ad5829b701aeb53a4a47c1
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 2%

---

# Fehlercodes für [!DNL FreeWheel] Anzeigenübermittlungen

Die Fehlermeldungen für fehlgeschlagene Anzeigenübermittlungen können entweder von Advertising Cloud DSP oder von [!DNL FreeWheel] stammen. Fehlermeldungen werden in der Spalte [!UICONTROL API Response] im [[!UICONTROL Freewheel Status]-Dialogfeld](freewheel-check-status.md) angezeigt.

## Interne Advertising Cloud DSP-Fehler

| Fehlermeldung | Beschreibung | Nächste Schritte |
|--- |--- |--- |
| [!DNL Warte auf Statusantwort von [!DNL FreeWheel]] | [!DNL FreeWheel] hat noch nicht geantwortet, dass die Übermittlung erfolgreich war oder fehlgeschlagen war. | Überprüfen Sie den Status in 10 Minuten erneut. |
| [!DNL The submitted ad does not have a clock number assigned.] | [!DNL FreeWheel] akzeptiert keine britischen Anzeigen ohne zugewiesene Uhrennummern. | Weisen Sie der Anzeige eine Uhrennummer zu und senden Sie sie dann erneut. |
| [!DNL The ad you are attempting to submit has not yet finished transcoding. Please wait ten minutes then try again.] | Der Transcoder hatte die Transkodierung der Anzeige noch nicht abgeschlossen, als Sie versuchten, die Anzeige zu senden. | Warten Sie zehn Minuten und senden Sie die Anzeige dann erneut. |
| [!DNL The deal id you input is not setup as a guaranteed feed. Please submit guaranteed deals only.] | Das eingereichte Geschäft ist nicht als programmgesteuertes garantiertes Geschäft eingerichtet. [!DNL FreeWheel] akzeptiert nur garantierte Angebote. | Richten Sie die Deal-ID als programmgesteuertes garantiertes Deal ein. Die Anzeige wird automatisch an [!DNL FreeWheel] gesendet, wenn Sie die programmgarantierte Standardplatzierung am Ende des Deal-ID-Workflows speichern. |
| [!DNL Invalid external_deal_id:] \&lt;deal_id> | Die gesendete Deal-ID existiert entweder nicht oder ist auf der Adobe-Seite nicht aktiv. | Stellen Sie sicher, dass der Deal aktiv ist, und senden Sie die Anzeige dann erneut. |
| [!DNL \[public_id=]\&lt;deal>] ist nicht vorhanden | Die gesendete Deal-ID existiert nicht am [!DNL FreeWheel]-Ende. | Wenden Sie sich an Ihren [!DNL FreeWheel]-Support-Mitarbeiter, um die Deal-ID zu bestätigen. |
| [!DNL Ad with identifier] \&lt;>Anzeigenname *\>  [!DNL was not found.]* | Der gesendete Anzeigenschlüssel ist entweder nicht vorhanden oder auf dem Adobe-Ende nicht aktiv. | Suchen Sie den richtigen Anzeigenschlüssel und senden Sie die Anzeige dann erneut. |
| [!DNL Pending Submission] | Die Übermittlung steht noch aus. | Aktualisieren Sie die Seite. |

{style=&quot;table-layout:auto&quot;}

## FreeWheel-API-Fehler

| Code | Bedeutung | Beschreibung | Nächste Schritte |
|--- |--- |--- |--- |
| 401 | Unerlaubt | Falsche, fehlende oder ungültige Zugriffsberechtigungen. | Wenden Sie sich an Ihren Adobe Account Manager. |
| 403 | Verboten | Der Server hat die Anfrage verstanden, weigert sich jedoch, sie zu autorisieren. | Wenden Sie sich an Ihren Adobe Account Manager. |
| 404 | Nicht gefunden | Die angeforderte Ressource ist nicht verfügbar. Wenn die Creative-ID im PUT-Vorgang nicht gefunden wird, wird ein 404-Fehler zurückgegeben. | Wenden Sie sich an Ihren Adobe Account Manager. |
| 405 | Methode nicht zulässig | Eine Ressourcenanforderung erfolgte mithilfe einer Anforderungsmethode, die von dieser Ressource nicht unterstützt wurde (z. B. mithilfe von GET für eine Methode, bei der Daten über eine POST gesendet werden müssen, oder mittels PUT für eine schreibgeschützte Ressource). | Wenden Sie sich an Ihren Adobe Account Manager. |
| 408 | Anfrage-Timeout | Während der Verarbeitung dieser Anfrage trat eine Zeitüberschreitung auf. Timeouts werden in der Regel durch gleichzeitige Anforderungen an den ausschließlichen Zugriff auf bestimmte Ressourcen verursacht. | Senden Sie die Anfrage erneut, wenn Sie diesen Status erhalten. Wenn das Problem weiterhin besteht, wenden Sie sich an Ihren Kundenbetreuer von Adobe. |
| 422 | Nicht verarbeitbare Entität | Ungültige Ressource. Dieser Fehler tritt auf, wenn der Anfragetext ungültig ist oder die erstellte/aktualisierte Ressource ungültig ist (z. B. wenn die Angebots-ID nicht gefunden wurde). Weitere Informationen finden Sie unter [FreeWheel API 422 Errors](#freewheel-422-errors) . | Wenden Sie sich an Ihren Adobe Account Manager. |
| 500 | Interner Server-Fehler | API-Systemfehler. | Wenden Sie sich an Ihren Adobe Account Manager. |

{style=&quot;table-layout:auto&quot;}

## Fehler der FreeWheel API 422 {#freewheel-422-errors}

| Code | HTTP-Code | Beschreibung |
|--- |--- |--- |
| DATA_UNMARSHALL_FAILURE | 422 | Die Anfragedaten sind ein ungültiges JSON-Format. Weitere Informationen finden Sie in der Fehlermeldung. |
| DATA_VALIDATION_FAILURE | 422 | Die Anfragedaten fehlen erforderliche Felder oder weisen einen ungültigen Datentyp auf. Weitere Informationen finden Sie in der Fehlermeldung. |
| DATA_DEAL_INVALID | 422 | Der Deal ist falsch konfiguriert oder existiert nicht. Weitere Informationen finden Sie in der Fehlermeldung. |
| DATA_DEAL_GET_FAILURE | 422 | Die Vereinbarung wurde nicht gefunden oder ihre Konfiguration hat ein Problem. Weitere Informationen finden Sie in der Fehlermeldung. |
| DATA_CREATIVE_INGEST_FAILURE | 422 | Die Kreativ-URL ist ungültig. Weitere Informationen finden Sie in der Fehlermeldung. |
| DATA_CREATIVE_LINK_FAILURE | 422 | Der Kreativelement war nicht mit den Anzeigeneinheiten-Knoten des Geschäfts verknüpft. Weitere Informationen finden Sie in der Fehlermeldung. |
| DATA_CREATIVE_UPDATE_FAILURE | 422 | Das Kreativ wurde nicht aktualisiert. Weitere Informationen finden Sie in der Fehlermeldung. |
| DATA_DSP_GET_FAILURE | 422 | Die DSP existiert nicht im System. |
| DATA_CREATIVE_UNLINK_FAILURE | 422 | Die Verknüpfung des Kreativen mit den Anzeigen-Einheiten wurde nicht aufgehoben. |
| DATA_CREATIVE_DELETE_FAILURE | 422 | Das Kreativ wurde nicht gelöscht. |
| DATA_CREATIVE_DETECTION_FAILURE | 422 | Die URL wurde nicht erkannt. |
| DATA_ENTITY_NOT_FOUND | 422 | Die Kreativelemente existieren nicht. |

{style=&quot;table-layout:auto&quot;}

>[!MORELIKETHIS]
>
>* [Übersicht über die Einrichtung programmgesteuerter Garantiegeschäfte in FreeWheel](/help/dsp/inventory/freewheel-overview.md)
>* [Akzeptieren eines Angebots im Deal-ID-Posteingang](deal-id-inbox-accept.md)
>* [Senden einer Anzeige für einen programmgesteuerten garantierten Deal an FreeWheel](/help/dsp/inventory/freewheel-submit.md)
>* [Überprüfen des Status von Anzeigen  [!DNL FreeWheel] für programmgesteuerte garantierte Angebote](/help/dsp/inventory/freewheel-check-status.md)

