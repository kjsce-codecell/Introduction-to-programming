<h1 align="center"> Lists </h1>

## What are lists ?
> List is a collection in python. In most languages, it is called Array. We often need 'list' in our programs. Imagine you are writing a program to store name of every student in a class of 50 .  

> Elements in a list are stored in sequential order . Every element can be accessed by their index value .

```
Students                        [ "Chaitya",  "Neel" , "Ankit" , "Siddharth" ]

Forward Indexing                   0              1             2               3

Backward Indexing               -4             -3             -2            -1
```
### Declaring and Initializing a list

```Python
students = [ ]                           #  empty list

students_marks = list( )          #  empty list

player_scores = [ 78, 103, 200 , 57]            # >>> Initialized list with Integers

player_names = [ "Karan" , "Chirag" , "Jay" , "Raj" ]                   #  Initialized list with strings
```

> Unlike other programming languages ,  in python we can  Initialized or store elements in a list which are of different datatypes . For example,

```python

unknown_list = [ "google", "tensorflow", 73 , 37.5 ]            # works :P

print("Number of elements : "len(unknown_list))                # >>> Number of elements : 4

```

### Adding elements to the list

> We can add elements to the list by using append & insert methods  .

* Insert( index , element) - We use this method to add elements to a specific postion in a list .

* append( element ) - We use this method to add elements to the back( last postion ) of the list .

```python
scores = [ 1, 2 , 3 , 4 , 5 ]            # Initialized list with Integers

scores.append( 6 )                      # score = [ 1, 2, 3, 4, 5, 6]

score.append( 20 )              # score = [ 1, 2, 3, 4, 5, 6, 20]

score.insert( 0 , 8 )           # score = [ 8, 1, 2, 3, 4, 5, 6, 20]

score.insert( 4 , 4.5 )           # score = [ 8, 1, 2, 3, 4, 4.5, 5, 6, 20]

grades = [ "a" , "b" , "e"]             # Initialized list with characters .

grades[2] = "c"                 # >>> grades = [ "a", "b", "c"]


updated_grades = grades + [ "d", "e", "f"]              # >>> updated_grades = [ "a" , "b" , "c", "d", "e" ,"f"]

updated_grades.extend("g" ,"h")                 # >>> updated_grades = [ "a" , "b" , "c", "d", "e" ,"f" ,"g", "h"]
```

### Accessing elements from a list
> Elements of  a list are accessed using their index postion . [ list index starts from 0 ]

```python

 updated_grades = [ "a" , "b" , "c", "d", "e" ,"f"]

print(updated_grades[3])                # >>> d
print(updated_grades[-2])               # >>> e

print(updated_grades[3:])               # >>> ["d", "e", "f"]

print(updated_grades[2:4])              # >>> [ "c", "d"]

print(updated_grades[:])                # >>> [ "a" , "b" , "c", "d", "e" ,"f"]

# Get the index of the first item found
updated_grades.index('c')  # >>> 2
updated_grades.index('j')  # Raises a ValueError as "j" is not in the list

```

### Deleting elements from the list
> We use del [delete]  , remove  and pop methods to delete / remove elements from list .

* del list_name[index]- we use del keyword to remove an element from list which is mentioned / passed as index .

* list_name.remove(element) - here 'element' gets removed from the list if it's present .

* list_name.pop() - removes the last element from the list if the size of list is greater than 1 .

```python
li  = [ 1, 2, 2, 3]

del li[2]  # li is now [1, 2, 3]

li.append(4)            # li is now [1, 2, 3, 4]

li.remove(1)            # li is now [ 2, 3, 4 ]

li.pop()                       # li is now [ 2, 3]

```
### Traversing through a list
> We traverse ( access element in sequential order ) through a list by using loops .

* Using For loop :

```python

averages = [22.5 , 46.2 , 78.9 , 56.5 , 98.3 ]

for item in averages :
        print(item)
```

_output_

```
22.5
46.2
78.9
56.5
98.3
```

* Using While loop :

```python
scores  = [25, 89 , 90 , 45 , 87 ]

current = 0
end = len(score)

while current < end:
        print(scores[start])
        current +=1

```
_output_

```
25
89
90
45
87
```

> We can also traverse through a part of the list by simply using list comprehension techniques ( also mentioned above )

```python

grades = ["A+", "A", "B+", "B" , "C+" ,"C" ]

for item in grades[:4]:
        print(item)

```

_output_

```
A+
A
B+
B

```

### Performing various operations on list

* list_name.sort() - Sorts the elements in the list . By default the elements are sorted in ascending order .

*  list_name.reverse() - Reverses the order of elements present in the list  .

#### Implementation

```python
li = [ 4, 3, 1, 2 , 5 ]

li.sort()               # li is now [1 ,2 , 3 , 4 , 5]

li.reverse()            # li is now [5, 4, 3, 2, 1]

li = [ 4, 3, 1, 2 , 5 ]

li.sort(reverse=True)               # li is now [5, 4, 3, 2, 1]
print(sum(li))                  # >>> 15

li = ["c" ,"d" , "e" , "a" ,"b" ]

li.sort()                       # li is now ["a", "b" , "c" , "d" , "e"]
```
