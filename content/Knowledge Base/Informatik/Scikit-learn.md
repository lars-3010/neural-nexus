Tags: #🌿 
up:: [[../../Maps of Content/Python2]]

---
Scikit-learn (auch bekannt als sklearn) ist eine leistungsstarke Python-Bibliothek für maschinelles Lernen. Sie bietet eine konsistente Schnittstelle für eine Vielzahl von überwachten und unüberwachten Lernalgorithmen sowie Tools für die Datenvorverarbeitung, Modellauswahl und -evaluierung.

## Grundlegende Konzepte

- Daten: Merkmale (Features) und Zielvariablen (Targets)
- Modelle: Überwachtes Lernen (Klassifizierung, Regression) und unüberwachtes Lernen (Clustering, Dimensionsreduktion)
- Modellauswahl und -evaluierung: Trainings- und Testdaten, Kreuzvalidierung, Metriken

## Datenvorverarbeitung

- Skalierung von Merkmalen: `StandardScaler`, `MinMaxScaler`, `RobustScaler`
- Kodierung kategorischer Variablen: `OneHotEncoder`, `LabelEncoder`
- Aufteilung von Daten: `train_test_split`

## Überwachtes Lernen

- Klassifizierung:
    
    - Logistische Regression: `LogisticRegression`
    - Entscheidungsbäume: `DecisionTreeClassifier`
    - Random Forest: `RandomForestClassifier`
    - Support Vector Machines (SVM): `SVC`
    
- Regression:
    
    - Lineare Regression: `LinearRegression`
    - Entscheidungsbäume: `DecisionTreeRegressor`
    - Random Forest: `RandomForestRegressor`
    - Support Vector Regression (SVR): `SVR`
    

## Unüberwachtes Lernen

- Clustering:
    
    - K-Means: `KMeans`
    - Hierarchisches Clustering: `AgglomerativeClustering`
    - DBSCAN: `DBSCAN`
    
- Dimensionsreduktion:
    
    - Hauptkomponentenanalyse (PCA): `PCA`
    - t-SNE: `TSNE`
    

## Modellauswahl und -evaluierung

- Aufteilung von Daten: `train_test_split`
- Kreuzvalidierung: `cross_val_score`, `GridSearchCV`
- Metriken:
    
    - Klassifizierung: `accuracy_score`, `precision_score`, `recall_score`, `f1_score`
    - Regression: `mean_squared_error`, `mean_absolute_error`, `r2_score`
    

## Beispiel: Klassifizierung mit Scikit-learn

python

`from sklearn.datasets import load_iris from sklearn.model_selection import train_test_split from sklearn.svm import SVC from sklearn.metrics import accuracy_score  # Iris-Datensatz laden iris = load_iris() X, y = iris.data, iris.target  # Daten in Trainings- und Testset aufteilen X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)  # SVM-Modell erstellen und trainieren svm = SVC(kernel='linear', C=1.0, random_state=42) svm.fit(X_train, y_train)  # Vorhersagen auf dem Testset treffen y_pred = svm.predict(X_test)  # Genauigkeit des Modells berechnen accuracy = accuracy_score(y_test, y_pred) print(f"Accuracy: {accuracy:.2f}")`

Scikit-learn ist eine umfassende Bibliothek für maschinelles Lernen in Python und bietet eine Vielzahl von Algorithmen und Werkzeugen für die Datenvorverarbeitung, Modellierung und Evaluierung. Sie ist ein unverzichtbares Werkzeug für Data Scientists und ML-Praktiker.


### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 
### Sources:
---
