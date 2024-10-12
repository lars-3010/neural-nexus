represents entity inside real world
>	can have multiple & different instances
>		A can is a pet
>		A pet is not necessarily a cat
>		A dog can also be a pet



- classes are like modules
- way to take a grouping of functions & data, place them inside a container 
	- ->you can access them with the . (dot) operator

- Beispiel
	```python
	class Mammal
	:
	 def breath
	(self):
	 print
	("inhale and exhale"
	)
	class Cat
	(Mammal):
	 def speak
	(self):
	 print
	("meow"
	)
	henry = Cat()
	henry.breath()
	henry.speak()
	```
