Tags: #🌿 
up:: [[../../Maps of Content/Python2|Python2]]

---
Überwachtes Lernen ist ein Teilgebiet des maschinellen Lernens, bei dem ein Modell anhand von Beispieldaten lernt, eine Funktion zu approximieren, die Eingabedaten (Features) auf bekannte Ausgabedaten (Targets) abbildet. Das Ziel ist es, das Modell so zu trainieren, dass es auf neuen, ungesehenen Daten genaue Vorhersagen treffen kann.

## Arten von überwachtem Lernen

- Klassifizierung: Vorhersage diskreter Klassen oder Kategorien
    
    - Binäre Klassifizierung: Zwei mögliche Klassen (z.B. Spam/Nicht-Spam)
    - Multiklassen-Klassifizierung: Mehr als zwei Klassen (z.B. Bildkategorisierung)
    
- Regression: Vorhersage kontinuierlicher Werte
    
    - Lineare Regression: Vorhersage einer Zielvariablen basierend auf einer oder mehreren Eingabevariablen
    - Polynomiale Regression: Modellierung nichtlinearer Beziehungen durch Hinzufügen von Polynomtermen
    

## Trainingsprozess

1. Datenaufbereitung: Sammeln, Bereinigen und Vorverarbeiten der Daten
2. Merkmalsextraktion: Auswahl und Erstellung relevanter Merkmale aus den Rohdaten
3. Modellauswahl: Auswahl eines geeigneten Algorithmus für das Problem (z.B. Lineare Regression, Entscheidungsbäume, SVM)
4. Modelltraining: Anpassen der Modellparameter anhand der Trainingsdaten
5. Modellevaluierung: Bewertung der Leistung des Modells auf ungesehenen Testdaten
6. Modelloptimierung: Feinabstimmung der Hyperparameter und Verbesserung des Modells

## Herausforderungen und Überlegungen

- Überanpassung (Overfitting): Das Modell lernt die Trainingsdaten auswendig, generalisiert aber schlecht auf neue Daten
- Unteranpassung (Underfitting): Das Modell ist zu einfach und kann die zugrunde liegenden Muster nicht erfassen
- Datenqualität: Verzerrte, unvollständige oder fehlerhafte Daten können die Modellleistung beeinträchtigen
- Merkmalsauswahl: Identifizierung der relevanten Merkmale für das Problem
- Hyperparameteroptimierung: Finden der optimalen Einstellungen für die Modellparameter

## Beispiel: Lineare Regression mit Scikit-learn

python

`from sklearn.linear_model import LinearRegression from sklearn.model_selection import train_test_split from sklearn.metrics import mean_squared_error  # Daten vorbereiten X = [[1], [2], [3], [4], [5]]  # Eingabevariable y = [2, 4, 6, 8, 10]  # Zielvariable  # Daten in Trainings- und Testset aufteilen X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)  # Lineare Regression erstellen und trainieren model = LinearRegression() model.fit(X_train, y_train)  # Vorhersagen auf dem Testset treffen y_pred = model.predict(X_test)  # Mittleren quadratischen Fehler berechnen mse = mean_squared_error(y_test, y_pred) print(f"Mean Squared Error: {mse:.2f}")`

Überwachtes Lernen ist ein leistungsstarker Ansatz für Probleme, bei denen bekannte Ausgabedaten verfügbar sind. Durch die Auswahl geeigneter Algorithmen und eine sorgfältige Datenvorverarbeitung können genaue Vorhersagemodelle für verschiedene Anwendungen erstellt werden.


### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 
### Sources:
---
