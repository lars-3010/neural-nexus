Tags: #🌿 
up:: [[../../Maps of Content/Computing Infrastructure|Computing Infrastructure]]

---
kleinste Einheit der CPU-Nutzung
leichtgewichtiger Prozess innerhalb eines Prozesses

### Verhältnis zu Prozessen:
---
- Threads existieren innerhalb eines Prozesses
- Mehrere Threads können sich den Adressraum und Ressourcen eines Prozesses teilen
- Jeder Thread hat seinen eigenen Ausführungszustand und Stack

### Vorteile
---
- Schnellere Erstellung und Kontextwechsel als bei Prozessen
- Effiziente Kommunikation durch gemeinsamen Speicher

### Nachteile
---
- Erfordern sorgfältige Synchronisation
- Fehler in einem Thread können den gesamten Prozess beeinträchtigen

### Anwendungsfälle
---
- Webbrowser: Separate Threads für UI, Netzwerkkommunikation, Rendering
- Textverarbeitungsprogramme: Separate Threads für Eingabe, Rechtschreibprüfung, Autospeichern

## Vergleich zwischen Prozessen und Threads
---
- Ressourcennutzung: Prozesse haben eigene Ressourcen, Threads teilen Ressourcen
- Kommunikation: Inter-Prozess-Kommunikation ist komplexer als Inter-Thread-Kommunikation
- Stabilität: Fehler in einem Prozess beeinflussen andere Prozesse weniger als Fehler in Threads
- Skalierbarkeit: Threads sind leichtgewichtiger und skalieren besser für parallele Aufgaben auf Multicore-Systemen

## Thread Pools
---
- Effizienter für das OS: Es muss nicht ständig neue Threads erstellen und zerstören.
- Bessere Ressourcenkontrolle: Die Anzahl der gleichzeitig aktiven Threads ist begrenzt.
- Verbesserte Leistung: Wiederverwendung von Threads reduziert Overhead.


# Note Structure
### Relation
---
- **Where from**: 
- **Similar**: 
- **Leads to**: [[Prozesse]]
- **Opposite**: 

### Sources:
---
