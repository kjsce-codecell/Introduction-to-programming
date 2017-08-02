<h1 align="center"> Conditionals </h1>

## What are conditionals?
* In computer science, conditional statements, conditional expressions and conditional constructs are features of a programming language, which perform different computations or actions depending on whether a programmer-specified boolean condition evaluates to true or false.

## What are differnt types of conditional statements in python?
* A few commonly used conditional statements are -
	* if
	* if-else
	* if-elif-else

## IF
* One of the basic conditional statements that are used
* It decides whether to execute a given line or skip it depending on condition given to it

###  Implementation
```python
#following piece of code uses if to check who studies harder
Ankit=10.00 #ofc it is his CGPA
Siddharth=9.80 #not bad right??
if(Ankit>Siddharth): #checks if the given condition is true
	print("Ankit studies harder than Siddharth") #gets executed if the above statement is true
if(Siddharth>Ankit): #checks if the given condition is true
	print("Siddharth studies harder than Ankit")
```
Output
```
Ankit studies harder than Siddharth
```
the indentattion here is the key and all the statements that are indented inside the for will be executed regardless of the condition

## IF-Else
* It is an extension to the if condition
* It helps in deciding which statement to execute when a given condition is true and exucutes other set of them when the condition is false  

###  Implementation
```python
#following piece of code uses if-else to check who studies harder
Ankit=10.00
Siddharth=9.80
if(Ankit>Siddharth): #checks if the given condition is true
	print("Ankit studies harder than Siddharth")
else: #makes the below statements to execute if the above condition is false
	print("Siddharth studies harder than Ankit")
```
Output
```
Ankit studies harder than Siddharth
```
## IF-Elif-Else
* It is one step further to if-else
* It can be used to check for multiple conditions and deciding the set of statements that should be executed in case of any condition being true

### Implementation

```python
#following piece of code uses if-elif-else to check who studies harder
Ankit=10.00
Siddharth=9.80
if(Ankit>Siddharth): #checks if the given condition is true
	print("Ankit studies harder than Siddharth")
elif(Siddharth>Ankit): #checks if the given condn is true provided all condn above it are false 
	print("Siddharth studies harder than Ankit")
else: #makes the below statements to execute if all the above condition is false
	print("Both of them study equally hard")
```
Output
```
Ankit studies harder than Siddharth
```
One can insert any number of elif statements but only one if and else for a given set linked conditions
<br>If in situation we have more then one condition being true the first one from the top is executed and the rest are left unchecked and hence statements skipped

## Note
* These conditional statements can be even nested one inside others to the check conditions at various levels
### Implementation

```python
#following piece of code uses nested conditionals to check who studies harder among 3 people
Ankit=10.00
Siddharth=9.80
Chaitya=9.90 #legend for a reason
if(Ankit>Siddharth): #PRIMARY checks if the given condition is true
	if(Ankit>Chaitya): #SECONDARY checks for condition provided primary condn is true
		print("Ankit studies harder than Siddharth and Chaitya both")
	else: #executes if the primary condition is true but the secondary is false
		print("Ankit studies harder than Siddharth but Chaitya studies harder")
else:
	print("Siddharth Studies harder than Ankit")
```
Output
```
Ankit studies harder than Siddharth and Chaitya
```
Here which else and elif corresponds to which if is decided by the indentation and hence it plays a important role and must be taken care of. 
<br><br>
* Also a single condition can check multiple condition using logical operators 
### Implementation

```python
#following piece of code uses conditionals and logical operators to check who studies harder among 3 people
Ankit=10.00
Siddharth=9.80
Chaitya=9.90
if(Ankit>Siddharth and Ankit>Chaitya): #executes if both the conditions are true
	print("Ankit studies harder than Siddharth and Chaitya both")
elif(Siddharth>Ankit and Siddharth>Chaitya):
	print("Siddharth Studies harder than Ankit and Chaitya")
else:
	print("Chaitya Studies harder than Ankit and Siddharth")
```
Output
```
Ankit studies harder than Siddharth and Chaitya
```