Tags: #🌿 
up:: [[../../Maps of Content/Python2]]

---
CSV (Comma-Separated Values) und JSON (JavaScript Object Notation) sind zwei gängige Formate zum Speichern und Austauschen strukturierter Daten in Python.

## CSV

- CSV-Dateien enthalten tabellarische Daten, bei denen die Werte durch Kommas (oder andere Trennzeichen) getrennt sind
- Jede Zeile in einer CSV-Datei entspricht einem Datensatz
- Die erste Zeile kann optional eine Kopfzeile mit den Spaltennamen sein

## CSV-Dateien lesen

- Modul `csv` importieren: `import csv`
- CSV-Datei öffnen: `with open('example.csv', 'r') as file:`
- CSV-Reader erstellen: `csv_reader = csv.reader(file)`
- Über Zeilen iterieren: `for row in csv_reader:`

## CSV-Dateien schreiben

- Modul `csv` importieren: `import csv`
- CSV-Datei öffnen: `with open('example.csv', 'w', newline='') as file:`
- CSV-Writer erstellen: `csv_writer = csv.writer(file)`
- Zeilen schreiben: `csv_writer.writerow(row_data)`

## JSON

- JSON ist ein textbasiertes Format zum Speichern und Austauschen strukturierter Daten
- JSON unterstützt Datentypen wie Zahlen, Strings, Booleans, Listen und Objekte
- Python-Dictionaries können leicht in JSON-Objekte konvertiert werden und umgekehrt

## JSON-Daten lesen

- Modul `json` importieren: `import json`
- JSON-Datei öffnen: `with open('example.json', 'r') as file:`
- JSON-Daten laden: `data = json.load(file)`

## JSON-Daten schreiben

- Modul `json` importieren: `import json`
- JSON-Datei öffnen: `with open('example.json', 'w') as file:`
- Daten in JSON konvertieren und schreiben: `json.dump(data, file)`

## Beispiel: CSV lesen

python

`import csv  with open('example.csv', 'r') as file:     csv_reader = csv.reader(file)     for row in csv_reader:         print(row)`

## Beispiel: JSON schreiben

python

`import json  data = {     'name': 'John Doe',     'age': 30,     'city': 'New York' }  with open('example.json', 'w') as file:     json.dump(data, file)`

CSV und JSON sind weit verbreitete Formate für den Austausch und die Speicherung strukturierter Daten in Python und anderen Programmiersprachen.


### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 
### Sources:
---
