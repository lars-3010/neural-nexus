Tags: #🌿 
up:: [[../../Maps of Content/Java|Java]]

---
- **Aufzählung (enumeration)**
  - Mit dem Schlüsselwort `enum` eingeleiteter Programmbaustein zur Unterscheidung definierter Fälle oder Werte.
  - Spezielle Art von Objektklassen.
  - Können als Datentyp verwendet werden.

- **Aufzählungskonstante**
  - Bezeichnung eines möglichen Falls oder Wertes innerhalb einer Aufzählung.
  - Referenziert ein Aufzählungsobjekt.

- **Aufzählungsobjekt**
  - Objekt, das von einer Aufzählungskonstante referenziert wird.
  - Wird bei Deklaration von Aufzählungen erzeugt.
  - Speichert Information zur Aufzählungskonstante.

- **Aufzählungsreferenz**
  - Referenz auf ein Aufzählungsobjekt.



Enumerations (enum)
- **Datentyp** für **Unterscheidung definierter Fälle**
	- durch verschiedene Aufzählungskonstanten aufgezählt
- **Aufzählungskonstante**: Benennung eines möglichen Falls in einer Aufzählung
```java
<Modifizierer> enum <Aufzählungsname> {
<AUFZÄHLUNGSKONSTANTE1>,
<AUFZÄHLUNGSKONSTANTE2>,
...
<AUFZÄHLUNGSKONSTANTEn>;
… <Deklaration weiterer Größen>
}
```

- Für den Aufzählungsnamen gelten die gleichen Regeln wie für Klassennamen.
- Für die Aufzählungskonstanten gelten die gleichen Regeln wie für finale Variablen.
- Aufzählungskonstanten sind automatisch statisch und öffentlich.
- Es können optionale Parameter in Klammern hinter der jeweiligen Aufzählungskonstante angegeben werden.

Enums können auch zusätzliche Attribute und Methoden haben:
```java
public enum Planet {
	MERCURY(3.303e+23, 2.4397e6),
	VENUS(4.869e+24, 6.0518e6),
	EARTH(5.976e+24, 6.37814e6);
	
	private final double mass;   // in kilograms
	private final double radius; // in meters
	
	Planet(double mass, double radius) {
		this.mass = mass;
		this.radius = radius;
	}
	
	public double getMass() { return mass; }
	public double getRadius() { return radius; }
}
```
Wichtige Punkte zu Enums:

1. Jede Enum-Konstante ist eine Instanz der Enum-Klasse.
2. Enums können Konstruktoren, Methoden und Felder haben.
3. Enum-Konstruktoren sind immer private (implizit).
4. Enums implementieren automatisch java.lang.Comparable und java.io.Serializable.

#### Nützliche eingebaute Methoden für Enums:
- `values()`: Gibt ein Array aller Enum-Konstanten zurück.
- `valueOf(String name)`: Gibt die Enum-Konstante mit dem angegebenen Namen zurück.
- `ordinal()`: Gibt die Position der Enum-Konstante in ihrer Deklaration zurück (beginnend bei 0).
- `name()`: Gibt den Namen der Enum-Konstante als String zurück.
```java
DaysOfWeek today = DaysOfWeek.MONDAY; System.out.println(today); 
// Gibt "MONDAY" aus 
for (DaysOfWeek day : DaysOfWeek.values()) { 
	System.out.println(day); 
} 

Planet earth = Planet.EARTH; 
System.out.println("Earth's mass: " + earth.getMass());
```


# Note Structure
### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 

### Sources:
---
