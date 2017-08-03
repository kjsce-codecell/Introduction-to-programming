<h1 align="center"> Sets </h1>

## Introduction

>A set is an unordered collection, with no duplicate elements. Set contains operations such as union, intersection, difference, and symmetric difference.

## Syntax

>Set is initialized using the set() function or a curly brace. To create an empty set "{}" cannot be used as it will create empty dictionary, set() is used to create empty set.

<h3>Initialize:</h3>

>Make a new set and access elements.

```python
basket = {'apple', 'orange', 'apple', 'pear', 'orange', 'banana'} # Make a set
print(basket) # {'apple', 'orange', 'banana', 'pear'}
print ('pear' in basket) # Check if 'pear' in present in set. Prints True
print ('grapes' in basket) # False

set2 = set("Siddharth got 10.0 GPA") # Make a set using string
print(set2) # {'A', 'i', 'h', 'r', '1', ' ', 'g', 'o', 'd', '0', '.', 'P', 'G', 'S', 't', 'a'}
# Note that every character is inserted only once and they are not in order

set3 = set(["Neel", "loves", "python"]) # Make set using list
print(set3) # {'loves', 'Neel', 'python'}
# Note that characters are not inserted since it was a list of strings, not just one string
```
<h3>Set Operations:</h3>

>There are various operators to perform different set operations in sets.

```python
a = set('abracadabra') # {'a', 'r', 'd', 'b', 'c'}
b = set('alacazam') # {'a', 'z', 'l', 'c', 'm'}
print(a - b) # {'d', 'b', 'r'} (letters in a but not in b)
print(a | b) # {'c', 'd', 'l', 'a', 'm', 'b', 'z', 'r'} (letters in a or b or both)
print(a & b) # {'c', 'a'} (letters in both a and b)
print(a ^ b) # {'d', 'l', 'm', 'b', 'z', 'r'} (letters in a or b but not both)
```
## Functions

>There are many functions that can be used to perform operations on sets.

<h3>add()</h3>

>Used to add an element to a set.

```python
set1 = {1, 2, 3, "four", 5}
print(set1) # {1, 'four', 3, 2, 5}

set1.add(4)
print(set1) # {1, 2, 3, 4, 5, 'four'}
```

<h3>clear()</h3>

>Used to remove all elements from list

```python
set1 = {1,2,3}
set1.clear()
print(set1)
```

<h3>copy()</h3>

>Used to copy all elements of one set in other set.

```python
set1 = {1, 2, 3}
set2 = set1.copy()
print(set2) # {1, 2, 3}
```

<h3>remove()</h3>

>Used to remove an element from a set. If element is not found it gives error and program stops.

```python
set1 = {1, 2}
set1.remove(2)
print(set1) # {1}
set1.remove(3) # Raises Key Error
```

<h3>discard()</h3>

>Same as remove but does not give error if element is not present.

```python
set1 = {1, 2}
set1.discard(2)
print(set1) # {1}
set1.discard(3) # Does not give error
```

<h3>pop()</h3>

>Remove a random element form the set. It gives error if set is empty.

```python
set1 = set("Chirag")
print(set1.pop()) # h
print(set1.pop()) # r
print(set1.pop()) # i
```

## More

>There is a lot more to sets apart from this, especially functions. Explore [here](http://www.python-course.eu/python3_sets_frozensets.php)