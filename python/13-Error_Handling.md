<h1 align="center"> Error Handling </h1>


## Exceptions

>Even if a statement or expression is syntactically correct, it may cause an error when an attempt is made to execute it. **Errors detected during execution are called exceptions**

#### Some examples :

1.You ask for an integer but input value of other datatype
```python 
>>> n = int(input("Please enter a number: "))
Please enter a number: 23.5

Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ValueError: invalid literal for int() with base 10: '23.5'
```

2.The famous divide by zero exception
```python
>>> 10 * (1/0)

Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ZeroDivisionError: division by zero
```

3.Using undeclared variable
```python 
>>> 4 + spam*3

Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'spam' is not defined
```

4.Concatenation of string and integer doesn't work in python. 
```python
>>> '2' + 2

Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: Can't convert 'int' object to str implicitly
```
You can handle this situation by doing this
```python
'2'+str(2)
``` 

## Catching the notorious exceptions

>Exceptions handling in Python is very similar to Java. The code, which harbours the risk of an exception, is embedded in a try block. But whereas in Java exceptions are caught by catch clauses, we have statements introduced by an "except" keyword in Python.

As we saw an exception above where the user was entering a wrong datatype . With the aid of exception handling, we can write robust code for reading an integer from input:

```python
while True:
    try:
        n = input("Please enter an integer: ")
        n = int(n)
        break
    except ValueError:
        print("No valid integer! Please try again ...")
print("Great, you successfully entered an integer!")
```

It's a loop, which breaks only, if a valid integer has been given. It works like this :
>The while loop is entered. The code within the try clause will be executed statement by statement. If no exception occurs during the execution, the execution will reach the break statement and the while loop will be left. If an exception occurs, i.e. in the casting of n, the rest of the try block will be skipped and the except clause will be executed. The raised error, in our case a ValueError, has to match one of the names after except. In our example only one, i.e. "ValueError:". After having printed the text of the print statement, the execution does another loop. It starts with a new input(). 

>A try statement may have more than one except clause for different exceptions. But at most one except clause will be executed with different types of exceptions such as :

* ArithmeticError
* IOError
* ValueError

>You can even have more than one type of exception caught in a single except like this:
```python
except (IOError, ValueError):
```


## Rise of the Exceptions

>Python allows you to raise an exception by yourself .

>The sole argument to raise indicates the exception to be raised. This must be either an exception instance or an exception class (a class that derives from Exception). If an exception class is passed, it will be implicitly instantiated by calling its constructor with no arguments:

```python
raise ValueError  # shorthand for 'raise ValueError()'
```
>If you need to determine whether an exception was raised but don’t intend to handle it, a simpler form of the raise statement allows you to re-raise the exception:

```python
>>> try:
...     raise NameError('HiThere')
... except NameError:
...     print('An exception flew by!')
...     raise
...
An exception flew by!
Traceback (most recent call last):
  File "<stdin>", line 2, in <module>
NameError: HiThere
```
If no expressions are present, raise re-raises the last exception that was active in the current scope. If no exception is active in the current scope, a RuntimeError exception is raised indicating that this is an error.

## Creator of the Exceptions

Just like khaleesi , You can be the creator yourself. Just the story is changed a little bit , here you create exceptions... Get ready to become the mother of exceptions

>Programs may name their own exceptions by creating a new exception class. **Exceptions should typically be derived from the Exception class, either directly or indirectly**.

```python
# A python program to create user-defined exception

# class MyError is derived from super class Exception
class MyError(Exception):

	# Constructor or Initializer
	def __init__(self, value):
		self.value = value

	# __str__ is to print() the value
	def __str__(self):
		return(repr(self.value))

try:
	raise(MyError(3*2))

# Value of Exception is stored in error
except MyError as error:
	print('A New Exception occured with value: '+str(error.value))
```

Output:
```python
A New Exception occured with value: 6
```



## Defining clean-up actions(Roke tujhko aandhiyan ya zameen aur aasman Paayega jo lakshya hai tera)

As the title suggest :P , we will be defining a block of code which will run whether an exception occurs or not.

>The try statement has another optional clause which is intended to define clean-up actions that must be executed under all circumstances. For example:

```python
>>> try:
...     raise KeyboardInterrupt
... finally:
...     print('Goodbye, world!')
...


Goodbye, world!
KeyboardInterrupt
Traceback (most recent call last):
File "<stdin>", line 2, in <module>
```

## what **_else_**

>The try ... except statement has an optional else clause. An else block has to be positioned after all the except clauses. An else clause will be executed if the try clause doesn't raise an exception. 

```python
>>> try:
...     sambha_kitne_aadmi_the = 'ek huzoor' 
... else:
...     print('Your code is good to go :D')
...


Your code is good to go :D
```