>Open Source Tool für automatisierte Konfiguration und Orchestrierung
- Master Server verbindet sich über SSH mit den Zielsystemen, auf diesen wird kein weiterer Client benötigt
- Zielsysteme werden in einer Hosts-Datei beschrieben & können mit individuellen Parametern versehen werden
- über Kommandozeile können einfache Ad-hoc-Befehle abgesetzt werden z.B. $ansible -m ping all
- Komplexe Konfigurationen werden in YAML als Playbooks beschrieben und mit Python auf den Servern ausgeführt
- während der Ausführung gibt Ansible eine Übersicht aller Tasks und deren Status (ok/changed/failed)