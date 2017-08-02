<h1 align="center"> LOOPS </h1>

## Why LOOPS?
* Loops make our life easier by making it easier for us to perform repetetive task without having to actually write the same piece of code again and again that many times
* That is it helps you to perform a task as many as times you require depending on the condition you specify
## Different types of loop
* The two major kinds of loops that are used are
	* while loop
	* for loop

## While
* The basic idea behind while loop is
	__while some condition is true execute the following block of code__

### Implementation

```python
count=1 # initializes a counter variable equal to 1
while(count<=10): # checks if value of counter is less than equal to 15 if yes then execute the below
	print(str(count)+") I will do my homework everyday")
	count=count+1 #increments the value of counter otherwise it will remain less than 10 forever and thus infinite loop
print("Sorry")
```
 _Output_

```Python
1) I will do my homework everyday
2) I will do my homework everyday
3) I will do my homework everyday
4) I will do my homework everyday
5) I will do my homework everyday
6) I will do my homework everyday
7) I will do my homework everyday
8) I will do my homework everyday
9) I will do my homework everyday
10) I will do my homework everyday
Sorry

```

Here one should take care of the fact that lines which are indented inside the while are executed as and when the loop is true but the ones outside ie. `print(sorry)` is executed only once

## For
* The basic idea behind for loop is
	__to iterate through something and perform some action for each element of that something__

### Implementation
```python
#A girl has no name
list=['Jofrey','Cersei','Walder Frey','Meryn Trant','The Red Woman','Beric Dondarrion','Thoros of Myr','Ilyn Payne','The Mountain','The Hound'] # initialize a list with some values
for people in list: # assigns people a temporary value of elements in the list one by one and executes the code till all elemets in the list are iterated
	print(people) #prints the current value in the variable people each time
print("-Arya Stark") # You know who is it but look out for the indentation
```
_Output_
```
Jofrey
Cersei
Walder Frey
Meryn Trant
The Red Woman
Beric Dondarrion
Thoros of Myr
Ilyn Payne
The Mountain
The Hound
-Arya Stark
```
* For loop can be further combined with range function and used for looping through consecutive values in the range

### Implementation
```python
for x in range(1,11): #make a note of of the ending point of the list
	print(x,"Mississippi") # x takes one by one each value in the range
```
_Output_
```
1 Mississippi
2 Mississippi
3 Mississippi
4 Mississippi
5 Mississippi
6 Mississippi
7 Mississippi
8 Mississippi
9 Mississippi
10 Mississippi

```
for loop and while can in some situations be used interchangeably and thus comes down to which one you feel comfortable to work with

## Nesting
* for and while loops can also be nested within each other as many times required and as the situation demands
### Implementation
```python
count=1 #initializes count with value equal to 1
while(count<10): #checks if the count is less than 10
	print("Downloaded",str(10*count)+"% |",end="") #prints this for each time while is true
	for x in range(0,count): #prints '::' for each loop from 0 to current value of count
		print("::",end="")
	for x in range(count,10): # prints '  ' for each loop from current value of count upto 10
		print("  ",end="")
	print("|") #prints '|' once in while literally :)
	count=count+1 #increments the count so as to prevent infinite loop
print("Download Complete 100%")

```
_Output_
```
Downloaded 10% |::                  |
Downloaded 20% |::::                |
Downloaded 30% |::::::              |
Downloaded 40% |::::::::            |
Downloaded 50% |::::::::::          |
Downloaded 60% |::::::::::::        |
Downloaded 70% |::::::::::::::      |
Downloaded 80% |::::::::::::::::    |
Downloaded 90% |::::::::::::::::::  |
Download Complete 100%
```
