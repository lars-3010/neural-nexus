
- Kommentare
	`# This is a comment`

- [[strings]]

- String-formatting
	```python
    name = 'Bob'
    print(`Hello, {}`.format(name))
    ```
	- String interpolation / f-strings
		```python
    name = 'Bob'
    print(`Hello, {}`.format(name))
    
    a=5
    b=10
    print(f`Five plus ten is {a + b} and not {2 * (a + b)})
    ```
- template strings (standard library)
	```python
    from string import template
    my_name=`Bob`
	t=Template(`Hey, $name!)
	print(t.substitute(name=my_name))
    ```


- input()
	- Built-In Function
	- takes input from command line

- len()-Funktion
    
    - Ermittlung der Länge einer Zeichenkette
    
    ```python
    name = 'Extrameile'
    lenght = len(name)
    print(lenght)
    ```
    
- upper()-Methode
    
    wandelt eine Zeichenkette in Großbuchstaben um
    
    ```python
    name = 'Extrameile'
    name_groß = name.upper()
    print(name_groß)
    ```
    
- lower()-Methode
    
    Gegenteil von upper()-Methodefrt


## Codeblock-Template
```python
def hello_world():
	return "Hello, world!"
```



## unsortiert
### Befehle / Anweisung

- print()
    
    Anweisung an Computer, einen Wert in einem Bereich console (Shell) anzuzeigen (Ausgabe)
    
    Kann Variablen anzeigen → Wert wird angezeigt
    
- for
    
    **for** Variable **in** Liste
    
- len
    
    - Verwendung mit dem Listennamen
        
        → gibt die Anzahl der Elemente in einer Liste aus
        

---

- Werte
    
    - Strings mit “…” & Zahlen ohne
    - Boolean Werte: True & False
- Ausdruck
    
    Funktion: hinzufügen von String-Werten
    
    - werden zu Werten → können Berechnungsergebnisse speichern
    - Variablen und Werte können zugewiesen werden
- Variable
    
    Funktion: Informationen merken
    
    - steht am Anfang
        
    - Ohne Leerzeichen
        
    - ist Status, Wert kann geändert werden
        
    - Beispiele:
        
        - _ (Snake Case) → Mehrere Wörter
            - Home_city
        - = → Wert darin speichern
            - City = „Miami“
        - „(Wort)“ = String
- Negationsoperator
    
    not
    
- Gleichheitsoperator
    
    - ==
    - Überprüft / vergleicht, ob 2 Zahlen gleich sind
- Ungleichungsoperator
    
    !=
    
- Operatoren
    
    - kleiner als Operator (<) & kleiner-Gleich Operator (≤)
    - größer als Operator (>) & größer-Gleich Operator (≥)
- float
    
    Zahlen mit Nachkommsstellen
    
- f-strings
    
    formatierte Strings zeigen das Hinzufügen eines Strings zu einer Zahl fehlerfrei ah
    
- bedingte Anweisungen
    
    - elif: spezifische Bedingung nach if-Block, wenn Bedingungen davor =False
    - if … and … :
    - if … or … :
- Self-Assigning
    
    Daten ändern sich
    
- for Schleifen
    
    ```python
    x = [42, 5, 10]for i in range(len(x)):    print(x[i])print('finish')
    ```
    
    - gibt die Liste aus
- break
    
    ```python
    for i in range(0,20):    
    	if i > 15:        
    		break    
    	print(i)
    	print('finish')
    ```
    
    - bricht Schleife ab
- continue
    
    ```python
    for i in range(0,20):    
    	if i%2 == 1:        
    	continue    
    	print(i)print('finish')
    ```
    
    - Statements werden übersprungen, die in der Bedingung erfasst wurden
- Funktionen mit Parametern
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/50a1e696-ef76-4860-9b6f-593ff76eada1/Untitled.png)
    
- Default Werte für Funktionsargumente
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a10b3cc5-ee8d-481a-84bf-025daf56d6c5/Untitled.png)
    
- einfacher Integer Input
    
    ```python
    alter = input("Wie alt bist du?")
            alter2 = int(alter) + 5
            print("in 5 Jahren " + str(alter2))
    ```
    
- Dateien lesen
    
    ```python
    if __name__ == "__main__":
        f = open('text.txt', 'r')
        print(f.read())
    ```
    
    - w = write
    - r+ = lesen + schreiben
    - a = anhängen
    - r = lesen
    - b = Lese-& Schreibzugriff in Binärform
- Dateien schreiben
    
    ```python
    if __name__ == "__main__":
        f = open('text.txt', 'w')
        f.write('\\n4. Zeile')
        f = open('text.txt', 'r')
        print(f.read())
    ```
    
    ---
    
    oder mit close dazwischen
    
    ```python
    if __name__ == "__main__":
        f = open('text.txt', 'w')
        f.write('\\n4. Zeile')
        f.close()
        f = open('text.txt', 'r')
        print(f.read())
        f.close()
    ```
    
- Gültigkeitsbereich von Variablen
    
    ```python
    def f():
        def local():
            var = "local text"
        def do_nonlocal():
            nonlocal var 
            var = "non local text"
        def do_global():
            global var
            var = "global text"
        var = "text"
        local()
        do_nonlocal()
        do_global()
        print("after init: ", var)
    
    f()
    print("global", var)
    ```
    
    localvar = local text
    
    nonlocalvar = nonlocal text
    
    globalvar = global text
    
- Klassen
    
    ```python
    class MyClass:
        zahl = 42
        string = "Zeichenkette"
    
        def do_something(self, neueZahl):
            self.zahl = neueZahl
    instanz = MyClass()
    instanz.do_something(1337)
    print(instanz.zahl)
    ```
    
- Konstruktoren
    
    ```python
    class MyClass:
        zahl = 42
        string = "Zeichenkette"
    
        def __init__(self, BuchstabeNeu='a'):
            self.buchstabe = BuchstabeNeu
    
        def do_something(self, neuezahl):
            self.zahl = neuezahl
    
    instanz = MyClass()
    instanz.do_something(1337)
    print(instanz.buchstabe)
    ```
    
- Instanz- und Klassenvariablen
    
    - außen: Klassenvariablen
    - innen: Instanzvariablen
    
    ```python
    class MyClass:
        zahl = 42
        string = "Zeichenkette"
        list = []
    
        def __init__(self, BuchstabeNeu='a'):
            self.buchstabe = BuchstabeNeu
    
        def do_something(self, neuezahl):
            self.zahl = neuezahl
            self.list.append(neuezahl)
    
    instanz = MyClass('z')
    instanz2 = MyClass('a')
    instanz.do_something(1337)
    print(instanz.list)
    ```
    
    - Alternative mit Liste als Klassenvariable
        
        ```python
        class MyClass:
            zahl = 42
            string = "Zeichenkette"
        
            def __init__(self, BuchstabeNeu='a'):
                self.buchstabe = BuchstabeNeu
                self.list = []
        
            def do_something(self, neuezahl):
                self.zahl = neuezahl
                self.list.append(neuezahl)
        
        instanz = MyClass('z')
        instanz2 = MyClass('a')
        instanz.do_something(1337)
        print(instanz.list)
        ```
        
- append()
    
    - etwas dranhängen in einer Liste
- pop()
    
    removes the last element of a list
    
    (value at a specific index)
    

---

Listen

- Datensammeln in einer Liste
    
    […]
    
    - Daten in einer Liste sammeln
- Position eines Elements in einer Liste
    
    Index
    
- Element zu einer Liste hinzufügen / entfernen
    
    - am Ende hinzufügen: Listenname.**append()**
    - am Anfang hinzufügen: Listenname.**insert()**
    - entfernen: Listenname.**pop()**
- Maximum, Minimum finden
    
    - max()
    - min()
- Planung
    
    - nach Videos Projekt umsetzten
    - Text Adventure
- nicht nur alleine Programmieren → Teamfähigkeit
    
- Kommentare dazuschreiben um Code verständlich zu machen