Tags: #🌿 
up:: [[../../Maps of Content/Python2]]

---
In Python können Dateien mithilfe der integrierten Funktionen `open()`, `read()`, `write()` und `close()` gelesen und geschrieben werden.

## Dateien öffnen

- Syntax: `file_object = open(filename, mode)`
- `filename` ist der Name der Datei (inklusive Pfad, wenn nicht im aktuellen Verzeichnis)
- `mode` gibt den Zugriffsmodus an, z.B. `'r'` für Lesen, `'w'` für Schreiben, `'a'` für Anhängen
- Zusätzliche Modi: `'b'` für Binärmodus, `'+'` für Lesen und Schreiben
- Beispiel: `file_object = open('example.txt', 'r')`

## Dateien lesen

- Gesamten Inhalt lesen: `content = file_object.read()`
- Eine Zeile lesen: `line = file_object.readline()`
- Alle Zeilen als Liste lesen: `lines = file_object.readlines()`
- Iteration über Zeilen: `for line in file_object:`

## Dateien schreiben

- Text in Datei schreiben: `file_object.write(string)`
- Mehrere Strings schreiben: `file_object.writelines(list_of_strings)`
- Zeilenumbrüche müssen manuell mit `'\n'` hinzugefügt werden

## Dateien schließen

- Geöffnete Dateien sollten immer geschlossen werden: `file_object.close()`
- Alternativ kann `with` verwendet werden, um Dateien automatisch zu schließen:python
    
    `with open(filename, mode) as file_object:     # Dateioperationen`
    

## Beispiel: Datei lesen

python

`with open('example.txt', 'r') as file:     content = file.read()     print(content)`

## Beispiel: Datei schreiben

python

`with open('example.txt', 'w') as file:     file.write('Hello, World!\n')     file.write('This is a test.\n')`

## Nützliche Funktionen

- Überprüfen, ob eine Datei existiert: `os.path.exists(filename)`
- Verzeichnis einer Datei: `os.path.dirname(filename)`
- Dateiname ohne Verzeichnis: `os.path.basename(filename)`

Das Lesen und Schreiben von Dateien ist eine grundlegende Fähigkeit in Python und ermöglicht die Verarbeitung und Speicherung von Daten.


### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 
### Sources:
---
