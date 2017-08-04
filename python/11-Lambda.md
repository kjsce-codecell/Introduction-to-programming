# Lambda Functions

## Definition:  
Lambda functions are basically inline functions in python. That is the whole function in written in a single line.  
Key points about Lambda Function and what separates it from user defined functions in python:  
- No def keyword is needed to declare a lambda function.
- Lambda function has no return keyword either.
- Lambda functions are often called as anonymous functions. *(Since they have no name)*
- Lambda functions are small functions and at most time process only a single expression, unlike user defined functions which can be as long as the user requires. 
## Declaration:
So, here is how lambda functions are defined in python-  
```python
lambda x: x**2 #returns the square of the number passed to it.  
lambda x: x%3==0 #returns the numbers divisible by 3.  
```
Here lambda is the keyword and is always necessary, x is the argument passed to it, and the expression after colon *(:)* is what it is processing. Also, you can pass two arguments too, example:  

```python
lambda a,b: a+b #returns the sum of the passed variables
lambda a,b:a if a>b else b #returns greater of a or b
```

These were some of the ways to define a lambda function, now you might wonder how to use it ?  
Lambda functions are used mostly in, list functions, where you need to define functions for map or filter or reduce.  

## Calling a Lambda Function:
Although, you can also use it as normal functions as you use user defined functions in Python. Example-  
```python
temp=lambda x: x**2 #declaring lambda function and assigning it to temp.
print(temp(2)) #calling the temp with an argument, which is passed to lambda.
```
Output: 4.

That's it lambda is that easy, use the lambda keyword to define inline functions, and if you need to call it, assign it to a variable and call it from that.  
Now, let's look at how are lambda functions used in list functions such as map, filter, reduce. 

## Using Lambda for map, filter, reduce in lists:
```python
foo = [2, 18, 9, 22, 17, 24, 8, 12, 27]

print(list(filter(lambda x: x % 3 == 0, foo)))
#Here, the whole list is passed to the lambda element by element and it returns boolean value True or False if it is divisible or not, and that boolean value is used by the filter keyword to filter out the elements divisible by 3.
#[18, 9, 24, 12, 27]

print(list(map(lambda x: x * 2 , foo)))
#Whole list is passed to the lambda, element by element and each element is doubled and it is mapped and returned as a new list.
#[4, 36, 18, 44, 34, 48, 16, 24, 54]
```
The same way it can be ised for reduce as well.  

## Food For Thought:  
Take this piece of code, and predict it's output-  
```python 
def make_incrementor (n): return lambda x: x + n

f = make_incrementor(2)
g = make_incrementor(6)

print(f(42), g(42))
#44 48
print(make_incrementor(22)(33))
#55
```

The above code, defines a function make_incrementor, whichc returns a lambda function. So esentially, we are defining a function, that generates a function !  
Here, we are generating functions which perform a specific number of increments.  
f() is function, incrementing by 2, whereas g() is a function incrementing by 3.  
Also, the last line make_incrementor(22)(33), creates a function that increments by 22, and passes 33 to it. Hence, 55 is the output.  

This is the brief idea behind functional programming, where you work on functions, rather than objects like in object oriented programming.  

## Footnotes:    
- [Python Documentation](https://docs.python.org/3.5/tutorial/controlflow.html#lambda-expressions)
- [Yet Another Python Tutorial](https://pythonconquerstheuniverse.wordpress.com/2011/08/29/lambda_tutorial/)
- [Why are python lambda's useful?- StackOverflow](https://stackoverflow.com/questions/890128/why-are-python-lambdas-useful)





