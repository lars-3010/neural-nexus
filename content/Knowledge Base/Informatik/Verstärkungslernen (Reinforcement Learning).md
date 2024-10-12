Tags: #🌿 
up:: [[../../Maps of Content/Python2]]

---
Verstärkungslernen ist ein Teilgebiet des maschinellen Lernens, bei dem ein Agent lernt, optimale Entscheidungen in einer Umgebung zu treffen, indem er Belohnungen maximiert und Bestrafungen minimiert. Im Gegensatz zum überwachten und unüberwachten Lernen erhält der Agent keine direkten Zielvorgaben, sondern lernt durch Interaktion mit der Umgebung.

## Grundlegende Konzepte

- Agent: Die lernende Entität, die Entscheidungen trifft und Aktionen ausführt
- Umgebung: Der Kontext, in dem der Agent agiert und Rückmeldungen erhält
- Zustand: Die aktuelle Situation oder der Kontext, in dem sich der Agent befindet
- Aktion: Eine Entscheidung oder ein Verhalten, das der Agent ausführt
- Belohnung: Ein positives oder negatives Feedback, das der Agent nach einer Aktion erhält
- Policy: Eine Strategie oder ein Regelwerk, das die Aktionen des Agenten in verschiedenen Zuständen bestimmt

## Markov-Entscheidungsprozess (MDP)

- Ein mathematisches Modell für Entscheidungsprobleme in stochastischen Umgebungen
- Besteht aus Zuständen, Aktionen, Übergangswahrscheinlichkeiten und Belohnungen
- Ziel: Finden einer optimalen Policy, die die erwartete kumulative Belohnung maximiert

## Lernalgorithmen

- Q-Learning: Lernen einer Q-Funktion, die den erwarteten Wert einer Aktion in einem bestimmten Zustand schätzt
- SARSA (State-Action-Reward-State-Action): Ähnlich wie Q-Learning, aber berücksichtigt die tatsächlich ausgeführte Aktion im nächsten Zustand
- Policy Gradient: Direkte Optimierung der Policy durch Anpassung der Parameter in Richtung des Gradienten der erwarteten Belohnung

## Explorations-Exploitations-Dilemma

- Exploration: Erkundung neuer Zustände und Aktionen, um potenzielle Belohnungen zu entdecken
- Exploitation: Ausnutzung des aktuellen Wissens, um die besten bekannten Aktionen auszuführen
- Trade-off zwischen Exploration und Exploitation, um sowohl neue Möglichkeiten zu erkunden als auch bekanntes Wissen zu nutzen

## Anwendungen von Verstärkungslernen

- Robotersteuerung: Lernen von Bewegungen und Manipulationen durch Interaktion mit der Umgebung
- Spieleagenten: Lernen optimaler Strategien für Brettspiele oder Videospiele
- Empfehlungssysteme: Lernen personalisierter Empfehlungen durch Interaktion mit Benutzern
- Ressourcenmanagement: Optimierung der Zuweisung von Ressourcen in komplexen Systemen

## Beispiel: Q-Learning mit OpenAI Gym

python

`import gym import numpy as np  # Umgebung erstellen env = gym.make('FrozenLake-v1')  # Q-Tabelle initialisieren Q = np.zeros((env.observation_space.n, env.action_space.n))  # Hyperparameter learning_rate = 0.8 discount_factor = 0.95 num_episodes = 1000  # Q-Learning-Algorithmus for episode in range(num_episodes):     state = env.reset()     done = False          while not done:         # Aktion auswählen (Epsilon-Greedy)         if np.random.uniform(0, 1) < 0.1:             action = env.action_space.sample()  # Exploration         else:             action = np.argmax(Q[state])  # Exploitation                  # Aktion ausführen und Belohnung beobachten         next_state, reward, done, _ = env.step(action)                  # Q-Wert aktualisieren         Q[state, action] = Q[state, action] + learning_rate * (reward + discount_factor * np.max(Q[next_state]) - Q[state, action])                  state = next_state  print("Training abgeschlossen.")`

Verstärkungslernen ermöglicht es Agenten, durch Interaktion mit einer Umgebung optimale Entscheidungen zu treffen. Es hat breite Anwendungsmöglichkeiten in Bereichen wie Robotik, Spieleentwicklung und Empfehlungssystemen.


### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 
### Sources:
---
