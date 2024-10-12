Tags: #🌿 
up:: [[../../Maps of Content/Programmierung|Programmierung]]

---
> - **J**ava**S**cript **O**bject **N**otation
> - lightweight data-interchange format
> - plain text written in JavaScript object notation
> - used to send data between computers
> - language independent

shorter & quicker than XML + array usage

## Syntax
---
- **Objekte**: Bestehen aus Schlüssel-Wert-Paaren, eingeschlossen in geschweifte Klammern `{}`
- **Arrays**: Geordnete Sammlungen von Werten, eingeschlossen in eckige Klammern `[]`
- **Datentypen**: Unterstützt Zeichenketten, Zahlen, boolesche Werte, `null` und Objekte/Arrays

- Data is in name/value pairs `"name":"John"`
- Data is separated by commas

## JSON in Python

### Encoding (Python-Objekt zu JSON)
---
```python
import json  person = {     "name": "Max Mustermann",     "age": 30,     "city": "Berlin",     "hobbies": ["Lesen", "Reisen", "Kochen"] }  
# Objekt zu JSON-String konvertieren 
json_string = json.dumps(person) print(json_string)
```

### Decoding (JSON zu Python-Objekt)
---
```python
`json_string = '{"name": "Max Mustermann", "age": 30, "city": "Berlin", "hobbies": ["Lesen", "Reisen", "Kochen"]}'  
# JSON-String zu Python-Objekt konvertieren 
person = json.loads(json_string) print(person)
```

## Programmierung mit JSON

### JSON-Dateien lesen und schreiben
---

```python
# JSON-Datei lesen 
with open("data.json", "r") as file:     data = json.load(file)  
# JSON-Datei schreiben 
with open("data.json", "w") as file:     json.dump(data, file, indent=2)
```

### JSON und APIs
---
JSON wird häufig für den Datenaustausch zwischen Webanwendungen und APIs verwendet.

```python
import requests  
# HTTP-Anfrage an eine API senden 
response = requests.get("https://api.example.com/data")  
# JSON-Antwort in ein Python-Objekt konvertieren 
data = response.json()
```

### JSON und Datenbanken
---
Viele NoSQL-Datenbanken wie MongoDB speichern Daten im JSON-Format.

```python
from pymongo import MongoClient  
# Verbindung zur MongoDB-Datenbank herstellen 
client = MongoClient("mongodb://localhost:27017/") db = client["mydatabase"] collection = db["mycollection"]  
# Dokument in die Datenbank einfügen 
document = {"name": "Max Mustermann", "age": 30, "city": "Berlin"} collection.insert_one(document)
```

### Relation
---
- **Where from**:  
- **Similar**: 
	- **XML**: JSON is often compared with XML. JSON is less verbose and easier to read and write, while XML is more flexible.
- **Leads to**: 
	- **RESTful APIs**: JSON is the standard format for RESTful web services.
	- **AJAX**: JSON is frequently used with AJAX to update web pages asynchronously.
	- **NoSQL Databases**: Many NoSQL databases (e.g., MongoDB) use JSON-like formats to store data.
- **Opposite**: 
### Sources:
---
![[../../Resources/Media/Excalidraw/JSON MindMap]]
