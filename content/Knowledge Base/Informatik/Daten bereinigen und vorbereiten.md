Tags: #🌿 
up:: [[../../Maps of Content/Python2]]

---
Die Bereinigung und Vorbereitung von Daten ist ein wichtiger Schritt in der Datenanalyse und im Machine Learning. Python bietet verschiedene Bibliotheken und Techniken, um Daten zu bereinigen, zu transformieren und für die weitere Verarbeitung vorzubereiten.

## Datenbereinigung

- Entfernen von fehlenden Werten (NaN - Not a Number)
    
    - Löschen von Zeilen oder Spalten mit fehlenden Werten: `df.dropna()`
    - Ersetzen von fehlenden Werten durch einen bestimmten Wert: `df.fillna(value)`
    
- Entfernen von Duplikaten
    
    - Löschen von duplizierten Zeilen: `df.drop_duplicates()`
    
- Behandlung von Ausreißern
    
    - Identifizieren von Ausreißern mithilfe von statistischen Methoden oder Visualisierungen
    - Entfernen oder Ersetzen von Ausreißern je nach Anwendungsfall
    

## Datentransformation

- Skalierung von Merkmalen
    
    - Normalisierung (Skalierung auf den Bereich ): `from sklearn.preprocessing import MinMaxScaler`
    - Standardisierung (Mittelwert 0, Standardabweichung 1): `from sklearn.preprocessing import StandardScaler`
    
- Kodierung kategorischer Variablen
    
    - One-Hot-Kodierung: `from sklearn.preprocessing import OneHotEncoder`
    - Label-Kodierung: `from sklearn.preprocessing import LabelEncoder`
    
- Umgang mit Datumsangaben und Zeitstempeln
    
    - Konvertierung in datetime-Objekte: `pd.to_datetime()`
    - Extrahieren von Merkmalen wie Jahr, Monat, Tag, Wochentag usw.
    

## Datenintegration

- Zusammenführen von Daten aus verschiedenen Quellen
    
    - Zusammenführen von DataFrames basierend auf einer gemeinsamen Spalte: `pd.merge()`
    - Verketten von DataFrames vertikal: `pd.concat()`
    
- Umgang mit unterschiedlichen Datenformaten und Strukturen
    
    - Konvertierung zwischen verschiedenen Datentypen: `astype()`
    - Umstrukturieren von Daten mit Pivotierung und Melting: `df.pivot()`, `pd.melt()`
    

## Datenbereinigung mit Pandas

- Pandas ist eine leistungsstarke Bibliothek für die Datenmanipulation und -analyse in Python
- Wichtige Funktionen für die Datenbereinigung und -vorbereitung:
    
    - Informationen über den DataFrame: `df.info()`, `df.describe()`
    - Auswählen von Spalten: `df[['column1', 'column2']]`
    - Filtern von Zeilen basierend auf Bedingungen: `df[df['column'] > value]`
    - Anwenden von Funktionen auf Spalten: `df['column'].apply(function)`
    

Die Bereinigung und Vorbereitung von Daten erfordert oft ein iteratives Vorgehen und hängt stark vom spezifischen Datensatz und dem Anwendungsfall ab. Die Verwendung von Bibliotheken wie Pandas und scikit-learn kann den Prozess erheblich erleichtern.


### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 
### Sources:
---
