Tags: #🌿 
up:: [[../../Maps of Content/Python2]]

---
Matplotlib ist eine umfassende Bibliothek zur Erstellung von statischen, animierten und interaktiven Visualisierungen in Python. Sie bietet eine MATLAB-ähnliche Schnittstelle und ermöglicht die Erstellung einer Vielzahl von Diagrammtypen, darunter Liniendiagramme, Streudiagramme, Balkendiagramme, Histogramme und vieles mehr.

## Grundlegende Konzepte

- Figure: Die gesamte Abbildung, die ein oder mehrere Axes (Teildiagramme) enthalten kann
- Axes: Ein einzelnes Diagramm innerhalb einer Figure
- Subplot: Eine Anordnung mehrerer Axes in einem Raster innerhalb einer Figure

## Erstellen von Diagrammen

- Importieren von Matplotlib: `import matplotlib.pyplot as plt`
- Erstellen einer Figure und eines Axes: `fig, ax = plt.subplots()`
- Plotten von Daten: `ax.plot(x, y)`
- Hinzufügen von Beschriftungen: `ax.set_xlabel('X-Label')`, `ax.set_ylabel('Y-Label')`, `ax.set_title('Title')`
- Anzeigen des Diagramms: `plt.show()`

## Diagrammtypen

- Liniendiagramme: `ax.plot(x, y)`
- Streudiagramme: `ax.scatter(x, y)`
- Balkendiagramme: `ax.bar(x, height)`, `ax.barh(y, width)`
- Histogramme: `ax.hist(x)`
- Tortendiagramme: `ax.pie(sizes)`

## Anpassen von Diagrammen

- Festlegen von Grenzen für Achsen: `ax.set_xlim(left, right)`, `ax.set_ylim(bottom, top)`
- Hinzufügen einer Legende: `ax.legend()`
- Ändern von Farben und Stilen: `ax.plot(x, y, color='red', linestyle='--', marker='o')`
- Hinzufügen von Text und Anmerkungen: `ax.text(x, y, 'Text')`, `ax.annotate('Annotation', xy=(x, y))`

## Subplots und Anordnung

- Erstellen mehrerer Subplots: `fig, axs = plt.subplots(nrows, ncols)`
- Zugriff auf einzelne Subplots: `axs[row, col]`
- Anpassen des Abstands zwischen Subplots: `plt.tight_layout()`

## Beispiel: Erstellen eines Liniendiagramms mit Matplotlib

python

`import matplotlib.pyplot as plt import numpy as np  # Daten generieren x = np.linspace(0, 2 * np.pi, 100) y = np.sin(x)  # Figure und Axes erstellen fig, ax = plt.subplots()  # Daten plotten ax.plot(x, y, color='blue', linestyle='-', label='Sinus')  # Beschriftungen hinzufügen ax.set_xlabel('x') ax.set_ylabel('y') ax.set_title('Sinusfunktion') ax.legend()  # Diagramm anzeigen plt.show()`

Matplotlib ist eine leistungsstarke Bibliothek für die Datenvisualisierung in Python und bietet eine Fülle von Optionen zur Anpassung und Gestaltung von Diagrammen. Sie ist eng mit NumPy und Pandas integriert und ermöglicht die Erstellung professioneller Abbildungen für verschiedenste Anwendungen.


### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 
### Sources:
---
