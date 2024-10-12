Tags: #🌿 
up:: [[../../Maps of Content/Python2]]

---
Seaborn ist eine auf [[Matplotlib]] aufbauende Python-Bibliothek, die eine High-Level-Schnittstelle für die Erstellung informativer und ansprechender statistischer Grafiken bietet. Sie zielt darauf ab, häufige Visualisierungsanforderungen mit einfachen Funktionsaufrufen zu erfüllen und die Erstellung komplexer Diagramme zu erleichtern.

## Grundlegende Konzepte

- Datensatz-orientierte API: Seaborn arbeitet direkt mit [[Pandas]]-DataFrames und [[NumPy]]-Arrays
- Standardmäßig attraktive und informative Diagramme
- Integration mit Matplotlib: Seaborn-Diagramme können mit Matplotlib-Funktionen weiter angepasst werden

## Diagrammtypen

- Verteilungsdiagramme:
    
    - Histogramme: `sns.histplot()`
    - Kerndichteschätzung (KDE): `sns.kdeplot()`
    - Kombiniertes Histogramm und KDE: `sns.displot()`
    
- Kategorische Diagramme:
    
    - Kategorische Streudiagramme: `sns.stripplot()`, `sns.swarmplot()`
    - Violindiagramme: `sns.violinplot()`
    - Boxplots: `sns.boxplot()`
    - Balkendiagramme: `sns.barplot()`, `sns.countplot()`
    
- Regressionsdiagramme:
    
    - Lineare Regression: `sns.regplot()`, `sns.lmplot()`
    
- Matrixdiagramme:
    
    - Heatmaps: `sns.heatmap()`
    - Paarweise Streudiagramme: `sns.pairplot()`
    

## Stile und Farbpaletten

- Festlegen des Seaborn-Stils: `sns.set_style()`
- Verfügbare Stile: "darkgrid", "whitegrid", "dark", "white", "ticks"
- Farbpaletten: `sns.color_palette()`, `sns.cubehelix_palette()`, `sns.diverging_palette()`

## Statistische Analyse

- Lineare Regression: `sns.regplot()`, `sns.lmplot()`
- Korrelationsmatrizen: `sns.heatmap(df.corr())`
- Paarweise Beziehungen: `sns.pairplot()`

## Beispiel: Erstellen eines Violindiagramms mit Seaborn

python

`import seaborn as sns import matplotlib.pyplot as plt  # Beispieldatensatz laden tips = sns.load_dataset("tips")  # Violindiagramm erstellen sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, palette="muted")  # Titel und Beschriftungen hinzufügen plt.title("Verteilung der Rechnungsbeträge nach Wochentag und Raucherstatus") plt.xlabel("Wochentag") plt.ylabel("Rechnungsbetrag")  # Diagramm anzeigen plt.show()`

Seaborn bietet eine benutzerfreundliche Schnittstelle für die Erstellung ansprechender statistischer Grafiken und ergänzt Matplotlib um zusätzliche Funktionen und Stile. Es ist ein wertvolles Werkzeug für die explorative Datenanalyse und die Kommunikation von Ergebnissen.


### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 
### Sources:
---
