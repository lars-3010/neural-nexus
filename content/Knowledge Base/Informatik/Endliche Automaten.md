- Funktionsweise ([[EVA-Prinzip]])
    
    - nach dem **E**ingabe-**V**erarbeitung-**A**usgabe Prinzip
        - Eingabe, Ausgabe, Zustände, Überführungsfunktion, Ausgabefunktion, Anfangszustand
        - Eingabemedium: endliches in Felder eingeteiltes Band & Ausgabemedium: einseitig unbegrenztes Band
        - Zentraleinheit: kann verschiedene innere Zustände annehmen und die Arbeit des Automaten steuern
        - Lesekopf: auf Eingabeband & Schreibkopf: auf Ausgabeband
- Bestandteile EA = Endlicher Automat
    
    - Eingabe, Ausgabe, Zustände, Überführungsfunktion, Ausgabefunktion, Anfangszustand
    - Eingabemedium: endliches in Felder eingeteiltes Band
    - Ausgabemedium: einseitig unbegrenztes Band
    - Zentraleinheit: kann verschiedene innere Zustände annehmen und die Arbeit des Automaten steuern
    - Lesekopf: operiert auf dem Eingabeband
    - Schreibkopf: operiert auf dem Ausgabeband
    ![[Organisation/Bilder/F8767ACD-1253-4215-A528-00DEE9A65F8F.jpeg]]
    
- Bestandteile und Arbeitsweise 6-Tupel A=(…) EA (Transduktor) mit Ausgabe
    
    - Menge aller akzeptierenden Eingabeworte = Sprache des Automaten A → L(A)
    - nichtleere, endliche Mengen: X, Y, Z (Eingabealphabet, Ausgabealphabet, Zustandsmenge)
    
    ---
    
    - X: nichtleere, endliche Menge → Eingabealphabet
    - Y: nichtleere, endliche Menge → Ausgabealphabet
    - Z: nichtleere, endliche Menge → Zustandsmenge
    - $\delta$ : $X*Z$ → $Z$ (Überführungsfunktion)
    - $\lambda$ : $X*Y$ → $Y$ (Ausgabefunktion)
    - $z_{0E}Z$: Anfangszustand
    - $\dot{X}$: Menge aller Worte, die aus dem Eingabealphabet gebildet werden können
    - $\dot{Y}$: Menge aller Worte, die aus dem Ausgabealphabet gebildet werden können
    - $\epsilon$: leeres Wort
- Bsp. Transduktor
    
    - Morseautomat
        
        ![[../../Resources/Media/Informatik_Morsezeichen.jpeg]]
    - Prüfbitgenerator
        
        - bei (serieller) Datenübertragung kann es zu Übertragungsfehlern kommen → Bits ändern ihren Wert
        - nach fester Anzahl von Bits wird ein Prüfbit generiert → Paritätsbit
        - nach jedem 3. Bit des Datenworts
            - 0: wenn Anzahl von 1 gerade → gerade Parität
            - 1: wenn Anzahl von 1 ungerade → ungerade Parität
        
        ![[../../Resources/Media/Informatik_Datenwert.jpeg]]
    - Prüfautomat
        
        - **Paritätsbitgenerator** zeigt durch den **Zustand**, in dem er sich gerade **befindet**, an, ob im **letzten Datenwort** bisher eine **gerade** oder **ungerade** Anzahl von 1en **gelesen wurde**
        - Automaten ohne Ausgabe prüfen nur die Eingabe
        - z.B. PIN-Automat
            - im 1. Schritt wird jede bis auf die erste Ziffer $x_1$ akzeptiert
            - im 2. Schritt jede bis auf $x_2$ usw.
                - 42069
                    
                    → keine 4, keine 2, keine 0, keine 6, keine 9
                    
- Bestandteile und Arbeitsweise eines erkennenden EA
    
    - erkennender EA = Akzeptor: 5-Tupel
        - X: nichtleere, endliche Menge → Eingabealphabet
        - Z: nichtleere, endliche Menge → Zustandsmenge
        - $\delta$ : $X*Z$ → $Z$ (Überführungsfunktion)
        - $z_{0E}Z$: Anfangszustand
        - $z_{Ec}Z$: Teilmenge von Z → Menge der Endzustände
    - Menge aller akzeptierenden Eingabeworte = Sprache des Automaten A → L(A)
    - $L(A)=${$w/w_E\dot{X}$ und $\dot{\delta}(w,z_o)_EZ_E$}
- Beispiele Akzeptoren
    
    - Vierertester → prüft ob Dualzahl durch 4 teilbar ist
- Prüfgenerator- und Automat
    
    ### Prüfbitgenerator
    
    Übertragungsfehler (Daten)→ Bits ändern Wert, nach fester Anzahl von Bits wird Prüfbit generiert → Paritätsbit
    
    ### Prüfautomat
    
    z.B. PIN-Automat: **Paritätsbitgenerator,** keine Ausgabe: zeigt durch den Zustand
    
    - in dem er sich **befindet**, ob im **letzten Datenwort** eine **gerade** / **ungerade** Anzahl von 1en **gelesen wurde**
    - im 1. Schritt wird jede bis auf die erste Ziffer $x_1$ akzeptiert, 2. Schritt jede bis auf $x_2$ usw.
- Formale Sprache L
    
    - eine Teilmenge der möglichen Verknüpfungen eines Alphabets A
    - L = Grammatik ist ein 4-Tupel
    - N = Nichtterminal = Platzhalter : Menge der Nicht-Terminale
    - T = Terminale = Buchstaben : Menge der Terminale
    - S = Nichtterminal als Startsymbol : Element von N → Startsymbol
    - P = Menge der Produktionen
- reguläre Sprache
    
    - wenn reguläre Grammatik diese erzeugt = Sprache regulär wenn DEA diese erkennt
    - mithilfe regulärem Ausdrucks darstellbar
- Kontextfreie Sprachen
    
    - Test ob Anzahl a = Anzahl b → zuerst a dann b
    - flexible Speichermöglichkeit nach Last-In-First-Out-Prinzip (Stapel = Stack)
    - Kellerautomat ist ein deterministischer endlicher Automat, der um Kellerspeicher erweitert wurde
    - beliebig viele Zeichen ablegen und jeweils das oberste Zeichen auslesen
    - push (ablegen) - pop (oberstes entfernt) - nop (keine Operation)