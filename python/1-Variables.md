<h1 align="center"> Variables </h1>


### What is Variable?

>A variable is nothing but a reserved memory location to store values. In other words a variable in a program gives data to the computer to work on.

>Python is completely object oriented, and not "statically typed". You do not need to declare variables before using them, or declare their type. Every variable in Python is an object.(C and Java users beware, this might seem a bit strange for you to digest :P)


### Declaration

>The operand to the left of the = operator is the name of the variable and the operand to the right of the = operator is the value stored in the variable.

```python
name = "Ankit"     # A string <- this is a comment by the way(just use #)
year = 2019        # An integer assignment
pointer = 10.0     # A floating point <- yes , this guy is amazing
```

### Multiple Assignments

>Python allows you to assign a single value to several variables simultaneously.

 _**Example**_
```python
a = b = c = 1
```
Here, an integer object is created with the value 1, and all three variables are assigned to the same memory location.

>Python  also can allows assigning of multiple objects to multiple variables.

 _**Example**_
```python
a,b,c = 1,2,"john"
```
Here, two integer objects with values 1 and 2 are assigned to variables a and b respectively, and one string object with the value "john" is assigned to the variable c.
