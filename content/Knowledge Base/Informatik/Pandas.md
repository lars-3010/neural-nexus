Tags: #🌿 
up:: [[../../Maps of Content/Python2|Python2]]

---
Pandas ist eine leistungsstarke Python-Bibliothek für die Datenmanipulation und -analyse. Sie baut auf NumPy auf und bietet zusätzliche Datenstrukturen und Funktionen, die speziell auf die Arbeit mit tabellarischen Daten zugeschnitten sind.

## Datenstrukturen in Pandas

- Series
    
    - Eindimensionale, beschriftete Arrays, die Daten eines einzelnen Datentyps enthalten
    - Erstellen einer Series: `pd.Series(data, index=index)`
    
- DataFrame
    
    - Zweidimensionale, beschriftete Datenstruktur mit Spalten verschiedener Datentypen
    - Erstellen eines DataFrames: `pd.DataFrame(data, index=index, columns=columns)`
    

## Daten einlesen und speichern

- Einlesen von CSV-Dateien: `pd.read_csv()`
- Einlesen von Excel-Dateien: `pd.read_excel()`
- Einlesen von SQL-Datenbanken: `pd.read_sql()`
- Speichern von Daten in verschiedenen Formaten: `df.to_csv()`, `df.to_excel()`, `df.to_sql()`

## Datenauswahl und -filterung

- Auswählen von Spalten: `df[['column1', 'column2']]`
- Auswählen von Zeilen basierend auf Bedingungen: `df[df['column'] > value]`
- Auswählen von Zeilen und Spalten mit `loc` und `iloc`: `df.loc[rows, columns]`, `df.iloc[row_indices, column_indices]`

## Datenmanipulation

- Hinzufügen und Löschen von Spalten: `df['new_column'] = values`, `df.drop(columns=['column'])`
- Umbenennen von Spalten: `df.rename(columns={'old_name': 'new_name'})`
- Füllen von fehlenden Werten: `df.fillna(value)`
- Gruppieren und Aggregieren von Daten: `df.groupby('column').agg({'column': 'mean'})`

## Datenvisualisierung

- Erstellen von Diagrammen direkt aus DataFrames: `df.plot()`
- Unterstützte Diagrammtypen: Liniendiagramme, Balkendiagramme, Streudiagramme, Histogramme usw.

## Beispiel: Datenanalyse mit Pandas

python

`import pandas as pd  # Einlesen einer CSV-Datei df = pd.read_csv('data.csv')  # Anzeigen der ersten Zeilen print(df.head())  # Auswählen von Spalten selected_columns = df[['column1', 'column2']]  # Filtern von Zeilen basierend auf einer Bedingung filtered_rows = df[df['column1'] > 10]  # Gruppieren und Aggregieren von Daten grouped_data = df.groupby('category').agg({'value': 'mean'})  # Visualisieren der Daten df.plot(x='column1', y='column2', kind='scatter')`

Pandas bietet eine Vielzahl von Funktionen und Methoden für die effiziente Arbeit mit tabellarischen Daten und ist ein unverzichtbares Werkzeug für die Datenanalyse und -manipulation in Python.


### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 
### Sources:
---
