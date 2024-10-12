

```python
name = input("What is your name? ") 
age = input("How old are you? ") 
height = input("How tall are you? ") 
print(f"Hi {name}, you're {age} years old and {height} tall.")
```

```python
from string import Template 
my_name="Bob" 
t=Template('Hey, $name!') 
print(t.substitute(name=my_name)) 
# 'Hey, Bob!'
```

