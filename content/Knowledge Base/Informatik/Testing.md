___
## Development Driven Testing
- write code according requirements -> test


___
## Test Driven Development
- writing tests before writing code
- just enough code to pass test
- test passed -> improve code
- next responsibility first in the form of a new test
- repeat
- red / green 
	- fails = red
	- pass = green

### Refactoring
- process of restructuring existing computer code without changing external behavior
- improving existing code, keeping functionality
-> improved code readability
-> reduced complexity
->improved maintainability
-> more expressive internal architecture

### Emergent Design
- code base increase -> more attention is consumed by refactoring
- design constantly evolving & under constant review
- technique to deliver high-quality code to testers

### Problems 
- detail in test creates a dependency on internal structure of object being tested
	- if requirements guide us to change an array to a hash, test will fail, even though the behavior hasn‘t changed
- can make test suites much more expensive to maintain & is the reason for tests to become ignored


## Behavior Driven Development
>BDD
>- Problem with testing an object‘s internal structure is that we‘re testing what an object **is** instead of what it **does**
>- Stakeholders usually don’t care that data is being persisted in an ANSI-compliant, relational database
>- They care that it’s in „the database“, but even then, they generally mean that it‘s stored somewhere and they can get in back

- focus on behavior instead of structure at every level of development
- object calculating, distance between cities etc. - all behavior
- changes the way we think about driving out of code
- think more about interactions between people & systems or between objects, that we do about structure of the objects

#### communication issues
- most software-development teams face 
- BDD aims to help communication by simplifying the language we use to describe scenarios in which the software will be used

-> BDD can exten TDD cycle or used on it‘s own

### given, when, then
- simple words that we use: application behavior object behavior
- easily understood by business analysts, testers & developers

- TDD is testing a White Box
	- you know how it works inside (Unit Test)
- BDD is testing a Black Box
	- can only see it from outside and interact with it


## Tools
[[../../Behave]]
