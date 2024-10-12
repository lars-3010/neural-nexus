- Biber-Aufgabe
    
    - Ein fleißiger Bieber mit n Zuständen ist eine Turingmaschine mit n Zuständen, die zwei Bedingungen erfüllt:
    
    1. Sie bleibt, wenn man sie auf ein Band mit lauter Nullen aussetzt irgendwann stehen.
    2. Sie schreibt zwischen Start und Stopp mindestens so viele Einsen auf das Band wie jede andere Turingmaschine mit n Zuständen, die gleichfalls anhält.
    
    - Die maximale Zahl von Einsen, die eine irgendwann anhaltende Turingmaschine mit Zuständen auf ein Band mit lauter Nullen durchsucht, bezeichnet man als B(n).
    - B ist dabei die sogenannte Biberfunktion bzw. Radofunktion. Bis heute sind lediglich 4 Funktionswerte bekannt:
    - B(2)=1 →
    - B(3)=4 →
    - B(4)=6 → 1962
    - B(5)=13 → 1973
- Automaten
    
    > X=(a,b)
    > 
    > regulärer Ausdruck: $a^nb$ ; ne/N
    
    Eine **Turringmaschine** TM ist ein Sechser-Tupel $(E,Z,K,z_o,Z_E, \delta)$
    
    Bestehend aus:
    
    -einer nichtleeren, endlichen Menge E von Bandzeichen
    
    -einer nichtleeren, endlichen Menge Z von Zuständen
    
    -dem Startzustand $z_o$
    
    -einer nichtleeren, endlichen Menge $Z_E$ von Endzuständen
    
    -einer Überführungsfunktion $\delta$: $ExZ → ExZxK$
    
	![[Organisation/Bilder/Pasted image 20230930223739.png]]

    
    ‘ ‘ = leer
    
    → Bei Wörtern in gemischter Form mit mind. 1x a vor einem b bleiben so viele b enthalten, die mehr als a am Anfang hintereinander stehen, falls mehr b im Wort enthalten als a am Anfang hintereinander stehen.
    
    Turing Berechenbarkeit
    
    → Haltefunktion:
    
- Beispiel-Turingmaschinen
    
    **Halteproblem:**
    
    - Können [[Algorithmen]] entwickelt werden, mit dem man testen kann, ob ein übergebener Algorithmus bei der Verarbeitung übergebener Daten hält oder nicht
        
    - Minus 1
        
        Die Maschine subtrahiert von einer natürlichen Zahl in Strichdarstellung eine Eins:
        
        |0|_|_|L|1|
        |---|---|---|---|---|
        |0|a|a|R|0|
        |1|a|_|S|2|
        
    - Minus
        
        Die Maschine berechnet die Differenz a - b zweier Strichzahlen, wobei a ≥ b vorausgesetzt wird.
        
        aaaaa-aa → aaa
        
        |0|||S|5|
        |---|---|---|---|---|
        |0|-|-|R|1|
        |0|a|a|R|0|
        |1|||L|2|
        |1|a|a|R|1|
        |2|-||S|5|
        |2|a||L|3|
        |3|||R|4|
        |3|-|-|L|3|
        |3|a|a|L|3|
        |4|a||R|0|
        
    - Add 1
        
        Die Maschine addiert zu einer natürlichen Zahl in Strichdarstellung eine Eins.
        
        aaa → aaaa
        
        |0||a|S|1|
        |---|---|---|---|---|
        |0|a|a|L|0|
        
    - Add
        
        Die Maschine berechnet die Summe a + b zweier Strichzahlen.
        
        |0||a|S|1|
        |---|---|---|---|---|
        |0|a|a|L|0|
        
    - Kopiermaschine
        
        1111 ⇒ 1111_1111
        
        |0|a|b|R|1|
        |---|---|---|---|---|
        |0|||L|4|
        |1|a|a|R|1|
        |1|||R|2|
        |2|a|a|R|2|
        |2||a|L|3|
        |3|||L|3|
        |3|a|a|L|3|
        |3|b|b|R|0|
        |4|b|a|L|4|
        |4|||S|5|
        
    - Multiplizieren
        
        11 * 111 → 111111
        
        |0|1||r|1|
        |---|---|---|---|---|
        |0|x||r|6|
        |1|1|1|r|1|
        |1|x|x|r|2|
        |2|1|2|r|3|
        |2|=|=|l|5|
        |3||1|l|4|
        |3|1|1|r|3|
        |3|=|=|r|3|
        |4|1|1|l|4|
        |4|=|=|l|4|
        |4|2|2|r|2|
        |5|2|1|l|5|
        |5|x|x|l|5|
        |5|1|1|l|5|
        |5|||r|0|
        |6|1||r|6|
        |6|=||S|6|
        
    - Dualzahlen-Plus 1
        
        101011 →
        
        |0|1|1|r|0|
        |---|---|---|---|---|
        |0|0|0|r|0|
        |0|||l|1|
        |1|1|1|l|1|
        |1|0|1|r|2|
        |2|1|0|r|2|
        |2|||s|2|
        
- Rado-Funktion
    
    ### erweitert: Algorithmus um Rado-Funktionen zu finden → Halteproblem
    
    2*(n-1)
    
    - n ist die Anzahl der Möglichkeiten in andere Zustände zu wechseln
        - s_0,1,2 = 12_6+4_2
            - 12 Möglichkeiten für jeweils + 2 Möglichkeiten je nicht Endzustand
                - 2 * s_0 + 2 * s_0
                - 2 * s_1 + 2 * s_1
                - 2 * s_2