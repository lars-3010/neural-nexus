Tags: #🗺️  
up:: [[Programmierung]]

---
>high level, interpreted, object-oriented Programming Language
>open-source language
>clean syntax, beginner friendly & widely used
>dynamic typing -> automatically defines type of variables

>supports:
>	- object-oriented programming
>	- functional programming
>	- procedural programming
>	- large standard library

>usecase:
> 	- Machine Learning

## Grundlagen

- [[../Knowledge Base/Informatik/Variablen und Datentypen|Variablen und Datentypen]]
- [[../Knowledge Base/Informatik/Operatoren|Operatoren]]
- [[../Knowledge Base/Informatik/Kontrollstrukturen (if, for, while)|Kontrollstrukturen (if, for, while)]]
- [[../Knowledge Base/Informatik/Funktionen|Funktionen]]
- [[../Knowledge Base/Informatik/Module und Pakete|Module und Pakete]]

## Datenstrukturen

- [[../Knowledge Base/Informatik/Listen]]
- [[../Knowledge Base/Informatik/Tupel]]
- [[../Knowledge Base/Informatik/Sets]]
- [[../Knowledge Base/Informatik/Dictionaries]]

## Datei-I/O und Datenverarbeitung

- [[../Knowledge Base/Informatik/Dateien lesen und schreiben]]
- [[../Knowledge Base/Informatik/CSV und JSON]]
- [[../Knowledge Base/Informatik/Daten bereinigen und vorbereiten]]

## Data Science Bibliotheken

- [[../Knowledge Base/Informatik/NumPy|NumPy]]
- [[../Knowledge Base/Informatik/Pandas]]
- [[../Knowledge Base/Informatik/Matplotlib]]
- [[../Knowledge Base/Informatik/Seaborn]]
- [[../Knowledge Base/Informatik/Scikit-learn]]

## Machine Learning Grundlagen

- [[../Knowledge Base/Informatik/Überwachtes Lernen (Supervised Learning)]]
- [[../Knowledge Base/Informatik/Unüberwachtes Lernen (Unsupervised Learning)]]
- [[../Knowledge Base/Informatik/Verstärkungslernen (Reinforcement Learning)]]
- [[../Knowledge Base/Informatik/Evaluierungsmetriken]]
- [[../Knowledge Base/Informatik/Hyperparameter-Tuning]]

## Deep Learning mit PyTorch

- [[../Knowledge Base/Informatik/Einführung in PyTorch]]
- [[Tensoren und Gradienten]]
- [[Neuronale Netze]]
- [[Convolutional Neural Networks (CNNs)]]
- [[Rekurrente Neuronale Netze (RNNs)]]
- [[Praxisprojekte mit PyTorch]]

## Fortgeschrittene Themen

- [[Zeitreihenanalyse]]
- [[Textverarbeitung und NLP]]
- [[Empfehlungssysteme]]
- [[Anomalieerkennung]]

## Praxisprojekte

- [[Projekt 1: Beschreibung]]
- [[Projekt 2: Beschreibung]]


# Python-Grundlagen und fortgeschrittene Konzepte für Projekte

## Grundlegende Syntax und Datenstrukturen

### Variablen und Datentypen
- Verwendung von Variablen ohne explizite Typdefinition
- Grundlegende Datentypen: int, float, str, bool
- Komplexe Datentypen: list, tuple, dict, set

```python
# Beispiel für verschiedene Datentypen
user_id = 12345  # int
username = "max_mustermann"  # str
is_active = True  # bool
scores = [95, 88, 72, 91]  # list
user_info = {"name": "Max", "age": 30}  # dict
```

### Kontrollstrukturen
- if-elif-else für bedingte Ausführung
- for und while Schleifen für Iterationen

```python
# Beispiel für eine bedingte Anweisung
if user_info["age"] >= 18:
    print("Zugriff gewährt")
else:
    print("Zugriff verweigert")

# Beispiel für eine Schleife
for score in scores:
    if score > 90:
        print(f"Ausgezeichnete Leistung: {score}")
```

## Objektorientierte Programmierung (OOP) in Python

### Klassen und Objekte
- Definition von Klassen als Blaupausen für Objekte
- Erstellung von Objekten aus Klassen

```python
class User:
    def __init__(self, name, age):
        self.name = name
        self.age = age
    
    def greet(self):
        return f"Hallo, ich bin {self.name}!"

# Objekt erstellen
new_user = User("Anna", 28)
print(new_user.greet())  # Ausgabe: Hallo, ich bin Anna!
```

### Vererbung und Polymorphismus
- Erstellung von Unterklassen zur Spezialisierung von Funktionalität
- Überschreiben von Methoden in Unterklassen

```python
class AdminUser(User):
    def __init__(self, name, age, access_level):
        super().__init__(name, age)
        self.access_level = access_level
    
    def greet(self):
        return f"{super().greet()} Ich bin ein Admin mit Zugriffsebene {self.access_level}."

admin = AdminUser("Max", 35, "High")
print(admin.greet())
```

## Fehlerbehandlung und Ausnahmen

### Try-Except Blöcke
- Abfangen und Behandeln von Fehlern zur Laufzeit

```python
def divide_numbers(a, b):
    try:
        result = a / b
    except ZeroDivisionError:
        return "Error: Division durch Null nicht möglich"
    except TypeError:
        return "Error: Bitte nur Zahlen eingeben"
    else:
        return f"Das Ergebnis ist {result}"

print(divide_numbers(10, 2))  # Normaler Fall
print(divide_numbers(10, 0))  # ZeroDivisionError
print(divide_numbers(10, "2"))  # TypeError
```

## Arbeiten mit Dateien und APIs

### Dateioperationen
- Lesen und Schreiben von Dateien

```python
# Datei lesen
with open("example.txt", "r") as file:
    content = file.read()
    print(content)

# Datei schreiben
with open("output.txt", "w") as file:
    file.write("Dies ist ein Test.")
```

### API-Anfragen mit `requests`
- Senden von HTTP-Anfragen an APIs

```python
import requests

response = requests.get("https://api.example.com/data")
if response.status_code == 200:
    data = response.json()
    print(data)
else:
    print(f"Fehler: {response.status_code}")
```

## Asynchrone Programmierung mit `asyncio`

### Grundlagen von Asynchronität
- Verwendung von `async` und `await` für nicht-blockierende Operationen

```python
import asyncio
import aiohttp

async def fetch_data(url):
    async with aiohttp.ClientSession() as session:
        async with session.get(url) as response:
            return await response.text()

async def main():
    urls = ["https://api.example.com/data1", "https://api.example.com/data2"]
    tasks = [fetch_data(url) for url in urls]
    results = await asyncio.gather(*tasks)
    for result in results:
        print(result)

asyncio.run(main())
```

## Fortgeschrittene Konzepte (für spätere Vertiefung)
- [[Python Decorators]]
- [[Context Managers]]
- [[Generators and Iterators]]
- [[Metaprogramming in Python]]

# Note Structure
### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 

### Sources:
---
