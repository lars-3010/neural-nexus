Tags: #🌱
up:: [[../../Maps of Content/Python2|Python2]]

---
Module und Pakete dienen dazu, Python-Code zu organisieren, wiederzuverwenden und mit anderen zu teilen.

## Module

- Eine Moduldatei enthält Python-Definitionen und -Anweisungen
- Module werden mit `import` importiert, z.B. `import math`
- Auf Funktionen und Variablen eines Moduls wird mit der Punktnotation zugegriffen, z.B. `math.pi`
- Mit `from modul import funktion` können spezifische Funktionen direkt importiert werden, z.B. `from math import sin`
- Mit `from modul import *` werden alle Funktionen und Variablen eines Moduls direkt importiert (nicht empfohlen)
- Der `as`-Alias ermöglicht es, Module oder Funktionen unter einem anderen Namen zu importieren, z.B. `import numpy as np`

## Pakete

- Pakete sind Verzeichnisse, die mehrere Moduldateien und ein `__init__.py`-Skript enthalten
- Pakete ermöglichen es, Module hierarchisch zu strukturieren
- Pakete werden mit `import paket.modul` importiert
- Die `__init__.py`-Datei wird beim Import des Pakets ausgeführt und kann verwendet werden, um Untermodule zu importieren oder Initialisierungscode auszuführen

## Standardbibliothek und externe Pakete

- Python verfügt über eine umfangreiche Standardbibliothek mit vordefinierten Modulen und Paketen
- Externe Pakete können mit Paketmanagern wie pip installiert werden, z.B. `pip install numpy`
- Virtuelle Umgebungen ermöglichen es, Pakete projektspezifisch zu installieren und zu verwalten

Module und Pakete fördern die Modularität, Wiederverwendbarkeit und Wartbarkeit von Python-Code.


### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 
### Sources:
---
