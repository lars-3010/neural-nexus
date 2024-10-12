Tags: #🌿 
up:: [[../../Maps of Content/Python2]]

---
Tupel sind eine weitere wichtige Datenstruktur in Python. Sie ähneln Listen, haben jedoch einige entscheidende Unterschiede.

## Eigenschaften von Tupeln

- Tupel sind unveränderbar (immutable), d.h. Elemente können nach der Erstellung nicht mehr geändert werden
- Tupel können Elemente unterschiedlichen Typs enthalten (z.B. Zahlen, Strings, andere Tupel)
- Auf Elemente eines Tupels wird mit einem Index zugegriffen, der bei 0 beginnt, z.B. `tupel`
- Tupel haben eine Länge, die mit `len(tupel)` abgefragt werden kann

## Erstellen von Tupeln

- Leeres Tupel: `tupel = ()`
- Tupel mit Elementen: `tupel = (element1, element2, ...)`
- Tupel aus einem iterierbaren Objekt: `tupel = tuple(iterable)`
- Tupel ohne Klammern: `tupel = element1, element2, ...`

## Zugriff auf Tupelelemente

- Zugriff auf ein Element mit Index: `tupel[index]`
- Zugriff auf einen Bereich von Elementen (Slicing): `tupel[start:ende]`
- Negative Indizes zählen von hinten, wobei -1 das letzte Element ist

## Tupel als Rückgabewerte

- Funktionen können mehrere Werte als Tupel zurückgeben
- Die Rückgabewerte können in separate Variablen entpackt werden, z.B. `a, b = tupel`

## Unveränderbarkeit von Tupeln

- Tupel können nicht verändert werden, was sie für bestimmte Anwendungen geeignet macht (z.B. Schlüssel in Dictionaries)
- Tupel sind speichereffizienter als Listen, da sie unveränderbar sind

## Tupel als Schlüssel in Dictionaries

- Da Tupel unveränderbar sind, können sie als Schlüssel in Dictionaries verwendet werden
- Listen können nicht als Schlüssel verwendet werden, da sie veränderbar sind

Tupel sind eine effiziente und unveränderbare Alternative zu Listen in Python.


### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 
### Sources:
---



tuples group related pieces of data
> tuples can return multiple values inside functions
> can be used inside [[Dictionaries]]
### Creating Tuples
```python
movies = [("Vertigo", "Parasite"), (1958, 2019)]

movie_tuples = []

ThisIsATuple = ("...", )
```


### Tuples and Lists
> difference: values can't be updated, added, or deleted from tuples