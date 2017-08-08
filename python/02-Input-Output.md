<h1 align="center"> Input & Output </h1>

## How to Input ?

#### Input an `string` or a `character` from console

```Python
#input() method here assigns name variable with entered string or character

name = input("Enter your name : ")        
```
#### Input an `integer` or `float` from console
```Python
# int(input()) method here takes input from the console converts it into integer and assigns it to variable roll_no

roll_no = int(input("Enter your Roll Number: "))       

average = float(input("Enter average: "))       # to input floating value
```

## How to Output ?

#### Printing out a `string`
```Python
print("I'm Python. Nice to meet you!")  # >>> I'm Python. Nice to meet you!
```
> By default the print function also prints out a `newline` at the end.Use the optional argument end to change the end string.

```Python
print("Hello, World", end="!")  # >>> Hello, World!
```

#### Printing `numbers` with a `string`
> (Notice the space after 'is' in the output )

> Case 1: here we print string and then integer
```Python
print("My jersey number is",10)  # >>> My jersey number is 10
```

> Case 2: here we convert integer 10 into string  and then print all of it at once
```Python
print("My jersey number is "+str(10))  # >>> My jersey number is 10
```

> Case 3: here we have a variable integer value and a string
```Python
roll = int(input("Enter roll number: "))        # >>> Enter roll number : 102
print("Roll number is :" , roll)                     # >>> Roll number is : 102
```

> Case 4: here string is variable
```Python
name = input("Enter name: ")    # >>> Enter name: cheetah
print("My name is " + name)      # >>> My name is cheetah
```

#### Printing out `float` values

```Python
var = 10.5782
print("average is %.2f"%(var))             # >>> average is 10.58
print("now average is %.6f"%var)        # >>> now average is 10.578200
```
