Tags: #🌿 
up:: [[../../Maps of Content/Python2]]

---
Evaluierungsmetriken sind quantitative Maße, die verwendet werden, um die Leistung eines maschinellen Lernmodells zu bewerten. Sie ermöglichen es, die Qualität der Vorhersagen eines Modells im Vergleich zu den tatsächlichen Werten zu messen und verschiedene Modelle miteinander zu vergleichen.

## Metriken für Klassifizierungsprobleme

- Genauigkeit (Accuracy): Anteil der korrekt klassifizierten Beispiele an der Gesamtzahl der Beispiele
- Präzision (Precision): Anteil der korrekt als positiv klassifizierten Beispiele an allen als positiv klassifizierten Beispielen
- Trefferquote (Recall): Anteil der korrekt als positiv klassifizierten Beispiele an allen tatsächlich positiven Beispielen
- F1-Score: Harmonisches Mittel aus Präzision und Trefferquote
- ROC-Kurve (Receiver Operating Characteristic): Visualisierung der Leistung eines binären Klassifikators bei verschiedenen Schwellenwerten
- AUC (Area Under the ROC Curve): Maß für die Gesamtleistung eines binären Klassifikators

## Metriken für Regressionsprobleme

- Mittlerer quadratischer Fehler (Mean Squared Error, MSE): Durchschnittlicher quadratischer Unterschied zwischen vorhergesagten und tatsächlichen Werten
- Mittlerer absoluter Fehler (Mean Absolute Error, MAE): Durchschnittlicher absoluter Unterschied zwischen vorhergesagten und tatsächlichen Werten
- Wurzel des mittleren quadratischen Fehlers (Root Mean Squared Error, RMSE): Quadratwurzel des MSE
- R-Quadrat (R-Squared, R²): Anteil der Varianz in den abhängigen Variablen, der durch die unabhängigen Variablen erklärt wird

## Metriken für Clusteringprobleme

- Silhouettenkoeffizient: Maß für die Qualität der Clusterbildung basierend auf der Intra-Cluster-Kompaktheit und Inter-Cluster-Trennung
- Davies-Bouldin-Index: Verhältnis der Summe der Intra-Cluster-Streuungen zur Inter-Cluster-Separation
- Calinski-Harabasz-Index: Verhältnis der Inter-Cluster-Varianz zur Intra-Cluster-Varianz

## Kreuzvalidierung

- Technik zur Bewertung der Generalisierungsfähigkeit eines Modells
- Aufteilung der Daten in k Teilmengen (Folds)
- Training und Evaluierung des Modells k-mal mit unterschiedlichen Trainings- und Validierungsteilmengen
- Durchschnittliche Leistung über alle Folds gibt Aufschluss über die erwartete Leistung auf ungesehenen Daten

## Beispiel: Evaluierung eines Klassifikationsmodells mit Scikit-learn

python

`from sklearn.datasets import load_iris from sklearn.model_selection import train_test_split from sklearn.svm import SVC from sklearn.metrics import accuracy_score, precision_score, recall_score, f1_score  # Iris-Datensatz laden iris = load_iris() X, y = iris.data, iris.target  # Daten in Trainings- und Testset aufteilen X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)  # SVM-Modell erstellen und trainieren svm = SVC(kernel='linear', C=1.0, random_state=42) svm.fit(X_train, y_train)  # Vorhersagen auf dem Testset treffen y_pred = svm.predict(X_test)  # Evaluierungsmetriken berechnen accuracy = accuracy_score(y_test, y_pred) precision = precision_score(y_test, y_pred, average='weighted') recall = recall_score(y_test, y_pred, average='weighted') f1 = f1_score(y_test, y_pred, average='weighted')  print(f"Accuracy: {accuracy:.2f}") print(f"Precision: {precision:.2f}") print(f"Recall: {recall:.2f}") print(f"F1-Score: {f1:.2f}")`

Evaluierungsmetriken sind entscheidend, um die Leistung von maschinellen Lernmodellen zu quantifizieren und zu vergleichen. Die Auswahl geeigneter Metriken hängt von der Art des Problems und den spezifischen Anforderungen der Anwendung ab.


### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 
### Sources:
---
