Tags: #🌿 
up:: [[../../Maps of Content/Python2]]

---
Hyperparameter-Tuning ist der Prozess der Optimierung der Hyperparameter eines maschinellen Lernmodells, um dessen Leistung zu verbessern. Hyperparameter sind Einstellungen, die vor dem Training festgelegt werden und nicht während des Trainings gelernt werden, wie z.B. die Lernrate, die Anzahl der Schichten in einem neuronalen Netz oder die Tiefe eines Entscheidungsbaums.

## Manuelle Suche

- Manuelle Auswahl und Erprobung verschiedener Hyperparameterkombinationen
- Zeitaufwendig und erfordert Erfahrung und Intuition
- Kann zu suboptimalen Ergebnissen führen

## Gittersuche (Grid Search)

- Systematische Suche über einen vordefinierten Hyperparameterraum
- Ausprobieren aller möglichen Kombinationen von Hyperparameterwerten aus einem festgelegten Gitter
- Kann rechenintensiv sein, insbesondere bei einer großen Anzahl von Hyperparametern und Werten
- Garantiert das Finden der besten Kombination im definierten Suchraum

## Zufällige Suche (Random Search)

- Zufällige Auswahl von Hyperparameterkombinationen aus einem definierten Suchraum
- Effizienter als Gittersuche, insbesondere bei hochdimensionalen Suchräumen
- Kann gute Ergebnisse mit weniger Rechenaufwand erzielen
- Bietet keine Garantie, die optimale Kombination zu finden

## Bayessche Optimierung

- Iterative Optimierungstechnik, die ein probabilistisches Modell des Suchraums erstellt
- Nutzt vorherige Evaluierungen, um vielversprechende Regionen im Suchraum zu identifizieren
- Effizient bei teueren Evaluierungsfunktionen und kontinuierlichen Hyperparametern
- Erfordert mehr Implementierungsaufwand als Gittersuche oder zufällige Suche

## Kreuzvalidierung

- Kombination von Hyperparameter-Tuning mit Kreuzvalidierung
- Auswertung jeder Hyperparameterkombination mit k-facher Kreuzvalidierung
- Robustere Schätzung der Generalisierungsleistung im Vergleich zur Verwendung eines einzelnen Validierungssets
- Erhöhter Rechenaufwand aufgrund der mehrfachen Modelltrainings

## Beispiel: Hyperparameter-Tuning mit Gittersuche und Scikit-learn

python

`from sklearn.datasets import load_iris from sklearn.model_selection import GridSearchCV from sklearn.svm import SVC  # Iris-Datensatz laden iris = load_iris() X, y = iris.data, iris.target  # Hyperparameterraum definieren param_grid = {     'C': [0.1, 1, 10],     'kernel': ['linear', 'rbf'],     'gamma': [0.1, 1, 10] }  # SVM-Modell erstellen svm = SVC(random_state=42)  # Gittersuche durchführen grid_search = GridSearchCV(estimator=svm, param_grid=param_grid, cv=5) grid_search.fit(X, y)  # Beste Hyperparameter und Ergebnis ausgeben print(f"Beste Hyperparameter: {grid_search.best_params_}") print(f"Bestes Ergebnis: {grid_search.best_score_:.2f}")`

Hyperparameter-Tuning ist ein entscheidender Schritt bei der Entwicklung von maschinellen Lernmodellen, um deren Leistung zu optimieren. Die Wahl der geeigneten Tuning-Methode hängt von der Komplexität des Modells, der Anzahl der Hyperparameter und den verfügbaren Ressourcen ab.


### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 
### Sources:
---
