<h1 align="center"> User Defined Functions </h1>

In all programming and scripting language, a function is a block of program statements which can be used repetitively in a program. It saves the time of a developer. In Python concept of function is same as in other languages. There are some built-in functions which are part of Python. Besides that, we can define functions according to our need.

In Python, a user-defined function's declaration begins with the keyword ```def``` and followed by the function name.
The function may take arguments(s) as input within the opening and closing parentheses, just after the function name followed by a colon.
After defining the function name and arguments(s) a block of program statement(s) start at the next line and these statement(s) must be indented.
Here is the syntax of a user defined function.

## Syntax
```
def function_name(argument1, argument2, ...) :
    statement_1 
    statement_2
    ....
 ```
## Call a function

Calling a function in Python is similar to other programming languages, using the function name, parenthesis (opening and closing) and parameter(s). See the syntax, followed by an example.

## Syntax
```
function_name(arg1, arg2)
```
### Example :
```
def avg_number(x, y):  
    print("Average of ",x," and ",y, " is ",(x+y)/2)  
avg_number(3, 4)  
```
Output :
```
Average of 3 and 4 is 3.5
```
## Explanation :

1. Lines 1-2 : Details (definition) of the function. 
2. Line 3 : Call the function.
3. Line 1 : Pass parameters : x = 3, y = 4
4. Line 2 : Print the value of two parameters as well as their average value.

## Function without arguments :

The following function has no arguments.
```
def function_name() :
    statement_1 
    statement_2
    ....
```
### Example :

```
def printt():  
    print("I Love CodeCell")  
    print("I Love CodeCell")  
    print("I Love CodeCell")  
printt()  
```   
Output :
```
I Love CodeCell
I Love CodeCell
I Love CodeCell
```
## Explanation :

1. Lines 1-4 : Details (definition) of the function. 
2. Line 5 : Call the function.
3. Line 1 : No parameter passes.
4. Line 2-4 : Execute three print statements.

## The Return statement in function

In Python the return statement (the word return followed by an expression.) is used to return a value from a function, return statement without an expression argument returns none. See the syntax.
```
def function_name(argument1, argument2, ...) :
    statement_1 
    statement_2
    ....
    return expression

function_name(arg1, arg2)
```
### Example :

The following function returns the square of the sum of two numbers.
```
def nsquare(x, y):  
    return (x*x + 2*x*y + y*y)  
print("The square of the sum of 2 and 3 is : ", nsquare(2, 3))  
 ```              
Output :
```
The square of the sum of 2 and 3 is : 25
```
## Explanation :

1. Lines 1-2 : Details (definition) of the function. 
2. Line 3 : Call the function within a print statement.
3. Line 1 : Pass the parameters x = 2, y = 3
4. Line 2 : Calculate and return the value of (x + y)
