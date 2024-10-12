Tags: #🗺️  
up:: [[Programmierung]]

---
Projekt kompilieren:
- Die integrierte Build-Funktion von VS Code nutzen (⇧⌘B oder Ctrl+Shift+B).

### Klausurvorbereitung
---
- Aufgabe 1 & 2: (30 Punkte)
	- Fragen zum Verständnis der Grundbegriffe 
		- bezogen auf Java
		- objektorientierte Programmierung im Allgemeinen
	- Aufgabe 1: Single/Multiple Choice ähnlich PingoQuestions
	- Aufgabe 2: Fragen zum Grundverständnis der objektorientierten Programmierung
	- Danach: 5 weitere Aufgaben, z.B. aus einem der folgenden Bereiche (ggf. auch in Kombination
		- Speicherbilder, Speicherverwaltung, Felder, Notationskonventionen, Syntax, statische Klassen, Objektklassen, Konstruktoren, Methoden, Vererbung, Java-API, Aufzählungstypen, Ausnahmen, Schnittstellen, Generizität(nur Grundverständnis der Generics, ohne Collections, Listen etc.
- MusicianApp


## Objektorientierte Programmierung
---
- [[Kapselung]]
	- Bündelung von Attributen und Methoden in einer Einheit (Objektklasse bzw. Objekt)
	- Zugriffsbeschränkung: Kein direkter Zugriff auf Objektattribute von außen erlaubt
	- Zugriffsmethoden: Verwendung von Methoden für den Zugriff (in Java: getter/setter)
	- Zweck: Verhinderung des direkten Zugriffs auf die Daten eines Objektes
- Geheimnisprinzip / Sichtbarkeit
	- Grundsatz: Nur notwendige Informationen und Methoden nach außen bereitstellen
	- Sichtbarkeit: Instanzvariablen und interne Methoden bleiben privat
	- Öffentliche Schnittstelle: Nur explizit als public deklarierte Instanzmethoden sind sichtbar
	- Datenschutz: Alles andere bleibt das "Geheimnis" der Objektklasse
- Vererbung
	- Konzept: Übertragung von Attributen und Methoden von übergeordneten auf nachgelagerte Klassen
	- Bedeutung: Wichtigstes Merkmal der objektorientierten Programmierung
	- Struktur: Ermöglicht die Bildung von Klassenhierarchien
- Generalisierung & Spezialisierung
	- Prinzip: Zuordnung von Attributen und Methoden zu Ober- und Unterklassen
	- Optimierung: Attribute und Methoden so weit wie möglich in Oberklassen platzieren
	- Vorteile: Reduzierung von Wiederholungen und Fehleranfälligkeiten
	- Hilfsmittel: Verwendung abstrakter Klassen zur Bildung von Klassenhierarchien
- Polymorphie
	- ermöglicht es, Objekte verschiedener Typen als Objekte einer gemeinsamen Überklasse zu behandeln

	- Unterklasse Zugang zu Methoden der Oberklasse
		- kann auch Methoden der Oberklasse überschreiben
			- spezielle Implementierungen haben
	- ich füge 2 Sachen zusammen, damit ich was neues habe um etwas zu verbessern
		- ich kreuze 2 Tiere um eine Entwicklung zu nutzen
	- Modifizierung
	- Definition: Fähigkeit von Objekten verschiedener Klassen, gleiche Funktionen auszuführen
	- Möglichkeiten:
	    - Nutzung der Methode der Oberklasse
	    - Überschreiben der Methode der Oberklasse
	- Abstrakte Methoden: Können in Oberklassen verwendet werden
	- Methodenaufruf: Prüfung auf speziellere Implementierungen, die Vorrang haben
- [[../Knowledge Base/Informatik/Objekte|Objekte]]


- variable’s value is updated trough the “**=”** operator
- once defined a variable’s type can never change
- **object-oriented language**, requires all functions to be defined in a class
- “**class**” defines a class
- function within a class is referred to as a method
- each method can have zero or more parameters
- all parameters must explicitily typed, there is no type inference for parameters → return type must be made explicit
- values are returned from functions using “**return**”
- “**public**” access modifier must be added to allow a method to be called by other classes
- variable is defined by explicitly spefiying its type “int **explicitVar** = 10”


```java
public abstract class Musician extends Person{
	public Musician(String name, int yearOfBirth) {
		super(name, yearOfBirth);
	}
	public abstract boolean isSoloist();
	public String toString() {
		return super.toString();
	}
}
```


### Klassendatei
---

- Instanzvariablen
	- Attribute
```java
public class Student {
	private int id;
	private String name;
```

- Konstruktor (Abfragen)
	- setup Tool
	- Methode
```java
public Student(int id, String name) {
	if (id>10000 && id <= 99999)
		this.id = id;
	else {
		System.out.println("Fehler bei der id-
			Eingabe, id muss zwischen 10001
			und 99999 liegen. Id wurde auf 0
			gesetzt.");
		this.id = 0;
	}
	this.name = name;
}
```

- Konstruktoren (mit Id-Vergabe)
```java
public Student(String name) {
	this.id = nextId++;
	this.name = name;
}
```

- Getter
	- Methoden
```java
public int getId() {
	return this.id;
}
```

- Setter
	- Methoden
```java
public void setId(int id) {
	this.id = id;
}
```

- toString: Überschreiben 
	- Polymorphie
	- Methode aus Oberklasse ändern
```java
@Override
public String toString(){
	return "Student [id=" + id + ", name=" + name + "]";
}
```

- toString: Überladen
	- andere Parameter
	- Polymorphie
```java
public String toString(String type) {
	if (type == "long")
		return "Student "+ name +" hat die Id “ + id +".";
	else
		return toString();
}
```

- Klassenmethoden
```java
static int getNoOfAvailableIds() {
	return LAST_ID-nextId+1;
}

static int getNoOfAssignedIds() {
	return nextId-FIRST_ID;
}
```

### App
---

```java
public class StudentApp {
	public static void main(String[] args) {
		Student student5 = new Student(100, "Andrea Schmidt");
		Student student6 = new Student(10006);
		System.out.println(student5.getName() + " ("
							+ student5.getId() + ")");
		System.out.println(student6.getName() + " ("
							+ student6.getId() + ")");
	}
}
```

### Exceptions
---
- Code Anfang Vorlesung 9
```java
public class IdRangeException extends Exception {
	
}

...

public static int getNextId() throws IdRangeException {
	if ... {
		...
	}
	else {
		throw new IdRangeException("Id Overflow");
	}
}
```

```java
public class InvalidAgeException extends Exception { 
	private int age; 
	
	public InvalidAgeException(int age) { 
		super("Ungültiges Alter: " + age); 
		this.age = age; 
	} 
	
	public InvalidAgeException(String message, int age) { 
		super(message); 
		this.age = age; 
	} 
	
	public int getAge() { 
		return age; 
	} 
}
```

```java
public class DivisionByZeroSelfmade extends Exception { 
	public DivisionByZeroSelfmade(){ 
		super("Bist du dumm? Hast du nicht Aufgepasst? Null? Teilen?"); 
	} 
	public DivisionByZeroSelfmade(String errorDescription){ 
		super(errorDescription); 
	} 
}

public class ExceptionApp { 
	public static void main(String[] args) throws Exception { 
		int a = 25; 
		int b = 0; 
		int c; 
		int rest; 
		if (b==0){ 
			throw new DivisionByZeroSelfmade(); 
		} else { 
		c = a/b; 
		rest = a-c*b;
		} 
	System.out.println("Ergebnis; " + a + ":" + b + " = " + c +", Rest " + rest); 
	} 
}
```

### Arrays
---
- looping through an Array
```java
// ohne new = feste Anzahl von Elementen, Werte bekannt
String[] cars = {"Volvo", "BMW", "Ford", "Mazda"};
for (int i = 0; i < cars.length; i++) {
	System.out.println(cars[i]);
}

// mit new = dynamische Array-Erstellung (kann erst deklariert, 
// später initialisiert werden)
// entries kann man benutzen um durchzuloopen
int[] array1 = new int[] { 1, 2, 3, 5};
for(int entries : array1){
	System.out.println(entries);
}

// array.length Beispiel
int[] array1 = new int[] { 1, 2, 3, 5};
for(int i = 1; i <= array1.length; i++){
	System.out.println(array1[1]);
}

// letzten Wert ausgeben
private static int getLastValue(int... values) {
	return values[values.length-1];
}
//test it in main method via:
System.out.println(getLastValue(1,2,34,66,99));
```

### [[../Knowledge Base/Informatik/Aufzählungen|Aufzählungen]]
```java
<Modifizierer> enum <Aufzählungsname> {
<AUFZÄHLUNGSKONSTANTE1>,
<AUFZÄHLUNGSKONSTANTE2>,
...
<AUFZÄHLUNGSKONSTANTEn>;
… <Deklaration weiterer Größen>
}
```

```java 
public enum Voice {
    SOPRANO("Sopran", Gender.FEMALE),
    ALTO("Alt", Gender.FEMALE),
    TENOR("Tenor", Gender.MALE),
    BASS("Bass", Gender.MALE);

    private String germanName;
    private Gender gender;

	// privater Konstruktor
    private Voice(String germanName, Gender gender) {
        this.germanName = germanName;
        this.gender = gender;
    }

    @Override
    public String toString() {
        return this.germanName;
    }
    
    public Gender getGender() {
        return this.gender;
    }
}
```
### Java API
---
```java
@Override
public String toString() {
	return name + ", " + yearOfBirth + ", " + getAge() + ", ";
}

@Override
public int getAge() {
	return LocalDate.now().getYear() - yearOfBirth;
}
```

### Schnittstellen, Interfaces
---
Eine Klasse, die eine Schnittstelle implementiert, muss auch die in der Schnittstelle enthaltenen Methoden implementieren. 

- Definition der Schnittstelle
```java
public interface Fahrzeug { 
	void fahren(); 
	void tanken(); 
	int getGeschwindigkeit(); 
}
```

- Implementierung der Schnittstelle
```java 
public class Auto implements Fahrzeug {
    private int geschwindigkeit = 0;

    @Override
    public void fahren() {
        System.out.println("Auto fährt");
        geschwindigkeit = 60;
    }

    @Override
    public void tanken() {
        System.out.println("Auto wird betankt");
    }

    @Override
    public int getGeschwindigkeit() {
        return geschwindigkeit;
    }
}

public class Fahrrad implements Fahrzeug {
    private int geschwindigkeit = 0;

    @Override
    public void fahren() {
        System.out.println("Fahrrad fährt");
        geschwindigkeit = 15;
    }

    @Override
    public void tanken() {
        System.out.println("Fahrrad braucht keinen Treibstoff");
    }

    @Override
    public int getGeschwindigkeit() {
        return geschwindigkeit;
    }
}
```

- Anwedung der Schnittstelle
```java
public class FahrzeugTest {
    public static void main(String[] args) {
        Fahrzeug auto = new Auto();
        Fahrzeug fahrrad = new Fahrrad();
  
        fahren(auto);
        fahren(fahrrad);
    }

    public static void fahren(Fahrzeug fahrzeug) {
        fahrzeug.fahren();
        fahrzeug.tanken();

        System.out.println("Geschwindigkeit: " + fahrzeug.getGeschwindigkeit() + " km/h");
        System.out.println();
    }
}
```

### Generics
---
Unit.class

Grundüberlegung
- Statt mehrere Collection-Klassen StudentCollection, LecturerCollection, … zu schreiben, wird nur eine Collection Klasse Collection\<T\> geschrieben, in der die Collection-Methoden generisch programmiert sind (generische Klasse). 
* T ist dabei ein Typparameter, für den bei Nutzung der Collection-Klasse Objektklassen als Typ eingesetzt werden können.
* Statt einer Klasse StudentCollection nutzen Sie die Klasse Collection\<Student\> oder statt LecturerCollection die Klasse Collection\<Lecturer\>

Verwendung
* Eine generische Klasse kann wie nichtgenerische Klassen als Datentyp verwendet werden. 
* Bei der Verwendung der generischen Klasse sind jedoch für jeden Typparameter Datentypen einzusetzen.
* Es dürfen dabei beliebige Referenztypen (Klassen, Feldtypen, Aufzählungen, Schnittstellen) eingesetzt werden.
* Einfache Datentypen (int, boolean, char...) können nicht eingesetzt werden, dafür können hier Wrapper-Klassen genutzt werden.
``` java
public enum Unit {
	LITER,
    KILO,
    PIECE;
}
```

Apps
```java
public class TripleApp {
    public static void main(String[] args) {
	    //Triple String
        Triple<String> tripleString = new Triple("a", "b", "c");
        System.out.println(tripleString);
        tripleString.shiftLeft();
        System.out.println(tripleString);
        tripleString.shiftRight();
        System.out.println(tripleString); 
        // Triple Integer
        Triple<Integer> tripleInt = new Triple(1,8,25);
        System.out.println(tripleInt);
        tripleInt.shiftLeft();
        System.out.println(tripleInt);
        tripleInt.shiftRight();
        System.out.println(tripleInt);  
        //Triple ENUM
        Triple<Unit> tripleUnit = new Triple(Unit.KILO, Unit.LITER, Unit.PIECE);
        System.out.println(tripleUnit);
        tripleUnit.shiftRight();
        System.out.println(tripleUnit);
        tripleUnit.shiftLeft();
        System.out.println(tripleUnit); 

    }
}
```

``` java
public class Triple<T> {
    private T first;
    private T second;
    private T third;
    //Konstruktor
    public Triple(T first, T second, T third) {
        this.first = first;
        this.second = second;
        this.third = third;
    }
    //Getter & Setter
    public T getFirst() {
        return first;
    }
    public void setFirst(T first) {
        this.first = first;
    }

	... 
	
    }
	//shiftLeft
    public void shiftLeft() {
        T tmp = first;
        first = second;
        second = third;
        third = tmp;
    }
    //shiftRight
	public void shiftRight() {
        T tmp = third;
        third = second;
        second = first;
        first = tmp;
    }

    public String toString() {
        return "(" + this.first + ", " + this.second + ", " + this.third + ")";
    }
}
```

## Notationskonventionen
---
- Klassen und Interfaces:
	- PascalCase (auch UpperCamelCase genannt)
	- Beginnen mit einem Großbuchstaben
	- Beispiel: `public class MyClass {}`
- Methoden und Variablen:
	- camelCase (auch lowerCamelCase genannt)
	- Beginnen mit einem Kleinbuchstaben
	- Beispiel: `public void myMethod() {}`
- Konstanten:
	- Komplett in Großbuchstaben
	- Wörter durch Unterstriche getrennt
	- Beispiel: `public static final int MAX_VALUE = 100;`
- Pakete:
	- Komplett in Kleinbuchstaben
	- Beispiel: `package com.mycompany.myproject;`
	
- Einrückung:
	- Üblicherweise 4 Leerzeichen oder 1 Tab pro Ebene
- Klammern:
    - Öffnende geschweifte Klammer in derselben Zeile wie die Deklaration
    - Schließende geschweifte Klammer in einer eigenen Zeile
    
- Javadoc-Kommentare:
    - Für öffentliche Klassen, Methoden und Felder
    - Beginnen mit `/**` und enden mit `*/`
- Inline-Kommentare:
    - Für komplexe Codeabschnitte
    - Beginnen mit `//`

## Klassen
---
- hat Methoden und Attribute
### final
---
- kann nicht erweitert oder vererbt werden
- Das Ziel ist es, die Vererbungshierarchie an dieser Stelle zu beenden
- `public final class MeineKlasse { ... }`

### static
---
- Nur innere Klassen (nested classes) können als static deklariert werden.
- Eine statische innere Klasse gehört zur äußeren Klasse und nicht zu einer Instanz der äußeren Klasse.
- berechnet irgendwas
- `public class AeussereKlasse { public static class InnereKlasse { ... } }`
- Gehören zur Klasse, nicht zu Objektinstanzen
- Können ohne Objekterstellung aufgerufen werden
- Haben keinen Zugriff auf nicht-statische Mitglieder der Klasse
- Häufig für Utility-Funktionen oder Factory-Methoden verwendet

- 
### abstrakt
---
- haben keine Instanzvariablen
- Methodenkopf ohne Inhalt
	- 
- Konstruktor nur Variablen von der Oberklasse, von der geerbt wird
	- mit super
# Java Glossary
---
- **Attribute**
  - Maßgebliche Eigenschaften aller Instanzen einer Objektklasse.
  - Variablen

- **Abstrakte Klasse**
  - Mit `abstract` deklarierte Klasse.
  - Von ihr können keine Objekte (Instanzen) erzeugt werden.
  - Kann als Datentyp verwendet werden.
  - Mögliche Werte sind Referenzen auf Instanzen von Unterklassen der abstrakten Klasse.

- **Abstrakte Methode**
  - In einer (zumeist abstrakten) Klasse mit dem Schlüsselwort `abstract` eingeleiteter Methodenkopf ohne angefügtem Methodenrumpf.
  - Direkte Unterklassen müssen die abstrakte Methode als Methode bereitstellen.

- **Anweisungsblock (kurz: Block)**
  - Mit `{ ... }` geklammerte Folge von Anweisungen.
  - Variablen können deklariert werden, sind nur im jeweiligen Block sichtbar und verwendbar.

- **Ausnahme (exception)**
  - Objektklasse Exception oder Unterklasse der Objektklasse Exception.
  - Dient zur Aufzeigung und Behandlung von Sonder- oder Fehlersituationen.

- **Ausnahmebehandlung**
  - Für einen mit `try` eingeleiteten Anweisungsblock nachfolgende, mit `catch` eingeleitete Anweisungsblöcke.
  - Werden im Falle von geworfenen Ausnahmen ausgeführt.

- **Ausnahmeweitergabe (kurz: Weitergabe)**
  - Methoden können die Behandlung einer Ausnahme an die Aufrufer weitergeben.
  - Im Methodenkopf mit `throws` ... angegeben.

- **Datentyp**
  - Menge möglicher Werte (Wertebereich) und anwendbare Operationen.
  - Einfache Datentypen: `boolean`, `char`, `short`, `int`, `long`, `float`, `double`.
  - Weitere definierbare Datentypen: Objektklassen, Aufzählungen, Feldtypen, Schnittstellen.

- **Dynamische Bindung**
  - Auswahl und Ausführung von Instanzmethoden wird erst zur Laufzeit ermittelt.
  - Basiert auf Polymorphie und Überschreiben von Methoden.

- **Erweiterung (extends)**
  - Klassen können Klassen erweitern, Schnittstellen können Schnittstellen erweitern.
  - Bei Klassen mit `extends` eingeleitet.
  - Bei Schnittstellen können mehrere Schnittstellen erweitert werden.

- **Feld**
  - Speicherobjekt mit sequentiell angeordneten Feldpositionen.
  - Werte des gleichen Datentyps.
  - Feste Länge, mit `new`-Operator erzeugbar.

- **Feldreferenz**
  - Referenz auf ein Feld.

- **Feldtyp**
  - Datentyp, der Feldreferenzen als mögliche Werte hat.
  - Anwendbare Operationen: Längenabfrage, Zugriffe auf Feldpositionen.

- **Finale Klasse**
  - Mit `final` deklarierte Klasse.
  - Keine Unterklassen möglich.

- **Finale Methode**
  - Mit `final` deklarierte Methode.
  - Kann nicht in Unterklassen überschrieben werden.

- **Finale Variable**
  - Mit `final` deklarierte Variable.
  - Wert wird bei Initialisierung festgelegt und kann nicht geändert werden.

- **Geheimnisprinzip**
  - Instanzvariablen und interne Methoden bleiben privat und nach außen verborgen.
  - Nur public-Instanzmethoden werden nach außen sichtbar gemacht.

- **Generische Klasse**
  - Klasse mit einem oder mehreren Typparametern.
  - Typparameter sind Platzhalter für Datentypen.

- **Generische Methode**
  - Methode mit einem oder mehreren Typparametern.
  - Typparameter können anstelle von Datentypen verwendet werden.

- **Generische Schnittstelle**
  - Schnittstelle mit einem oder mehreren Typparametern.
  - Typparameter sind Platzhalter für Datentypen.

- **Instanz**
  - Synonym für Objekt.

- **Instanzmethode**
  - Auf Objekte anwendbare Methode.
  - Kann den Zustand von Objekten ändern und/oder Daten liefern.

- **Instanzvariable**
  - Variable innerhalb einer Objektklasse.
  - Speichert für jedes Objekt einen aktuellen Datenwert.

- **Klasse (class)**
  - Programmbaustein, in dem Programmgrößen deklariert werden.

- **Klassendiagramm**
  - Schematische Darstellung einer Objektklasse.
  - Dreigeteiltes Rechteck: Name, Attribute, Operationen.

- **Klassenmethode**
  - Mit `static` deklarierte Methode ohne Objektbezug.
  - Kann auf Klassenvariablen zugreifen, nicht auf Instanzvariablen.

- **Klassenvariable**
  - Mit `static` deklarierte Variable in einer Klasse.
  - Nicht in Objekten enthalten, sondern nur einmal in der Klasse.

- **Konstruktor**
  - Methode zum Initialisieren neu erzeugter Objekte.
  - Weist Instanzvariablen Anfangswerte zu.

- **Methode**
  - Funktionen in Java.
  - Bestehen aus Methodenkopf und Methodenrumpf.
  - Arten: Instanzmethoden und Klassenmethoden.

- **Methodenkopf**
  - Spezifiziert Bauart und Verwendbarkeit einer Methode.
  - Umfasst: Modifizierer, Rückgabetyp, Name, Parameterliste, Ausnahmeliste.

- **Methodenrumpf**
  - Anweisungsblock einer Methode.
  - Implementiert die Methode.

- **Methodensignatur**
  - Formale Festlegung der Aufrufbarkeit von Methoden.
  - Umfasst: Name, Anzahl, Datentypen und Reihenfolge der Parameter.

- **Modifizierer**
  - Schlüsselwörter zur Steuerung von Sichtbarkeit und weiteren Festlegungen.
  - Beispiele: `abstract`, `final`, `private`, `protected`, `public`, `static`.

- **Oberklasse**
  - Klasse, die von einer anderen Klasse erweitert wird.
  - Direkte oder indirekte Oberklasse möglich.

- **Oberschnittstelle**
  - Schnittstelle, die von einer anderen Schnittstelle erweitert wird.
  - Direkte oder indirekte Oberschnittstelle möglich.

- **Objekt (Synonym: Instanz)**
  - Speicherobjekt, das gemäß Bauplan der Objektklasse aufgebaut ist.
  - Dient zur Darstellung von realen oder programmtechnischen Objekten.
  - Mit `new`-Operator erzeugbar.

- **Objektklasse**
  - Programmbaustein, der einen Referenztyp definiert.
  - Definiert den "Bauplan" für gleichartige Objekte.
  - Umfasst Datenaufbau und anwendbare Operationen.

- **Objektreferenz**
  - Referenz auf ein Objekt einer Objektklasse.

- **Operationen**
  - Maßgebliche Fähigkeiten aller Instanzen einer Objektklasse.

- **Paket (Package)**
  - Logische Zusammenfassung von Programmbausteinen.
  - Kann Unterpakete enthalten.
  - Dient zur Strukturierung großer Softwareprojekte.

- **Polymorphie (Vielgestaltigkeit)**
  - Referenzen können auf Instanzen der Klasse oder Unterklassen verweisen.
  - Klassenzugehörigkeit oft erst zur Laufzeit ermittelbar.

- **Programmbaustein (kurz: Baustein)**
  - Oberbegriff für Aufzählung, Klasse, Schnittstelle.
  - Können in separaten Dateien oder in anderen Bausteinen enthalten sein.

- **Programmgröße (kurz: Größe)**
  - Oberbegriff für alles, was deklariert werden kann.
  - Umfasst: Aufzählung, Klasse, Methode, Schnittstelle, Variable.

- **Referenz**
  - Verweis (Zeiger) auf ein Speicherobjekt.

- **Referenzparameter**
  - Methodenparameter mit Referenztyp als Datentyp.

- **Referenzrückgabetyp**
  - Referenztyp als Rückgabetyp einer Methode.

- **Referenztyp**
  - Datentyp, bei dem die möglichen Werte Referenzen sind.
  - Gilt für: Aufzählungen, Feldtypen, Objektklassen, Schnittstellen.

- **Referenzvariable**
  - Variable mit einem Referenztyp als Datentyp.

- **Schnittstelle (Interface)**
  - Programmbaustein, der einen Referenztyp definiert.
  - Enthält Methodenvorgaben und default-Methoden.
  - Kann von Objektklassen implementiert werden.

- **Schnittstellenimplementierung (implements)**
  - Beziehung zwischen Klassen und Schnittstellen.
  - Klasse definiert mit `implements`, welche Schnittstellen sie implementiert.

- **Sichtbarkeit**
  - Festlegung, wo eine Programmgröße sichtbar und verwendbar ist.
  - Steuerung durch Modifizierer wie `public`, `protected`, `private`.

- **Speicherobjekt**
  - Bei Programmausführung angeforderter und genutzter Speicherbereich.
  - Für Objekte und Felder.

- **Standardmethode**
  - In einer Objektklasse erwartete Methoden:
    1. Konstruktor
    2. set- & get-Methoden
    3. equals(...)
    4. toString()

- **Statische Klasse**
  - Klasse mit ausschließlich Klassenvariablen und Klassenmethoden.
  - Keine Instanzvariablen und Instanzmethoden.

- **Überladen (einer Methode)**
  - Mehrere Methoden gleichen Namens mit unterschiedlicher Parameterstruktur.
  - Für unterschiedliche Parameterkonstellationen.

- **Überschreiben**
  - Re-Implementierung einer Methode, die schon in Oberklasse vorhanden ist.

- **Unterklasse**
  - Klasse, die eine andere Klasse erweitert.
  - Direkte oder indirekte Unterklasse möglich.

- **Unterschnittstelle**
  - Schnittstelle, die eine andere Schnittstelle erweitert.
  - Direkte oder indirekte Unterschnittstelle möglich.

- **Variable**
  - Programmgröße mit Namen & Datentyp.
  - Dient zur Speicherung von Daten.
  - Unterscheidung von Instanzvariablen und Klassenvariablen in OOP.

- Wrapper-Klasse
	- Integer / Triple statt int / T
		- ist nur für Generics benötigt
		- keine primitiven Datentypen

- **Zeichenkette (String)**
  - Vordefinierte Objektklasse in Java.
  - Stellt Methoden zum Arbeiten mit Zeichenketten bereit.
  - Spezielle Sprachelemente: Literale, length-Operator, Konkatenation.

- **Zusicherung (assertion)**
  - Mit Bedingung versehene `assert`-Anweisung.
  - Kontrolliert, ob eine Bedingung erfüllt ist.
  - Kann im Java-Laufzeitsystem ein- und ausgeschaltet werden.

- **Zustand (eines Objekts)**
  - Datenbelegung aller Instanzvariablen eines Objektes.


# Note Structure
### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 

### Sources:
---



