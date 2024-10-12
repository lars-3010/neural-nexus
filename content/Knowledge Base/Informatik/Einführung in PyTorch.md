Tags: #🌱
up:: 

---

>machine learning framework in Python

## Tensoren
---
- mehrdimensionale Arrays / Verallgemeinerungen von Skalaren, Vektoren & Matrizen auf beliebige Dimensionen (0D -> 2D Tensoren)
- natürliche Wahl für die Repräsentation von Daten und Modellparametern im Deep Learning
	- effiziente Kodierung Mehrdimensionaler Daten (Bilder / Videos: 3D / 4D)
	- Hardwarebeschleunigung durch GPU:
		- Deep Learning Frameworks führen Tensoroperationen wie Matrixmultiplikationen massiv parallel aus
	- **Automatische Differenziation** durch die eingebaute Fähigkeit, den Gradienten von Tensoroperationen zu berechnen, was für das Training neuronaler Netze mit Backpropagation entscheidend ist
	- Eine **einheitliche Architektur** für Daten, Modelle und Berechnungen bieten, was die Entwicklung und Portabilität von Deep Learning Modellen erleichtert



PyTorch ist eine leistungsstarke Open-Source-Bibliothek für maschinelles Lernen, die von Facebook entwickelt wurde. Sie bietet eine intuitive und flexible API für die Entwicklung von neuronalen Netzen und ermöglicht effiziente Berechnungen auf GPUs und CPUs.

## Grundlegende Konzepte

- Tensoren: Mehrdimensionale Arrays zur Speicherung von Daten und Parametern
- Autograd: Automatische Berechnung von Gradienten für das Training von neuronalen Netzen
- Optimierer: Algorithmen zur Optimierung der Parameter eines Modells während des Trainings
- Datensätze und Datenlader: Werkzeuge zur effizienten Verarbeitung und Bereitstellung von Trainingsdaten

## Tensoren

- Ähnlich wie NumPy-Arrays, aber mit zusätzlicher Unterstützung für GPU-Berechnungen
- Erstellung von Tensoren: `torch.tensor()`, `torch.zeros()`, `torch.ones()`, `torch.randn()`
- Tensoroperationen: Addition, Multiplikation, Transponierung, Indexierung usw.
- Übertragung zwischen CPU und GPU: `tensor.cpu()`, `tensor.cuda()`

## Autograd

- Automatische Berechnung von Gradienten durch Aufzeichnung von Operationen in einem Berechnungsgraphen
- Ermöglicht effizientes Training von neuronalen Netzen durch Rückwärtspropagation
- Erstellung von Tensoren mit Gradienten: `tensor.requires_grad = True`
- Berechnung von Gradienten: `loss.backward()`

## Neuronale Netze

- Definition von neuronalen Netzen durch Subklassen von `torch.nn.Module`
- Schichten: Lineare Schichten, Konvolutionsschichten, Aktivierungsfunktionen, Pooling usw.
- Vorwärtspass: Berechnung der Ausgabe des Netzes für gegebene Eingaben
- Rückwärtspass: Berechnung der Gradienten und Aktualisierung der Parameter

## Optimierer

- Algorithmen zur Optimierung der Parameter eines Modells während des Trainings
- Stochastic Gradient Descent (SGD), Adam, RMSprop usw.
- Festlegung der Lernrate und anderer Hyperparameter

## Datensätze und Datenlader

- Bereitstellung von Trainingsdaten in Batches für effizientes Training
- Verwendung von `torch.utils.data.Dataset` und `torch.utils.data.DataLoader`
- Unterstützung für Datentransformationen und Datenaugmentierung

## Beispiel: Einfaches neuronales Netz mit PyTorch

python

`import torch import torch.nn as nn import torch.optim as optim  # Daten generieren X = torch.randn(100, 10) y = torch.randn(100, 1)  # Modell definieren class Net(nn.Module):     def __init__(self):         super(Net, self).__init__()         self.fc1 = nn.Linear(10, 20)         self.fc2 = nn.Linear(20, 1)          def forward(self, x):         x = torch.relu(self.fc1(x))         x = self.fc2(x)         return x  # Modell erstellen model = Net()  # Optimierer und Verlustfunktion definieren optimizer = optim.SGD(model.parameters(), lr=0.01) criterion = nn.MSELoss()  # Training for epoch in range(100):     # Vorwärtspass     outputs = model(X)     loss = criterion(outputs, y)          # Rückwärtspass und Optimierung     optimizer.zero_grad()     loss.backward()     optimizer.step()          print(f"Epoch [{epoch+1}/100], Loss: {loss.item():.4f}")`

PyTorch bietet eine intuitive und flexible Umgebung für die Entwicklung von neuronalen Netzen und ermöglicht effiziente Berechnungen auf GPUs und CPUs. Es ist ein leistungsstarkes Werkzeug für Forschung und Entwicklung im Bereich des Deep Learning.

### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 
### Sources:
---
