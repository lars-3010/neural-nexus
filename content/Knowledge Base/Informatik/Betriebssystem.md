Tags: #🌿 
up:: [[../../Maps of Content/Computing Infrastructure|Computing Infrastructure]]

---
Das Betriebssystem ist die fundamentale Software, die die Hardware eines Computers verwaltet und eine Schnittstelle zwischen Hardware und Anwendungssoftware bietet.

- Kern des Betriebssystem: [[Kernel]]
- 

## Hauptaufgaben
---
- Ressourcenverwaltung (CPU, Speicher, Geräte)
- Prozessverwaltung
- Speicherverwaltung
- Dateisystemverwaltung
- Bereitstellung von Benutzerschnittstellen


# Threads & Prozesse: Beispiel
---
Vorstellung: Betriebssystem als eine große Baustelle:

- Prozesse sind wie einzelne Gebäude auf dieser Baustelle.
- Threads sind wie die Arbeiter innerhalb dieser Gebäude.

Das Betriebssystem (OS) als Bauleiter:

- Weist jedem Gebäude (Prozess) ein Grundstück (Speicherbereich) zu.
- Sorgt dafür, dass die Arbeiter (Threads) nur in ihrem zugewiesenen Gebäude (Prozess) arbeiten.

## Threads vs. Prozesse
---
- Einen neuen Prozess zu erstellen ist wie ein neues Gebäude zu errichten - aufwendig und ressourcenintensiv.
- Einen neuen Thread zu erstellen ist wie einen neuen Arbeiter in ein bestehendes Gebäude zu schicken - schneller und effizienter.

## Thread Pools
---
Ein Thread Pool ist wie ein Aufenthaltsraum für Arbeiter (Threads) in einem Gebäude (Prozess):
- Es gibt eine festgelegte Anzahl von Arbeitern, die bereit stehen.
- Wenn eine Aufgabe ankommt, greift sich ein freier Arbeiter die Aufgabe.
- Nach Erledigung der Aufgabe kehrt der Arbeiter in den Aufenthaltsraum zurück.
- Wenn alle Arbeiter beschäftigt sind, warten neue Aufgaben in einer Warteschlange.

### Vorteile des Thread Pools:
---
- Effizienter für das OS: Es muss nicht ständig neue Threads erstellen und zerstören.
- Bessere Ressourcenkontrolle: Die Anzahl der gleichzeitig aktiven Threads ist begrenzt.
- Verbesserte Leistung: Wiederverwendung von Threads reduziert Overhead.

1. Freiheit und Einschränkungen

- Threads sind innerhalb ihres Prozesses frei: Sie können verschiedene Aufgaben übernehmen, ähnlich wie Arbeiter in einem Gebäude verschiedene Tätigkeiten ausführen können.
- Aber: Sie sind auf ihren Prozess beschränkt, genau wie Arbeiter das Gebäude nicht verlassen können, um in einem anderen zu arbeiten.

## Bauplan-Analogie
---
Der Thread Pool kann tatsächlich mit einem Bauplan verglichen werden:

- Er definiert, wie viele "Arbeiter" (Threads) zur Verfügung stehen.
- Er legt fest, wie Aufgaben verteilt und bearbeitet werden.
- Er stellt sicher, dass Ressourcen effizient genutzt werden.

Zusammenfassend lässt sich sagen, dass Thread Pools eine Art "Arbeitsplan" für die effiziente Nutzung von Threads innerhalb eines Prozesses darstellen. Sie helfen dem Betriebssystem, Ressourcen zu sparen und die Leistung zu optimieren, indem sie eine kontrollierte Umgebung für die parallele Ausführung von Aufgaben bereitstellen.


# Note Structure
### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 

### Sources:
---
