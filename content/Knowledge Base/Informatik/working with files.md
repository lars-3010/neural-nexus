
### Reading from a File
```python
from sys import argv
script, filename = argv
txt = open(filename)
print(f"Here's your file {filename}:")
print(txt.read())
txt.close()
```
- open
	- opens specific file
	- content not loaded
	- call a function on txt named read

### writing to a file
```python
# Open a file and enable writing
file = open(filename, 'w')
# Write to the file
file.write("My new content")
# Closing the file to free up memory
file.close()
```



import files

```python
# this goes in fruit.py
orange = "Mmmh...oranges"
def apple():
 print("I AM APPLES!")
```

```python
import fruit

fruit.apple()
print(fruit.orange)
```
