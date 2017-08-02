<h1 align="center"> Dictionaries </h1>

## Introduction

>A dictionary is used to store a key value pair. A key is a variable which is assigned a value in the dictionary.

>The keys are unique in the dictionary while a value may not be. Values can be on any type but the keys need to be [immutable](https://codehabitude.com/2013/12/24/python-objects-mutable-vs-immutable/).

## Syntax

Each key is separated from its value by a colon (:), the items are separated by commas, and the whole thing is enclosed in curly braces. An empty dictionary without any items is written with just two curly braces, like this: {}.

<h3>Initialize:</h3>
Start a new dictionary with some elements and access them.

```python
love = {'Sam': 'Gilly', 'Tormund': 'Brienne', 'Jaime': 'Cersei', 'Hound': 'Chicken'}
#Access
print(love['Sam']) #Gilly
print(love['Hound']) #Chicken
```
<h3>Update Dictonary:</h3>
Add new entries to a dictionary, delete an entry and clear and delete the entire dictionary.

```python
#Take the dictionary declared above.

#Add new entry
love['Jorah'] = 'Daenerys'
love['Ramsay'] = 'Sansa' #OOPS..

#Remove an entry
del love['Ramsay']
print(love['Ramsay']) #Gives Error

#lets remove everything
love.clear()
print(love['Tormund']) #Gives Error that Tormund is not a key

#lets delete love
del love
print(love['Jaime']) #Gives Error that love is not defined
```
## Properties
<h3>Keys are unique:</h3>
Really?? Just jump to the code.

```python
#Consider love

#Lets use same key twice
love['Littlefinger'] = 'Catelyn'
love['Littlefinger'] = 'Sansa'
print(love['Littlefinger']) #Sansa
```
Yes, the latest value gets assigned.

<h3>Keys must be immutable:</h3>
The following are some immutable objects:

* int
* float
* decimal
* complex
* bool
* string
* tuple
* range
* frozenset
* bytes

## Functions
These are called directly and the dictionary object is passed as (function(dict))
<h3>len()</h3>
Gives the total length of the dictionary. This would be equal to the number of items in the dictionary.

```python
dict = {'Key': 'Value'}
print(len(dict)) #1
```
<h3>str()</h3>
Gives a string representation of the dictionary.

```python
#Consider love
print(str(love)) #Try yourself
```
## Methods
These are called using the dictionary object like (dict.method())

<h3>clear()</h3>
Removes all elements of dictionary.

<h3>copy()</h3>
Returns a copy of the dictionary, which can be stored in another dictionary.

```python
dict1 = {'Key': 'Value'}
dict2 = dict1.copy() #Now dict2 has all elements of dict1
```

<h3>get()</h3>
It returns the value of the key or None if not found. You can also set a default parameter that will be returned if the key is not found.

```python
#consider love
print(love.get('Jaime')) #Cersei
print(love.get('Bronn')) #None
print(love.get('Bronn', 'You wouldn\'t know her')) #You wouldn't know her
```

<h3>keys()</h3>
It gives a list of all keys of the dictionary.

```python
print(str(love.keys())) #Try yourself
```

<h3>values()</h3>
It gives a list of all values of the dictionary.

```python
print(str(love.values())) #Try yourself
```
<h3>More</h3>

> Explore other functions of dictionary [here](https://www.tutorialspoint.com/python3/python_dictionary.htm)