> [[../Informatik einsortieren/Basics/Functions]] 


- Source
	[The purest form of coding, where bugs are near impossible - YouTube](https://www.youtube.com/watch?v=HlgG395PQWw&list=WL&index=8)
# closures
> a <font color="#d99694">closure</font> is a poor man's <font color="#4bacc6">object</font> 
> 	& an <font color="#4bacc6">object</font> is a poor man's closure
```python
f(a){
	 (b) = a + b
}
```
- simple anonymous functions, that are defined in other functions
- can access data from the parent scope
- the full scopes remain in memory - until the last closure returns

# Higher order functions
> - creates reusable and isolated modules
> -> writing code more declaredly
- filter()
- sort()
- map()


# Immutability (and side-effects)
- side effects: uses data from outer scope / changes data in outer scope
- removing the variability from variables


# Currying and objects with closures
> - breaks up multiple arguments of a function into their own function cause, that we then chain together
> - achieved by the scope memory ability of closures -> each argument stay will stay in memory until the chain completes

- using closures to create something resembling an object
	- the first function in the chain acts as a kind of object constructor
	- where most of the internal data is defined
		- this data is privately scoped to the constructor function -> encapsulated by it
			![[Organisation/Bilder/Pasted image 20230918205508.png]]

		- returning a closure to provide external access to this private data
			- ![[Organisation/Bilder/Pasted image 20230918205644.png]]

	- this can be used for simple tasks, such as pre-computing & storing the result of expensive operations -> memoization
	- or returning multiple named closures to access and manipulate the internal data in more complex ways
		- ![[Organisation/Bilder/Pasted image 20230918205916.png]]
	- further solodifying it in its object-like behaviours

## The purely functional paradigm
> everything is declarative, deterministic and ideally unchanging, pretty much forever
> roots in the mathematical world
> we work primarily with types and expressions, where the following rules apply:
> 	- Code is generally evaluated rather than executed -> interesting new optimization abilities
> 		- lazy evaluation & automatic parallelization
> 	- Immutability is enforced everywhere -> when making changes to data, it's done by computing a new constant based off of an existing constant
> 	- to keep functions pure -> the mere thought of a side effect is punishable by the most horrific torture imaginable ...  having to learn MONADS


## Benefits and Drawbacks
> immutability of the functional paradigm forces to think more strictly about how data is passed around
> -> helping to ensure that changes don't happen unexpectedly
> guides us in forming readable code that's highly modular -> maintainable
> potentially being a bit harder to optimize, depending on where in the branch using functional
> can be a challenge to transition to a more declarative approach if you're already used to imperative styles of programming