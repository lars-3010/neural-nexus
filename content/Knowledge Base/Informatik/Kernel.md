Tags: #🌿 
up:: [[../../Maps of Content/Computing Infrastructure|Computing Infrastructure]]

---
Der Kernel ist der Kern des Betriebssystems und bildet dessen Herzstück.

Funktionen:

- Direkter Zugriff auf die Hardware
- Speicherverwaltung auf niedrigster Ebene
- CPU-Scheduling
- Interrupt-Handling
- Prozess- und Thread-Management

# Zusammenhänge
---
Zusammenfassend lässt sich sagen, dass der Kernel als zentraler Bestandteil des Betriebssystems die grundlegenden Mechanismen für die Verwaltung von Prozessen und Threads bereitstellt. Er bildet die Basis, auf der komplexere Konzepte wie Thread Pools aufbauen, und sorgt für die effiziente und sichere Nutzung der Systemressourcen durch verschiedene Anwendungen.
## OS, Kernel und Prozesse:
---
- Der Kernel erstellt und verwaltet Prozesse.
- Jeder Prozess erhält vom Kernel einen eigenen virtuellen Adressraum.
- Der Kernel plant die Ausführung von Prozessen auf der CPU (Scheduling).

## OS, Kernel und Threads:
---
- Der Kernel unterstützt auch die Erstellung und Verwaltung von Threads.
- Threads innerhalb eines Prozesses teilen sich den vom Kernel zugewiesenen Adressraum.
- Der Kernel plant auch die Ausführung einzelner Threads (Thread-Scheduling).

## Kernel und Ressourcenverwaltung:
---
- Der Kernel kontrolliert den Zugriff auf Systemressourcen.
- Er stellt sicher, dass Prozesse nur auf ihren eigenen Speicherbereich zugreifen können.
- Er verwaltet den Zugriff auf gemeinsam genutzte Ressourcen wie Dateien oder Netzwerkverbindungen.

## Kernel und Thread Pools:
---
- Thread Pools werden oft von Anwendungen oder Frameworks implementiert, aber der Kernel bietet die grundlegenden Mechanismen für deren Funktionsweise.
- Der Kernel plant die Ausführung der Threads im Pool, auch wenn er nicht direkt den Pool verwaltet.

## Sicherheit und Isolation:
---
- Der Kernel stellt sicher, dass Prozesse voneinander isoliert sind.
- Er implementiert Schutzmechanismen, um zu verhindern, dass ein Prozess auf den Speicher eines anderen zugreift.

##  Systemaufrufe:
---
- Prozesse und Threads kommunizieren mit dem Kernel über Systemaufrufe.
- Diese Aufrufe ermöglichen es Anwendungen, Dienste des Betriebssystems zu nutzen, ohne direkten Zugriff auf die Hardware zu haben.

## Kontext-Switching:
---
- Der Kernel ist verantwortlich für das Umschalten zwischen verschiedenen Prozessen und Threads (Kontext-Switching).
- Dies ermöglicht Multitasking und die effiziente Nutzung der CPU.


# Note Structure
### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 

### Sources:
---
