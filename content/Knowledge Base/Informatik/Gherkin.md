>language used in [[Behave]]
>small language with well-defined syntax
>super simple


```Gherkin
Feature: pay bill on-line 

 In order to reduce the time I spend paying bills 
 As a bank customer with a checking account 
 I want to pay my bills on-line 

Scenario: pay a bill 
	Given checking account with $50 
	And a payee named Acme 
	And an Acme bill for $37
	When I pay the Acme bill 
	Then I should have $13 remaining in my checking account
	And the payment of $37 to Acme should be listed in Recent Payments
```
everything up to and including the scenario declaration is treated as documentation (not executable)
- subsequent lines are executable steps

- allows to add some context to scenarios in a single feature
- much like a scenario containing a number of steps
- difference is when it is run
- background is run before each of your scenarios

```Gherkin
Feature: Multiple site support 
	As a Mephisto site owner 
	I want to host blogs for different people 
	In order to make gigantic piles of money 

Background: 
	Given a global administrator named "Greg" 
	And a blog named "Greg's anti-tax rants" 
	And a customer named "Dr. Bill"
	And a blog named "Expensive Therapy" owned by "Dr. Bill" 
	
Scenario: Dr. Bill posts to his own blog 
	Given I am logged in as Dr. Bill 
	When I try to post to "Expensive Therapy" 
	Then I should see "Your article was published."
```


### Data tables
