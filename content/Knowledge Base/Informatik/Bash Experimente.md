>in [[Linux]]


- Prompt = Eingabeaufforderung
	``$ [Benutzername]   [Name des Computers]`: [Heimverzeichnis]``

## Befehle
>beenden der Eingabe mit: Strg+
- ls = Liste
	- ls -l = Liste in Listenform
- mkdir = make directory (Verzeichnis erzeugen)
- cd = change directory
- mv = move = umbenennen
- nano = öffnet Datei
- echo = Argumente ausgeben
	echo … > … = Ausgabe in Datei umlenken
	echo … >> … = etwas zu einer Datei hinzufügen und bestehendes lassen
- `cat [Datei]` = Inhalt der Datei ausgeben
- wc = word count
- `cut -d‘ ‘ -f1
	- schneiden, Trennzeichen Leerzeichen, von jeder Zeile wird nur der erste Teil ausgegeben
- sort = alphabetische Sortierung
- rm = remove
- etwas herunterladen
	`[wget [Link]
### Programme installieren
- apt = advanced package tool
- apt update = List der verfügbaren Programmpakete aktualisieren
- sudo = super user do (Adminrechte
	$ sudo apt install …
### Befehl im Quadrat
>Weiterleiten von Ausgaben: **|**    = pipe
### Befehle definieren
>befehle speichern: `alias [Befehlname]=„[Anweisung]“
### Verschlüsseln
- `$ tr ‘e‘ ‘X‘ < [Textdatei]
	- tr = translate
	- e wird durch X ersetzt
- `alias kodieren=„$ tr ‘e‘ ‘X‘ < [Textdatei]
	- speichert den Befehl
	- Befehl verwenden: `kodieren < [Textdatei]
### alias Befehle dauerhaft speichern
``$ nano ~/.bashrc
- in die letzte Zeile schreiben: ``$ tr ‘e‘ ‘X‘ < [Textdatei]
- speichern und beenden per Strg+X
- alias Befehl benutzen: ``$ kodieren < [Textdatei]