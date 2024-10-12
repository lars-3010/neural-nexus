>Sammlung von miteinander verbundenen Geräten, die Informationen austauschen können

___
### LANs und WANs
- LAN (Local Area Network)
	- Netzwerk, das sich in einem begrenzten geografischen Bereich befindet
- WAN (Wide Area Network)
	- Netzwerk, das sich über größere geografische Entfernungen erstreckt
### Netzwerkgeräte
- Router
	- verbindet verschiedene Netzwerke miteinander & leitet Daten zwischen ihnen weiter
- Switch
	- verbindet Geräte innerhalb eines Netzwerks & ermöglicht die effiziente Datenübertragung zwischen ihnen
- Hub
	- sendet Daten an alle angeschlossenen Geräte, unabhängig davon, ob sie die Daten benötigen
- Gateway
	- Netzwerkknoten, der als Eingang / Ausgang für ein anderes Netzwerk fungiert
### OSI-Referenzmodell
- physikalische Schicht
	- Übertragung von Rohdaten über physikalische Medien wie Kabel oder Funkwellen
- Sicherungsschicht (Data Link Layer)
	- Fehlererkennung und -korrektur, Zugriffskontrolle
- Netzwerkschicht
	- Bestimmung des besten Pfades für den Datenverkehr durch das Netzwerk (Routing)
- Transportschicht
	- Gewährleistung zuverlässige Datenübertragung zwischen Geräten (TCP - Transmission Control Protocol, UDP - User Datagram Protocol)
- Sitzungsschicht
	- Verwaltung von Sitzungen (Verbindungen) zwischen Anwendungen
- Präsentationsschicht
	- Übersetzung, Verschlüsselung und Komprimierung von Daten
- Anwendungsschicht
	- Schnittstelle zwischen Netzwerk und der Anwendung (HTTP für Webseiten)

### TCP/IP-Protokollsuite
- Netzzugangsschicht
	- Kombination aus der physikalischen & Sicherrungsschicht des OSI-Modells
- Internetprotokollschicht
	- Netzwerkschicht im OSI-Modell
	- IP (IPv4 / IPv6) ist Hauptprotokoll dieser Schicht
- Transportschicht 
	- enthält TCP & UDP
- Anwendungsschicht
	- verschiedene Protokolle für Anwendungen 
		- HTTP (Web) & FTP (Dateiübertragung) & SMTP (E-Mail)
### IP-Adressierung
- IPv4
	- besteht aus 32 Bits
	- Oktketten (z.B. 192.178.168.1)
- IPv6
	- behebt Mangel an verfügbaren IPv4 Adressen
	- besteht aus 128 Bits
### Routing und Switching
- Routing
	- Prozess, bei dem Datenpakete den besten Weg zwischen Netzwerken finden
- Switching
	- Prozess, bei dem Daten innerhalb eines Netzwerks effizient zwischen Geräten übertragen werden
### Netzwerksicherheit
- Firewall
	- schützt Netzwerk, indem Datenverkehr kontrolliert & unerwünschten Zugriff blockiert
- VPN (Virtual Private Network)
	- verschlüsselte Verbindung über öffentliches Netzwerk (z.B. Internet)
- Verschlüsselung
	- Sicherung von Daten durch Umwandlung in Code
### Netzwerkprotokolle und Dienste
- HHTP/HTTPS
	- Übertragung von Webseiten im Internet
- FTP
	- Dateiübertragungsprotokoll
- DNS
	- Auflösung von Domänennamen in IP-Adressen
### Netzwerkmanagement
- Überwachung von Netzwerkleistung & -aktivität
- Fehlerbehebung bei Netzwerkproblemen
### Wireless Networking
- Wi-Fi
	- Drahtlose Netzwerktechnologie
- WEP, WPA, WPA2, WPA3
	- Sicherheitsprotokolle für WLANs