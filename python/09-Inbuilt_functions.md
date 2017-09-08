<h1 align="center"><a href="#"> Inbuilt Functions </a></h1>

* The Python interpreter has a number of functions and types built into it that are always available.
* There is no need to import any extra modules in order to use them.
* A few functions that we will be covering here are-
	* Map
	* Filter
	* Sort
	* Max/Min
	* Reduce

## Map
* It iterates through all the elements of an iterable and applies some specific function to each element of that iterable.
* With multiple iterables, the iterator stops when the shortest iterable is exhausted

### syntax
```python
r = map(func, seq)
#takes each element in seq 
#applies func function to them
#inserts them to r

```
### implementation
```python

#for a single list involved
a=['2011-12-22 46:31:11','2011-12-20 20:19:17', '2011-12-20 01:09:21']
dt=list(map(str.split, a)) #split function is applied to each element and it returns a list corresponding to each element
print(dt)

#for multiple lists involved
a = [1,2,3,4] 
b = [17,12,11,10]
print(list(map(lambda x,y:x+y, a,b)))
#goes through each element of a,b 
#adds them correspondingly till one of the lists end

```
Output
```
[['2011-12-22', '46:31:11'], ['2011-12-20', '20:19:17'], ['2011-12-20', '01:09:21']]
[18, 14, 14, 14]
```
## Filter
* As the name justifies,filter creates a list of elements for which a function returns true.

### Syntax
```python
filter(filter_fnc,list)
```
### implementation
```python
def fn(x):
	return (x<0) #(x<0) is condition automatically returns true or false
number_list = range(-10, 10)
less_than_zero = list(filter(fn, number_list))
print(less_than_zero)
```
Output
```
[-10, -9, -8, -7, -6, -5, -4, -3, -2, -1]
```

## Sort/Sorted
* Python lists have a built-in sort() method that modifies the list in-place and a sorted() built-in function that builds a new sorted list from an iterable
* There are many ways to use them to sort data and there doesn't appear to be a single, central place in the various manuals describing them
* The key difference between both is that sorted returns a new list whereas sort changes the original list itself.

### syntax
```python
list.sort()
sorted(container)#sort in ascending order
sorted(list,reverse=True)#sort in descending order
sorted(list,key=<insert the key>)#sort in ascending order of the key set
```  
### implementation
```python

a = [5, 2, 3, 1, 4]
a.sort() #sort() function is specific to lists
print(a)

chir={2: 'D', 1: 'B', 4: 'B', 3: 'E', 5: 'A'}# declaring a dictionary
for ind in sorted(chir): #sorted is general approach, although return type is a list
	print("{}:{}".format(ind,chir[ind]),end=" ")
print()
for ind in sorted(chir,reverse=True): #note the order is descending of the keys
	print("{}:{}".format(ind,chir[ind]),end=" ")
def gv(key):
	return chir[key];
print()
for ind in sorted(chir,key=gv,reverse=True): #note the order is descending of the values of each key
	print("{}:{}".format(ind,chir[ind]),end=" ")

```
Output
```
[1, 2, 3, 4, 5]
1:B 2:D 3:E 4:B 5:A 
5:A 4:B 3:E 2:D 1:B 
3:E 2:D 1:B 4:B 5:A

```
## max/min
* Returns the greatest/smallest item in an iterable or the smallest of two or more arguments.
* It can also be made to make use of key argument as used in sort function
### implementation
```python
list = [1, 4, 3, 5,9,2]
print(max(list)) #returns maximum value of list
print(min(list)) #returns minimum value in the list
print(max(list[2:-2])) #returns max value combined with slicing 
print(min(list[4:])
print(max(4,2,3,5))
print(min(7,2,1,8,4))
```
Output
```
9
1
5
9
5
1

```

## Reduce
* Reduce is a really useful function for performing some computation on a list and returning the result.
* It applies a rolling computation to sequential pairs of values in a list
>note this not an inbuilt function as such because it needs to be imported from func tools but is pretty useful.

### implementation
```python
#Normal way to find product of elements in a list
product = 1
list = [1, 2, 3, 4]
for num in list:
    product = product * num

#Using reduce function to do so
from functools import reduce
def func(x,y):
	return x*y
product = reduce(func, [1, 2, 3, 4])

```
Output
```
24
24
```



