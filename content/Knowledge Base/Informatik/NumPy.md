Tags: #🌱
up:: [[../../Maps of Content/Python2|Python2]]

---
>for working with multidimensional arrays

NumPy (Numerical Python) ist eine fundamentale Bibliothek für wissenschaftliches Rechnen in Python. Sie bietet Unterstützung für große, mehrdimensionale Arrays und Matrizen sowie eine Vielzahl von mathematischen Funktionen zur effizienten Durchführung von Operationen auf diesen Arrays.

## NumPy-Arrays

- Erstellen von Arrays
    
    - Aus einer Liste: `np.array()`
    - Mit Startwert, Endwert und Schrittweite: `np.arange(start, stop, step)`
    - Mit einer bestimmten Anzahl von gleichmäßig verteilten Werten: `np.linspace(start, stop, num)`
    
- Eigenschaften von Arrays
    
    - Anzahl der Dimensionen: `arr.ndim`
    - Form des Arrays: `arr.shape`
    - Anzahl der Elemente: `arr.size`
    - Datentyp der Elemente: `arr.dtype`
    

## Indizierung und Slicing

- Zugriff auf Elemente eines Arrays über Indizes: `arr[i, j]`
- Auswählen von Teilbereichen (Slicing): `arr[start:stop:step]`
- Boolesche Indizierung: `arr[arr > value]`

## Mathematische Operationen

- Elementweise Operationen: `+`, `-`, `*`, `/`, `**`
- Vergleichsoperatoren: `<`, `>`, `<=`, `>=`, `==`, `!=`
- Mathematische Funktionen: `np.sin()`, `np.cos()`, `np.exp()`, `np.log()` usw.
- Statistische Funktionen: `np.mean()`, `np.median()`, `np.std()`, `np.var()` usw.
- Lineare Algebra: `np.dot()`, `np.linalg.inv()`, `np.linalg.eig()` usw.

## Broadcasting

- Automatische Anpassung der Größe von Arrays für arithmetische Operationen
- Ermöglicht die Durchführung von Operationen auf Arrays unterschiedlicher Größe und Form

## Umformung und Manipulation von Arrays

- Ändern der Form eines Arrays: `arr.reshape()`
- Transponieren eines Arrays: `arr.T`
- Verknüpfen von Arrays: `np.concatenate()`, `np.stack()`, `np.hstack()`, `np.vstack()`
- Aufteilen von Arrays: `np.split()`, `np.hsplit()`, `np.vsplit()`

## Beispiel: Erstellen und Manipulieren eines NumPy-Arrays

python

`import numpy as np  # Erstellen eines 2D-Arrays arr = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])  # Zugriff auf Elemente print(arr[0, 1])  # Ausgabe: 2  # Slicing print(arr[1:, :2])  # Ausgabe: [[4, 5], [7, 8]]  # Elementweise Operation print(arr * 2)  # Ausgabe: [[ 2,  4,  6], [ 8, 10, 12], [14, 16, 18]]`

NumPy ist ein leistungsstarkes Werkzeug für die effiziente Verarbeitung großer Datenmengen und bildet die Grundlage für viele andere wissenschaftliche Python-Bibliotheken wie Pandas, Matplotlib und scikit-learn.
### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 
### Sources:
---
