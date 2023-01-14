---
source-git-commit: ad978a021c063377e4c91ed41e902d98a03749e4
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---
# Gemeinsame Dokumentation für Adobe Advertising

Dies ist das Dokumentations-Repository für Adobe Advertising, einschließlich produktübergreifender und DSP Dokumente. (Später werden Dokumente für die Suche und möglicherweise (?) für Kreativ.)

**Hinweis: Diese Seite wird nicht in der kundenorientierten Dokumentation veröffentlicht.**

## TOC

+ `TOC.md` im Stammverzeichnis eines Benutzerhandbuchs finden Sie die Organisation der Themen, die im Handbuch enthalten sind.
+ Jedes Benutzerhandbuch verfügt über eine eindeutige `TOC.md`, in dem Sie alle Seiten/Themen nach Bedarf sortieren können.


## Benutzerhandbuch

+ Die Einführung in das Benutzerhandbuch finden Sie unter `overview.md`
+ Jedes Thema im Benutzerhandbuch verfügt über ein eigenes Verzeichnis.
   + Wenn ein Thema im Handbuch mit dem Namen *Implementierung*, lautet das entsprechende Verzeichnis . `/implementation`
+ Alle Bild-Assets werden in `/assets` im Stammverzeichnis des Benutzerhandbuchs.
   + Alle Bilder in `/assets` wird lokalisiert.
   + Alle Bilder in `/no-localize` -Verzeichnis nicht lokalisiert (es gibt eine Überraschung!). Dies kann verwendet werden, um in lokalen Versionen sicherzustellen, dass bestimmte Assets nicht unnötig reproduziert werden.

## Metadaten auf Benutzerhandbuchebene

+ Metadaten, die das Benutzerhandbuch beschreiben, werden im Abschnitt `TOC.md`. Dazu gehören:
   + product - Name des Produkts/der Funktion.
   + cloud - Cloud, zu der dieses Produkt gehört.
   + audience - Zielgruppe oder Archetyp, auf den das Handbuch ausgerichtet ist.
   + user-guide - Name des Benutzerhandbuchs.

## Metadaten auf Seitenebene

+ Metadaten, die zur Beschreibung eines Dokuments erforderlich sind, werden als Teil jeder einzelnen Seite gespeichert. Dazu gehören:
   + title - Titel der Seite
   + description - Beschreibung der Seite
   + seo-title - alternative Seo-Bezeichnung
   + seo-description - Alternativtitel für SEO-Zwecke
   + short-title - (optionales Feld)
   + index - ja/nein - wird die Seite durch die Suchplattform der Adobe indexiert?
   + translate - ja/nein - Wird diese Seite lokalisiert?
   + beta - Ist dieses Produkt in der Beta-Phase?
   + redirect - kann verwendet werden, um bei Bedarf eine Referenz zu einer neuen Seite zu erstellen
   + doc-type: reference (Standard) / troubleshooting/developer/tutorial/kb/whitepaper

## Weitere Informationen

Weitere Veröffentlichungsanweisungen, Stilhandbücher, Beispiele und andere Ressourcen finden Sie unter:

+ [Beiträge zu Autorenrichtlinien **speziell für Adobe Advertising**](https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=EfficientFrontier&amp;title=Contributing+Author+Guidelines+for+Advertising+Cloud+Help)
+ [Gemeinschaftliches Authoring für alle Autoren von Adoben](https://experienceleague.adobe.com/docs/authoring-guide-exl/using/home.html)

Siehe auch:

+ contributing.md Ein Überblick darüber, wie Sie zur Dokumentation beitragen.

<!-- * guidelines.md For an overview on what is expected in contributions and how to compose your documentation contributions. -->
+ code-of-conduct.md Ein Überblick über die Verhaltensstandards, die wir erwarten, wenn Sie zu diesem Dokumentationsprojekt beitragen.
