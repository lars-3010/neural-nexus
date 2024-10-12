>methods

>each class can have instance functions
>	these can alter the object‘s state
>	Invoked by sending a message to the object
>	Object executes the message

### Beispiele
```python
def print_one(arg1):
 print(f"one arg1: {arg1}")
def print_two(arg1, arg2):
 print(f"two arg1: {arg1}")
 print(f"two arg2: {arg2}")
print_one("First!")
print_two("Hello","World")
```

```python
i = 0
numbers = []

while i < 6:
print(f"At the top i is {i}")
numbers.append(i)

i = i + 1
print("Numbers now: ", numbers)
print(f"At the bottom i is {i}")
print("")

print("The numbers: ")

for num in numbers:
print(num)
```
```python
def add(a, b): print(f"ADDING {a} + {b}") return a + b def subtract(a, b): print(f"SUBTRACTING {a} - {b}") return a - b def multiply(a, b): print(f"MULTIPLYING {a} * {b}") return a * b def divide(a, b): print(f"DIVIDING {a} / {b}") return a / b print("Let's do some math with just functions!") 

# Continuation of previous slide 
age = add(25, 6) 
height = subtract (200, 30) 
weight = multiply(40, 2) 
iq = divide(100, 2) 
print(f"Age: {age}, Height: {height}, Weight: {weight}, IQ: {iq}") 
print("Here is a puzzle.") 

what = add(age, subtract(height, multiply(weight, divide(iq, 2)))) 
print(f"That becomes: {what} Can you do it by hand?")
```

