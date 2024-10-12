

### Feature Files
- one feature per system functionality, making sure the Feature is specific to a single functionality in particular & as independent as possible from other functionalities
- best way to make feature files understandable -> use same language to describe functionality -> describing actions as the client would
>The most important thing is that the steps briefly describe what you want to do in the functionality and not how you want to do it

### Features and Scenarios
- statements must be written in order „Given-When-Then“ 
	- Given = precondition
	- When = action
	- Then = result / consequence of the action
- neither should „Should-Given-Then“ be replaced per stage, 
	- extend any of the sentences „And“
- sentences have to be consistent with each other & with description of the scenario
- as much as possible, not use many steps for a single scenario
- sentences: explanatory & brief
	- write the scenarios as we would like them to be presented to us
	- „But“ statement works the same as „Then“
		- it is used when we want to verify that no concrete result is observed
- very important: scenarios are as independent as possible 
-> scenarios can‘t be coupled

### Scenario Background
Folie 12

### Scenario Outline 
- input data is specified

### Doc Strings
- 