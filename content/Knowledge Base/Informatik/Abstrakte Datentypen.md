Tags: #🌿 
up:: [[../../Maps of Content/Java|Java]]

---
Datentyp, der durch seine Operationen und das Verhalten dieser Operationen definiert wird, ohne die konkrete Implementierung zu spezifizieren.
In Java können ADTs auf verschiedene Weise realisiert werden:
1. **Interfaces**: Definieren eine Sammlung von abstrakten Methoden ohne Implementierung.
2. **Abstrakte Klassen**: Können sowohl abstrakte als auch konkrete Methoden enthalten.
3. **Klassen mit privaten Datenfeldern und öffentlichen Methoden**: Kapseln die interne Implementierung und stellen nur die definierten Operationen nach außen zur Verfügung.

```java
public interface Stack<T> { 
	void push(T item); 
	T pop(); 
	T peek(); 
	boolean isEmpty(); 
}
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
