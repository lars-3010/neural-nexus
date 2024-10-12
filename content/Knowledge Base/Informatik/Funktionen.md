Tags: #🌱
up:: [[../../Maps of Content/Python2|Python2]]

---
Funktionen sind benannte Codeblöcke, die eine bestimmte Aufgabe erfüllen und wiederverwendbar sind.

## Funktionsdefinition

- Syntax: `def funktionsname(parameter1, parameter2, ...): ...`
- Parameter sind optionale Eingabewerte, die an die Funktion übergeben werden können
- Der Funktionskörper wird eingerückt und enthält den auszuführenden Code
- Funktionen können mit `return` einen Wert zurückgeben

## Funktionsaufruf

- Syntax: `funktionsname(argument1, argument2, ...)`
- Argumente werden an die Funktion übergeben und den Parametern zugewiesen
- Der Funktionskörper wird ausgeführt und ein eventueller Rückgabewert kann weiterverwendet werden

## Parameter und Argumente

- Positionsargumente werden in der Reihenfolge der Parameter übergeben
- Schlüsselwortargumente werden mit dem Parameternamen übergeben, z.B. `funktionsname(param1=wert1, param2=wert2)`
- Standardwerte für Parameter können in der Funktionsdefinition festgelegt werden, z.B. `def funktionsname(param1, param2=defaultwert): ...`
- `*args` sammelt überzählige Positionsargumente in einem Tuple
- `**kwargs` sammelt überzählige Schlüsselwortargumente in einem Dictionary

## Gültigkeitsbereich (Scope)

- Lokale Variablen innerhalb einer Funktion sind nur im Funktionskörper sichtbar
- Globale Variablen außerhalb von Funktionen sind im gesamten Modul sichtbar
- Die `global`-Anweisung ermöglicht den Zugriff auf globale Variablen innerhalb einer Funktion
- Die `nonlocal`-Anweisung ermöglicht den Zugriff auf Variablen aus dem umschließenden Scope innerhalb einer verschachtelten Funktion

Funktionen ermöglichen es, Code zu strukturieren, wiederzuverwenden und die Komplexität zu reduzieren.


### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 
### Sources:
---
