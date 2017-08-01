<h1 align="center"> Input & Output </h1>

### How to Input ?
* Simple way to get `input ` from console

```Python
var = input("Enter some data: ")        # => to input string

roll_no = int(input("Enter your Roll Number: "))        # => to input integer

average = float(input("Enter average: "))       # => to input floating value
```
### How to Output ?

* Printing out a string
```Python
print("I'm Python. Nice to meet you!")  # => I'm Python. Nice to meet you!
```
* By default the print function also prints out a `newline` at the end.Use the optional argument end to change the end string.

```Python
print("Hello, World", end="!")  # => Hello, World!
```

* Printing `numbers` with a `string` . (Notice the space after 'is' in the output. )

`Case 1:` here we print string and then integer
```Python
print("My jersey number is",10)  # => My jersey number is 10
```
`Case 2:` here we convert integer 10 into string  and then print all of it at once
```Python
print("My jersey number is "+str(10))  # => My jersey number is 10
```

`Case 3:` here we have a variable integer value and a string
```Python
roll = int(input("Enter roll number: "))
print("Roll number is :",roll)
```

`Case 4:` here string is variable
```Python
name = input("Enter name: ")
print("My name is "+name)       
```

* Printing out float variables

```Python
var = 10.5782
print("%.2f"%(var))             # => 10.57
print("%.6f"%var)               # => 10.578200
```
