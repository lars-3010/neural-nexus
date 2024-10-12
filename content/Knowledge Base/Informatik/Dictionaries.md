Tags: #🌿 
up:: [[../../Maps of Content/Python2]]

---
Dictionaries (auch als "dict" bezeichnet) sind eine ungeordnete Sammlung von Schlüssel-Wert-Paaren in Python. Sie ermöglichen einen effizienten Zugriff auf Werte über eindeutige Schlüssel.

## Eigenschaften von Dictionaries

- Dictionaries sind veränderbar (mutable), d.h. Elemente können hinzugefügt, entfernt oder geändert werden
- Schlüssel in einem Dictionary müssen eindeutig sein
- Schlüssel müssen unveränderbar (immutable) sein, z.B. Strings, Zahlen oder Tupel
- Werte können von beliebigem Typ sein, einschließlich anderer Dictionaries
- Dictionaries sind ungeordnet, d.h. die Reihenfolge der Elemente ist nicht festgelegt
- Auf Werte wird über Schlüssel zugegriffen, nicht über Indizes

## Erstellen von Dictionaries

- Leeres Dictionary: `dict_variable = {}` oder `dict_variable = dict()`
- Dictionary mit Elementen: `dict_variable = {key1: value1, key2: value2, ...}`
- Dictionary aus einer Liste von Tupeln: `dict_variable = dict([(key1, value1), (key2, value2), ...])`
- Dictionary aus benannten Argumenten: `dict_variable = dict(key1=value1, key2=value2, ...)`

## Zugriff auf Werte

- Zugriff auf einen Wert über den Schlüssel: `dict_variable[key]`
- Zugriff auf einen Wert mit Standardwert, wenn der Schlüssel nicht vorhanden ist: `dict_variable.get(key, default_value)`

## Hinzufügen, Ändern und Entfernen von Elementen

- Element hinzufügen oder ändern: `dict_variable[key] = value`
- Element entfernen (wirft KeyError, wenn Schlüssel nicht vorhanden): `del dict_variable[key]`
- Element entfernen und zurückgeben: `value = dict_variable.pop(key, default_value)`
- Alle Elemente entfernen: `dict_variable.clear()`

## Iteration über Dictionaries

- Iteration über Schlüssel: `for key in dict_variable:`
- Iteration über Werte: `for value in dict_variable.values():`
- Iteration über Schlüssel-Wert-Paare: `for key, value in dict_variable.items():`

## Nützliche Dictionary-Methoden

- Überprüfen, ob ein Schlüssel vorhanden ist: `key in dict_variable`
- Anzahl der Elemente: `len(dict_variable)`
- Liste der Schlüssel: `list(dict_variable.keys())`
- Liste der Werte: `list(dict_variable.values())`
- Liste der Schlüssel-Wert-Paare: `list(dict_variable.items())`

Dictionaries sind eine leistungsstarke Datenstruktur für die Verwaltung von Schlüssel-Wert-Paaren und den effizienten Zugriff auf Werte in Python.


### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 
### Sources:
---


to associate a meaning to each value in a collection of values, we use a data structure: **dictionary**
> made up of pairs of keys and values, separated by "**:**"
> keys: labeled indices, help to retrieve values based on their meaning (can be any type)
> each key is associated with exactly one value
> inside dictionary, key-value pairs are separated by ","
> no limitation to storing key-value pairs inside a dictionary

- create a dictionary
	- name = {}

- dictionary values are accessed by their key
```python
actor_bio = {
 "name": "Bill Murray",
 "known for": ["Lost in Translation", "Rushmore"]
}

print(actor_bio["name"])
```


- adding keys: code the dictionary's name and then the key's name between square brackets []
- to check if a dictionary contains a certain key: "key" in dictionary_name
- removing a key-value pair:
	- coding dictionary name followed by the `.pop() ` instruction
	- specify which key we want to remove
	- tip: check if a key is in a dictionary by coding `for ... in ...` 



>treat a dict like it‘s a database for storing & organizing data
___
### adding Dictionaries 
```python
person = {'name': 'Alice', 'age': 81, 'height': 170}
person['weight'] = 80
# Integers also work
person[1] = "Wow"
print(person)

{'name': 'Alice', 'age': 81, 'height': 170, 'weight': 80, 1: 'Wow'}
```
### removing Dictionaries
```python
person = {'name': 'Alice', 'age': 81, 'height': 170}
del person['height']
print(person)

{'name': 'Alice', 'age': 31
```