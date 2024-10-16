
## Grundbegriffe
- DevOps
	- Entwickler und Betrieb arbeiten zusammen an neuer Software, Versionen und Features
	- Fixes sowie neue Features sind schneller in Produktion
	- Code wird zielgerichteter, konstanter, stabiler entwickelt
- GitOps
	- Konzept: [[Git]] für Entwicklung, Bereitstellung, Wartung eines Softwareproduktes
	- [[Git]]: Software zur Versionsverwaltung von Code im Zusammenspiel mit mehreren Entwicklern
	- Neuer Code wird dabei an einer zentralen Stelle verwaltet und kann von dort in alle Bereiche verteilt werden
- CI/[[CI CD]]
	- Continuous Integration and Continuous Delivery/Development
	- Entwickler teilen regelmäßig ihre Änderungen am Code um Differenzen und Widersprüche früh zu erkennen und zu beseitigen
- ZeroTouch
	- um Software auf vielen verschiedenen Geräten gleichzeitig zu verteilen
	- Rollout wird automatisch angestoßen, sobald Development und Testing erfolgreich abgeschlossen sind
	- großer Vorteil bei Verwaltung von vielen Systemen: IoT & RAN
- Data Analytics
	- Fähigkeit, auf Basis verknüpfter Daten und analysierter Ergebnisse automatisiert reagieren zu können
	- steigert Qualität vor Kunde & hilft effizienter zu agieren
	- Prognosen & Trendanalyse für die Zukunft
# Automated Operations
- FrontEnd
	- Funktionsweise: Verwendet Software zur Bilderkennung Standart Eingabenmethoden zur Verarbeitung
	- Vorteile:
		- Prozesse können sehr simpel und ohne Programmiererfahrung umgesetzt werden
		- kann auf nahezu jeden manuellen Prozess angewendet werden
	- Nachteile: 
		- starke Abhängigkeit zur GUI
		- Laufzeit begrenzt durch Ladezeiten
		- keine Parallelisierung möglich
	- Software: Autobot
- BackEnd
	- Funktionsweise: Verwendet APIs, sowie Libraries zur Anreicherung und Verarbeitung von Daten
	- Vorteile:
		- schnelle Abarbeitung von Prozessen auch parallel möglich
		- Verwendung von standardisierten Schnittstellen erleichtert Bedienung
	- Nachteile: 
		- starke Abhängigkeit zur API
		- Programmiererfahrung notwendig
	- Software: Resolve
- Autobot
	- Excel Tabelle & Auftragstool -> Daten eintragen -> werden angezeigt
	- Arbeitsabläufe durch Frontend Roboter automatisieren
	- anfangs Software zur Skriptentwicklung mit Hilfe  von Bilderkennung (SikuliX) -> Skrite in [[../../Maps of Content/Python2]] geschrieben und können mit visuellen Eingaben vom Display angereichert werden
	- steigende Anforderungen -> neue Software mit besserer Modularität, sowie zusätzliche Features
	- Frontend Automation Software, ermöglicht nicht nur Einsatz von zahlreichen Modulen, sondern kann auch beliebig viele Features erweitert werden
- Resolve
	- Prozesse werden durch einzelne Schritte zu einem Runbook hinzugefügt (Tasks, Loops, weitere Runbooks) 
		- wie ein Struktogramm
	- Workflows sind Open Source -> Wiederverwendbar
	- Runbooks von Resolve in Groovy Script übersetz -> User benötigt keine Programmiererfahrung
	- ca. 2000 Netzabfragen im Mobilfunknetz täglich in der FirstLine
- Automated Operations - SikuliX
	- IoT Netzmonitoring über ein Developer Kit SARA-N211
	- zur Automatisierung verschiedener Abläufe: Frontend Klickroboter mit Hilfe von SikuliX
		- Workfow
			- Beginn: Durchlaufzeiten des Skripts können frei gesetzt werden
			- mit IoT Test SIM-Karte wird sich in das Mobilfunknetz eingewählt
			- verschiedene Messwerte zur Performance und Verfügbarkeit der Mobilfunkzelle werden ausgelesen und abgespeichert
			- Schwellwert in Daten überschritten -> Skript erstellt ein Ticket
- Automated Operations - Resolve (Usecase)
	- für 5G Rollout müssen alle RAD NTs durch CSGs ersetzt und von der AGS Plattform auf NGMA umgeschaltet werden 
	- durch Umbau verschiebt sich die Routinginstanz auf das CSG -> alte BFD auf dem eNodeB löschen
	- Löschung der BFD kann vom Außendienst per Resolve gestartet werden
	- Ersparnis pro Tag ca. 60 Minuten bei 5-8 Umbauten pro Tag
# Test Automation
- Motivation
	- Netze wachsen -> Aufwand, komplexere Netze zu betreiben, steigt
	- konkurrenzfähig bleiben
	- langfristige zentrale Verwaltung für neue Dienste und Plattformen
	- Abhängigkeit von Herstellern verringern -> mehr Software durch Open-Source-Projekte & eigene Entwickler
	
	- Übergabe der Software ist je nach Hersteller verschieden, verzögert den Start der Testphase durch oft zahlreiche Anpassungen des Testverfahrens
	- Einrichtung der Software kann oft nur zusammen mit dem Hersteller erfolgen
	- Entwickler und Tester verwenden nicht die gleichen Softwarekomponenten bzw. Tools und erhalten dadurch unterschiedliche Ergebnisse
	- verschiedene Umgebungen werden von unterschiedlichen Abteilungen betrieben -> Kommunkation und Dokumentation wird erschwert
	- Testumgebung unterscheidet sich oft stark von der Wirkumgebung -> Software kann nicht unter den gleichen Bedingungen getestet werden
	- teilweise werden hunderte Testcases manuell von einigen wenigen Mitarbeitern durchgeführt und je nach Version / Netzelement wiederholt
- TDD = Test Driven Development
	- Unittests
	- Funktionsweise: Entwickler definiert einen Test und schreibt Code -> Code bestätigen
	- Vorteile:
		- Tests können schnell durchgeführt werden
		- Hinweis auf Fehlerursache
	- Nachteile:
		- Testgruppe ist eingeschränkt
		- Tests können ohne den dazugehörigen Code nicht wiederverwendet werden
	- Beispiel:
		- Zündschlüssel drehen -> Anlasser startet, Kurbelwelle dreht, Zylinderkolben bewegen sich
- BDD = Behaviour Driven Development
	- neuer Ansatz, der sich auf Enduser fokussiert
	- Funktionsweise: Tests können bereits vor der Entwicklung definiert werden & beschreiben Benutzererfahrung
	- Vorteile:
		- Alle Beteiligten können Tests definieren & auswerten
		- Tests sind allgemein definiert -> wiederverwendbar
	- Nachteile:
		- langsamer als TDD in der Durchführung
		- fehlgeschlagene Tests geben keinen Hinweis auf Fehlerursache
	- Beispiel:
		- Zündschlüssel drehen -> Motor geht an
- BDD und TDD ergänzen sich -> TDD zum Fehler überprüfen
- Tools (Gherkin, Cucumber, Behave)
- Gherkin:
	- Funktionalität (Feature) kann im Klartext beschrieben und verarbeitet werden
	- Testfälle können in mehreren Sprachen geschrieben werden
	- Feature besteht aus den Bereichen Context, Event, Outcome
	- spezifische Keywords am Anfang jeder Zeile definieren die Eigenschaften
		- Given: Kontext der Funktionalität
		- When: Beschreibung Event, das eintrifft
		- Then: Beschreibt ein erwartetes Ergebnis
		- And: Beschreibt zusätzliche Eigenschaften
		- But: Beschreibt eine Eigenschaft, die nicht eintreffen soll
		- Feature: Beschreibung der Funktionalität
		- Scenario: konkretes Beispiel
		- Background: Zusatzbedingungen für Feature
- Cucumber
	- Klartext (Testcase) in (Definition) Maschinensprache übersetzten
		- Ruby, Jruby, Java, Groovy, Javascript, .NET, PHP, C++, usw…
	- jedes Feature wird schrittweise überprüft, dafür werden Step-Definitionen geschrieben
	- dabei werden wichtige Parameter durch Variablen ersetzt, um gleiche Szenarios mit einer Step- Definition überprüfen zu können
	- verschiedene Datentypen werden von Cucumber unterstützt
		- integer, float, word, string, any, custom
- Behave
	- spezialisiert auf [[../../Maps of Content/Python2]] BDD Framework
	- gehört nicht offiziell zum Cucumber Projekt, verhält sich jedoch sehr ähnlich und verwendet das Gherkin Format
	- unterstützt Frameworks Django und Flask für Entwicklung von WebServices
	- besitzt keine standartmäßige Parallelausführung von Tests, dafür wird ein extra spinoff Framework (behave-parallel) benötigt
	- PyCharm Professional Edition Support
# Lifecycle Automation
- Software Lifecycle Automation - DevOpsLab
	- Vernetzung in verschiedene Bereiche
		- keine direkte Verbindung zueinander (Sicherheitsgründe)
	- zentrale Stelle zum Code publishen
- Neue Arbeitsmethoden
	- [[unsorriwer/Programme/Apps/Gitlab/GitLab]]
	- JFrog Artifactory
		- Software Repository für Binärdateien (Artifacts)
		- zentrales Repository bei der Entwicklung von Software -> gemeinsame Toolbasis -> Konflikte sowie unterschiedliche Abhängigkeit werden verringert
	- [[../../../../Archiv/Organisation/Institutionen & Programme/Institutionen/Unternehmen/Telekom/Magenta CI CD]]
		- [[../../Docker]]
		- [[../../Kubernetes]]
- Verwendete Technologien
- Tools (Magenta CICD, Ansible, Chef, Puppet)
- SCM - Software Configuration Management
	- Zentrale Verwaltung & Konfiguration von mehreren Endsystemen
	- basiert meist auf einem Client-Server-Prinzip, auf Zielsystemen wird ein extra Client installiert, der mit dem zentralen Server kommuniziert
	- Konfigurationen werden in einfache Blueprints auf dem Server beschrieben und durch den Client in ausführbare Skriptbefehle übersetzt
	- SCM-Tools bieten besonders beim Betrieb von vielen Systemen einen großen Vorteil, da mehrere Änderungen gleichzeitig durchgeführt werden können
	- mit optimierten Lösungen können über 100.000 Knoten verwaltet werden
	- bekannte SCM-Tools: [[Ansible]], [[Chef]], [[Puppet]]
		- Architektur: Master only - Master / Agent
		- Skriptsprache: YAML - Ruby DSL - Puppet DSL
		- Programmiersprache: Python - Ruby & Erlang - Ruby
		- Skalierung: Sehr gut 
		- Deployment: Konfig-Push - Konfig-Pull
		- Synchronisierung: Nein - Ja
# Automated Analytics
- Datenkompetenz
	- Fähigkeit: wichtige Daten zu sammeln, aufzubereiten und auszuwerten
	- Data Literacy 
		- Konzeptioneller Rahmen - Grundverständnis über Daten und deren Wertschöpfung
		- Datensammlung - Informationen aus unterschiedlichsten Quellen zu erhalten
		- Datenmanagement - Qualität der Daten kritisch bewerten und strukturieren
		- Datenanwendung - Entscheidungen anhand der präsentierten Daten treffen
		- Trennung der wichtigen und unwichtigen Daten
		- Big Data und IoT sind große Herausforderungen für die Zukunft
- Data Driven Company
	- beim Data Driven Business wird aus Daten wird ein Mehrwert für Kunden und die eigenen Mitarbeiter gewonnen
	- wichtige Entscheidungen für die Zukunft oder Optimierungen bestehender Prozesse
	- Daten aus Technik, Marketing, Service, Sales, usw.
	- Trendanalysen & Forecasts können mit Hilfe von KI noch effizienter und gezielter getroffen werden
- Motivation
	- für Bereitstellung eines funktionsfähigen Services werden mehrere essentielle Komponenten benötigt, welche teilweise voneinander abhängig sind
	- jeder dieser Server & Anwendung hat ein eigenes Logging: Informationen, Events, Fehler, Warnungen
	- Logs sind unstrukturierte Text Daten, meist nur durch Anwendung und Zeitstempel strukturiert
	- Serviceausfall -> jeder Server und jede Anwendung muss auf möglich Ursachen geprüft werden
	- Betriebssysteme verfügen über Tools, die Daten zu filtern und strukturieren, sind aber verteilt -> kein klares Fehlerbild
	- Ziel: Log-Daten an einem zentralen Punkt sammeln, filtern, strukturieren & grafisch aufbereiten -> schnell & übersichtlich ausgewertet werden können
- Tools (Filebeat, Logstash, Elasticsearch, Kibana)
	- Elastic Stack
		- ELK Stack (Elasticsearch, Logstash, Kibana)
		- mehrere Open Source Projekte 2012 zusammengeschlossen
		- 2015: Beats löst Logstash als Datensammler ab
		- Elasticsearch: hohe Performanz & Skalierbarkeit 
	- Filebeat
		- performante und leichtgewichtete Open Source Software -> Sammeln & Weiterleiten von Daten
			- Filebeat: Log-Dateien aus ca. 20 verschiedenen Eingabe Typen
			- Metricbeat: Metriken wie z.B. CPU, RAM, Speicher, usw.
			- Packetbeat: Netzwerkdaten für ca. 15 verschiedene Protokolle
			- Apachebeat: Status eines Apache Webservers auslesen
		- viele neue Module von der Community auf Basis des „libbeat“ Frameworks geschrieben
		- Daten können an mehrere Outputs (Kafka, Redis, File, Console) verteilt werden
	- Logstash
		- Elastic Stack Komponente zur Datenaufbereitung
		- Geschrieben in JRuby (JVM)
		- besteht aus den Bereichen Input > Filter > Output
		- kann Daten anonymisieren und geolocation lookups
		- nutzt Grok zur Strukturierung der Daten durch reguläre Ausdrücke
		- kann Vielzahl von Inputs verarbeiten (file, exec, github, kafka, redis, …)
		- kann Daten an mehrere Outputs liefern (email-´, mongodb, nagios, zabbix, …)
		- lässt sich mit über 200 Plugins erweitern für individuelle Kombination aus Inputs, Filtern & Outputs
	- Elasticsearch
		- NoSQL Datenbank / RESTful.Suchmaschine auf JSON Basis, bildet Kernkomponente des Elastic Stacks
		- seit 2010 auf Basis von Apache Lucene in Java entwickelt
		- bietet Indizierung & Suche von Dateien in nahezu Echtzeit
		- Daten können über verschiedene Befehle abgefragt werden
			- `GET <index>/_doc/<_id>` - Bezieht alle Datenfelder einer ID
			- `HEAD <index>/_doc/<_id>` - Prüft, ob Datensatz existiert
	- Kibana
		- Open Source Frontend Anwendung, um Daten sowie Konfigurationen des Elastic Stacks zu visualisieren und zu verwalten
		- in [[../../01.01. Programmierung/Software Engineering/Programmieren/Programmiersprachen/Web-Entwicklung/Javascript]] geschrieben und 2010 als Teil des ELK Stacks veröffentlicht
		- verfügt über integrierte Konsole, mit der die einzelnen Komponenten konfiguriert werden können
		- in Logstash eingefügte Standortdaten können in Kibana ausgewertet und in geografische Karten visualisiert werden
		- Alarme können definiert und mit verschiedenen Reaktionen versehen werden, z.B. Benachrichtigungen per Mail oder Chat