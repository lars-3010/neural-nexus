


## Programmiersprachen
>zählt als Programmiersprache, wenn es das Turing Problem lösen kann
>ständig neue Sprachen
>für Spezialisierung
>Python wichtigste aktuell
>Integer, Bedingung & Schleifen und mehr

- wann ist eine Programmiersprache eine Programmiersprache?
	- Turing Test bestehen
	- kann Bedingungen, Schleifen, while loops, mit Integer

- C: imperative Sprache, kein Garbage Collector
- Java: Backend, funktionsorientiert, keine Variablen, für Business Logik
- objektorientiert: Objekt, Daten in der Klasse hinerlegen, Funktion zu dem Objekt bauen
- Javascript: deklerativ, 
- Python: KI, Daten
- PHP: Wordpress in PHP geschrieben
- SQL: Datenbanksprache
- Assembly Language: IoT, SmartHome ; Controller (eigene Prozessoren, ohne Compiler, direkt auf der Maschine)
- Go. C in besser (von Google, mit Garbage Collector)
- MatLab: 
- Rust: Garbage Collector
- Swift: FrontEnd für iOS
- Fortran: genauer rechnen als C, mathematische Sachen
- R: grafische Aufbereitung von statistischen Daten
- Kotlin: mobile Apps schreiben
- Scala: funktionale Sprache

- HTML: keine Programmiersprache: HyperTextMarkupLanguage, deklerativ

- deklarativ, imperativ, funktionsorientiert, objektorientiert
## Von-Neumann-Architektur
- Zentralprozessor: CPU (central processing unit)
	- steuert entsprechend den jeweiligen Programmen den Gesamtablauf der Informationsverarbeitung
	- koordiniert beteiligte Funktionseinheiten 
	- führt Rechenoperationen aus
	- Durchführung von **Maschinenbefehlen**
		- Steuerwerk
		- Rechenwerk (ALU) - arithmetic language unit
- Hauptspeicher / Zentralspeicher: RAM (RandomAccessMemory) / ROM (ReadOnlyMemory)
	- enthält die aktuell laufenden Programme und aktuell zu verarbeitenden Daten
		- RAM: Arbeitsspeicher 
		- ROM: Festwertspeicher: Gedächtnis, mit Firmware, BIOS
- Eingabe- & Ausgabegeräte 
- externer Speicher
- Leitungen: BUS mit Clock (Takt) (mit vielen einzelnen Leitungen, fängt bei 8 an, wegen Bit)
	- Daten-BUS
	- Steuer-BUS

- Maschinenbefehle
	- arithmetische Befehle (addieren, subtrahieren, multiplizieren)
	- logische Befehle (vergleichen, verknüpfen)
	- Datentransferbefehle (übertragen, verschieben)
	- Ein- und Ausgabebefehle (lesen, schreiben)

[[Hardware]]

## Mehrkernprozessoren & Mehrkernprozessorsysteme
- Mehrkernprozessor: 
	- mehrere Prozessorkerne für parallele Ausführung von Programmen

## Memory
- Speicherchips
	- flüchtige Speicherchips
		- DRAM & SDRAM
		- SRAM
	- ROM
		- Irreversibler Inhalt FROM, PROM
		- Reversibler Inhalt EPROM, EEPROM
	- MRAM
	- Flash
		- NOR-Flash
		- NAND-Flash
	- NRAM
- überflüssiger Flash-Speicher um fehlerhafte Bites zu ersetzten

## Moore‘sches Gesetz
- Komplexität integrierter Schaltkreise mit minimalen Komponentenkosten verdoppelt sich regelmäßig (alle 12 / 18 / 24 Monate)
- annähernd exponentielles Wachstum

## Betriebssystem
>Verwaltung der Betriebsmittel

## Raid Systeme
- Redundant Array of Independent Disks
	- RAID 0: Striping - Beschleunigung ohne Redundanz (schneller)
	- RAID 1: Mirroring - Spiegelung (sicherer)
	- RAID 5: Leistung + Parität, Block-Level Striping mit verteilter Paritätsinformation (schneller und sicherer)

## Externe Speicher & Virtualisierung
>Computer simulieren

## Anwendungen der Datenkommunikation

## Übermittlung von Signalen

## Protokolle
- Paketmodell
- Schichtenmodell

## IP-Adressen
- IP-Adressen ermöglichen hardwareunabhängige Adressierung
- verbinden lokale Netze auf der zweiten Schicht: Sicherungsschicht
- Zuordnung zwischen physischer Adresse (MAC-Adresse) und IP-Adresse über ARP-Protokoll
- IPv4: 4 Byte hoch 32
- IPv6: 6 Byte hoch 32


### Komponenten & verteiltes Arbeiten
- Browser - Webserver - Application Server - OB
- Client <-> Server (Dienstanforderungen -> / Ergebnisdaten <-)
- Austausch im eigenem Netz: peer to peer

### Internet und Dienste
- Internet
	- weltweite Verbindung vieler Netzwerke verschiedener Betreiber auf Basis der TCP/IP-Protokollfamilie
- Internet Service Provider (ISP)
	- Internet Access Provider: Unternehmen, das Verbindungen zum Internet bereitstellt
	- Nutzer zahlt für die Anbindung ans Internet (Datenvolumen / Bandbreite)
	- Kosten: entfernungsunabhängig
- Domain Name Service (DNS)
	- Internet-Dienst, der Domain-Namen in IP-Adressen übersetzt
- Dienstleistungsmodelle für **Cloud Computing
	- Software-as-a-Service (SaaS)
		- PaaS + Anwendungssoftware
	- Platform-as-a-Service (PaaS)
		- Hardware, Systemsoftware, Infrastruktursoftware, Entwicklungssoftware extern ausgelagert
	- Infrastructure-as-a-Service (IaaS)
		- Hälfte von Hardware, Systemsoftware, Infrastruktursoftware extern ausgelagert
- Cloud
	- elastische Skalierung
	- minutengenaue Abrechnung
	- umgehende Bereitstellung

### Firewall & VPN
- Firewall
	- Hard- und / oder Software, die verschiedene Netzwerkteile selektiv voneinander abtrennt und nur bestimmte Pakete durchlässt
		- IP-Adressen überprüfen
		- HTTP(S) nur auf Port 80 lassen
		- Domains überprüfen
- VPN (virtual private network)
	- sichere „Tunnel“-Verbindung im Internet
	- Daten werden durch VPN-Server verschlüsselt und in eine Hülle des IP-Protokolls „eingepackt“
	- VPN sieht für verbundene Standorte wie ein „echtes“ privates Netz aus
### Technologie-getriebene Megatrends
- Individualisierung
- Miniaturisierung (alles wird kleiner)
- Informationsflut
- Verhaltensänderungen
