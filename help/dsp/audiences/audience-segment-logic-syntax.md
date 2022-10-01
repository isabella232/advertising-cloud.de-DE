---
title: Syntax für Zielgruppensegmentlogik
description: Referenzieren Sie die Syntax, die Sie verwenden können, um die Logik für Zielgruppensegmente zu definieren.
feature: DSP Audiences
exl-id: 3a51b1b5-1eef-453b-9be5-0694e27491a8
source-git-commit: efd04189de975f8f075dec7851a3a06d2d647ded
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Syntax für Zielgruppensegmentlogik

Wenn Sie wiederverwendbare Zielgruppen erstellen, können Sie die Segmentlogik mithilfe alphanumerischer Segment-IDs (Schlüssel) und der folgenden Syntax manuell definieren:

* () um eine Gruppe anzugeben
* `||` für [!DNL OR] <!-- || escaped with backticks so Jenkins doesn't think it's a Markdown table -->
* &amp;&amp; für [!DNL AND]
* ! für [!DNL NOT] (ausschließen)

>[!NOTE]
>
>* Alle angegebenen Segmentgruppen sind eingeschlossen, es sei denn, ihnen wird vorangestellt! (der sie ausschließt).
>* Sie können [Segment-ID für eine Zielgruppe suchen](reusable-audience-clipboard.md) von [!UICONTROL Audiences] > [!UICONTROL All audiences].


Beispielsweise die folgende Logik:

```
(X5vUk1cNvZxvBJ3jMjTt) || (sfvXrmQkk77PL5OtHpLH) && !(SMWSjTZFiy9hR1bKm1vw || x08UReA0IcP9HAJdcGVe)
```

bedeutet (in einfachem Englisch)

```
[!DNL INCLUDE] Segment ID X5vUk1cNvZxvBJ3jMjTt [!DNL OR] INCLUDE Segment ID sfvXrmQkk77PL5OtHpLH [!DNL AND EXCLUDE] (Segment ID SMWSjTZFiy9hR1bKm1vw AND Segment ID x08UReA0IcP9HAJdcGVe)
```

>[!NOTE]
>
>In den Platzierungseinstellungen können Sie gespeicherte Zielgruppen entweder als Zielgruppen zum expliziten Targeting oder als separate Zielgruppen verwenden, die vom Targeting ausgeschlossen werden sollen. Stellen Sie sicher, dass Ihre Segmentlogik den Zweck widerspiegelt, für den Sie die Zielgruppe verwenden werden.

>[!MORELIKETHIS]
>
>* [Kopieren Sie den Segmentschlüssel für eine wiederverwendbare Zielgruppe in die Zwischenablage.](reusable-audience-clipboard.md)
>* [Über Zielgruppen-Management](audience-about.md)
>* [Wiederverwendbare Zielgruppe erstellen](reusable-audience-create.md)
>* [Zielgruppeneinstellungen](audience-settings.md)
>* [Verfügbare Drittanbieter von Daten](third-party-data-providers.md)

