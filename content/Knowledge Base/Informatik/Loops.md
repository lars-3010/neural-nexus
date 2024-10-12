>control flow statement for specifying iteration
>allows code to be executed repeatedly
>Python supports all common types of loops (For, While, …)
>often used in combination with list

- for i in x
    
    ```python
    x = [42, 5, 10]
    for i in range(len(x)):
		print(x[i])print('finish')
    ```

- break
    
    ```python
    for i in range(0,20):    
    	if i > 15:        
    		break    
    	print(i)
    	print('finish')
    ```
    
    - interrupts the loop
- continue
    
    ```python
    for i in range(0,20):    
    	if i%2 == 1:        
    	continue    
    	print(i)print('finish')
    ```
    
    - Statements werden übersprungen, die in der Bedingung erfasst wurden
    - skip statements, which are defined in a condition

### while-loops
>runs until expressions is False
>problem: sometimes they don‘t stop