Tags: #🌿 
up:: [[../../Maps of Content/Python2]]

---
Sets sind eine ungeordnete Sammlung von eindeutigen Elementen in Python. Sie eignen sich besonders für Operationen wie Schnittmenge, Vereinigung und Differenz.

## Eigenschaften von Sets

- Sets sind veränderbar (mutable), d.h. Elemente können hinzugefügt oder entfernt werden
- Sets enthalten keine duplikaten Elemente
- Sets sind ungeordnet, d.h. die Reihenfolge der Elemente ist nicht festgelegt
- Auf Elemente eines Sets kann nicht mit einem Index zugegriffen werden
- Sets haben eine Länge, die mit `len(set)` abgefragt werden kann

## Erstellen von Sets

- Leeres Set: `set_variable = set()`
- Set mit Elementen: `set_variable = {element1, element2, ...}`
- Set aus einem iterierbaren Objekt: `set_variable = set(iterable)`

## Hinzufügen und Entfernen von Elementen

- Element hinzufügen: `set_variable.add(element)`
- Mehrere Elemente hinzufügen: `set_variable.update(iterable)`
- Element entfernen (wirft KeyError, wenn Element nicht vorhanden): `set_variable.remove(element)`
- Element entfernen (kein Fehler, wenn Element nicht vorhanden): `set_variable.discard(element)`
- Zufälliges Element entfernen und zurückgeben: `element = set_variable.pop()`
- Set leeren: `set_variable.clear()`

## Mengenoperationen

- Vereinigung (Union): `set1 | set2` oder `set1.union(set2)`
- Schnittmenge (Intersection): `set1 & set2` oder `set1.intersection(set2)`
- Differenz: `set1 - set2` oder `set1.difference(set2)`
- Symmetrische Differenz: `set1 ^ set2` oder `set1.symmetric_difference(set2)`

## Überprüfen auf Teilmengen und Obermengen

- Teilmenge (Subset): `set1 <= set2` oder `set1.issubset(set2)`
- Echte Teilmenge (Proper Subset): `set1 < set2`
- Obermenge (Superset): `set1 >= set2` oder `set1.issuperset(set2)`
- Echte Obermenge (Proper Superset): `set1 > set2`

Sets sind eine leistungsstarke Datenstruktur für die Verwaltung von eindeutigen Elementen und die Durchführung von Mengenoperationen in Python.


### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 
### Sources:
---
