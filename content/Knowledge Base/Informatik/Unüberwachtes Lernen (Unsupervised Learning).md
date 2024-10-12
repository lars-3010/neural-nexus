Tags: #🌿 
up:: [[../../Maps of Content/Python2]]

---
Unüberwachtes Lernen ist ein Teilgebiet des maschinellen Lernens, bei dem Algorithmen Muster und Strukturen in Daten ohne explizite Zielvorgaben erkennen. Im Gegensatz zum überwachten Lernen gibt es keine bekannten Ausgabewerte, anhand derer das Modell trainiert werden kann. Stattdessen versucht das Modell, die zugrunde liegende Struktur der Daten zu entdecken und zu lernen.

## Arten von unüberwachtem Lernen

- Clustering: Gruppierung ähnlicher Datenpunkte in Cluster oder Gruppen
    
    - K-Means: Aufteilung der Daten in K Cluster basierend auf der Ähnlichkeit der Datenpunkte
    - Hierarchisches Clustering: Erstellung einer Hierarchie von Clustern durch schrittweises Verbinden oder Trennen von Datenpunkten
    - DBSCAN: Dichtebasiertes Clustering, das Cluster basierend auf der Dichte der Datenpunkte identifiziert
    
- Dimensionsreduktion: Verringerung der Anzahl der Merkmale unter Beibehaltung der wesentlichen Informationen
    
    - Hauptkomponentenanalyse (PCA): Projektion der Daten auf eine niedrigdimensionale Unterraum, der den größten Teil der Varianz erklärt
    - t-SNE: Nichtlineare Dimensionsreduktion zur Visualisierung hochdimensionaler Daten in niedrigdimensionalen Räumen
    
- Anomalieerkennung: Identifizierung von Datenpunkten, die von der Norm abweichen oder ungewöhnlich sind

## Anwendungen von unüberwachtem Lernen

- Kundensegmentierung: Gruppierung von Kunden basierend auf Verhaltensmustern oder demografischen Merkmalen
- Bildkomprimierung: Verringerung der Dimensionalität von Bildern unter Beibehaltung der wesentlichen Informationen
- Themenerkennung in Textdaten: Identifizierung der Hauptthemen in einer Sammlung von Dokumenten
- Anomalieerkennung in Transaktionsdaten: Erkennung ungewöhnlicher oder betrügerischer Transaktionen

## Herausforderungen und Überlegungen

- Wahl der Anzahl der Cluster oder Dimensionen: Bestimmung der optimalen Anzahl von Clustern oder Dimensionen für das Problem
- Interpretation der Ergebnisse: Die Ergebnisse des unüberwachten Lernens erfordern oft menschliche Interpretation und Domänenwissen
- Skalierbarkeit: Viele Algorithmen für unüberwachtes Lernen haben eine hohe Zeitkomplexität bei großen Datenmengen
- Vorverarbeitung der Daten: Normalisierung, Skalierung und Behandlung fehlender Werte sind wichtig für die Leistung der Algorithmen

## Beispiel: K-Means-Clustering mit Scikit-learn

python

`from sklearn.cluster import KMeans from sklearn.datasets import make_blobs  # Beispieldaten generieren X, _ = make_blobs(n_samples=200, centers=4, random_state=42)  # K-Means-Modell erstellen und anpassen kmeans = KMeans(n_clusters=4, random_state=42) kmeans.fit(X)  # Clusterzuordnungen abrufen labels = kmeans.labels_  # Clusterzentren abrufen centroids = kmeans.cluster_centers_  print(f"Cluster labels: {labels}") print(f"Cluster centroids:\n{centroids}")`

Unüberwachtes Lernen ermöglicht es, Muster und Strukturen in Daten zu entdecken, ohne dass explizite Zielvorgaben erforderlich sind. Es ist ein wertvolles Werkzeug für die explorative Datenanalyse, Segmentierung und Dimensionsreduktion.


### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 
### Sources:
---
