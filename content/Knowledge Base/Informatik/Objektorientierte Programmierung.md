Tags: #🌿 
up:: [[../../Maps of Content/Programmierung|Programmierung]]

---


## 1. Klassen und Objekte
---
Klassen sind Blaupausen für Objekte. Sie definieren Attribute (Daten) und Methoden (Funktionen), die ein Objekt haben wird.

### Beispiel:

```python
class ErrorCode:
    def __init__(self, code, description):
        self.code = code
        self.description = description
        self.translation = None
    
    def set_translation(self, translation):
        self.translation = translation
    
    def __str__(self):
        return f"Error {self.code}: {self.description}"

# Objekt erstellen
not_found = ErrorCode(404, "Not Found")
print(not_found)  # Ausgabe: Error 404: Not Found

# Methode aufrufen
not_found.set_translation("Seite nicht gefunden")
print(not_found.translation)  # Ausgabe: Seite nicht gefunden
```

### Anwendung im Projekt:
Sie könnten eine `ErrorCode`-Klasse verwenden, um jeden Fehlercode mit seinen zugehörigen Informationen (Beschreibung, Übersetzung) zu kapseln. Dies macht es einfacher, diese Informationen zusammen zu verwalten und zu manipulieren.

## 2. Vererbung
---
Vererbung ermöglicht es, eine neue Klasse basierend auf einer existierenden Klasse zu erstellen. Die neue Klasse (Unterklasse) erbt Attribute und Methoden der Basisklasse (Überklasse).

### Beispiel:

```python
class HTTPError(ErrorCode):
    def __init__(self, code, description, http_version):
        super().__init__(code, description)
        self.http_version = http_version
    
    def __str__(self):
        return f"HTTP {self.http_version} Error {self.code}: {self.description}"

# Objekt der Unterklasse erstellen
server_error = HTTPError(500, "Internal Server Error", "1.1")
print(server_error)  # Ausgabe: HTTP 1.1 Error 500: Internal Server Error
```

### Anwendung im Projekt:
Sie könnten spezifische Fehlertypen als Unterklassen definieren, z.B. `HTTPError`, `DatabaseError`, etc. Dies erlaubt es Ihnen, allgemeine Funktionalität in der Basisklasse zu definieren und spezifische Funktionalität in den Unterklassen hinzuzufügen.

## 3. Polymorphismus
---
Polymorphismus ermöglicht es, dass Objekte verschiedener Klassen auf die gleiche Schnittstelle reagieren können.

### Beispiel:

```python
def print_error_details(error):
    print(f"Code: {error.code}")
    print(f"Description: {error.description}")
    if hasattr(error, 'http_version'):
        print(f"HTTP Version: {error.http_version}")

# Verwendung mit verschiedenen Objekttypen
generic_error = ErrorCode(400, "Bad Request")
http_error = HTTPError(403, "Forbidden", "1.1")

print_error_details(generic_error)
print_error_details(http_error)
```

### Anwendung im Projekt:
Polymorphismus ermöglicht es Ihnen, verschiedene Arten von Fehlercodes einheitlich zu behandeln, während Sie trotzdem spezifische Funktionalitäten für bestimmte Fehlertypen beibehalten.

## 4. Kapselung
---
Kapselung bezieht sich auf die Bündelung von Daten und den Methoden, die auf diese Daten zugreifen, in einer einzigen Einheit (Klasse). Sie ermöglicht auch die Kontrolle des Zugriffs auf die internen Details eines Objekts.

### Beispiel:

```python
class ErrorCode:
    def __init__(self, code, description):
        self._code = code  # Konvention für "protected" Attribute
        self.__description = description  # "Private" Attribut
    
    @property
    def code(self):
        return self._code
    
    @property
    def description(self):
        return self.__description
    
    @description.setter
    def description(self, value):
        if isinstance(value, str) and value:
            self.__description = value
        else:
            raise ValueError("Description must be a non-empty string")

# Verwendung
error = ErrorCode(404, "Not Found")
print(error.code)  # Zugriff über Property
error.description = "Page Not Found"  # Setter wird aufgerufen
# error.__description  # Dies würde einen AttributeError verursachen
```

### Anwendung im Projekt:
Kapselung hilft Ihnen, die interne Implementierung Ihrer Klassen zu schützen und eine klare Schnittstelle für die Interaktion mit den Objekten zu definieren. Dies kann besonders nützlich sein, wenn Sie die Logik für die Verarbeitung oder Validierung von Fehlercodes und deren Übersetzungen kapseln möchten.

## 5. Abstrakte Klassen und Methoden
---
Abstrakte Klassen dienen als Basisklassen, die nicht direkt instanziiert werden können. Sie definieren eine gemeinsame Schnittstelle für eine Gruppe verwandter Klassen.

### Beispiel:

```python
from abc import ABC, abstractmethod

class BaseError(ABC):
    @abstractmethod
    def get_error_message(self):
        pass

class DatabaseError(BaseError):
    def __init__(self, code, message):
        self.code = code
        self.message = message
    
    def get_error_message(self):
        return f"Database Error {self.code}: {self.message}"

# Verwendung
db_error = DatabaseError("ORA-00001", "Unique constraint violated")
print(db_error.get_error_message())
```

### Anwendung im Projekt:
Abstrakte Klassen können nützlich sein, um eine gemeinsame Schnittstelle für verschiedene Arten von Fehlern zu definieren, während Sie die spezifische Implementierung den konkreten Unterklassen überlassen.

# Note Structure
### Relation
---
- **Where from**:  
- **Similar**: 
- **Leads to**: 
- **Opposite**: 

### Sources:
---
