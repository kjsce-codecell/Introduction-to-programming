<h1 align="center"> Modules </h1>
> Modules are explicitly designed to encourage and enhance the portability of Python programs .<br>
The Python installers for the Windows platform usually include the [entire standard library](https://docs.python.org/3/library/index.html) and often also include many additional components.<br> Bulit in modules which will be covered in this documentaion are

* math - for mathematical functions
* random - to generate pseudo-random numbers
* sys - system specific parameters and functions
* os - operating system interfaces


> In addition to the standard library, there is a growing collection of several thousand components (from individual programs and modules to packages and entire application development frameworks), available from [PyPI](https://pypi.python.org/pypi) , which you are free to explore after getting comfortable using some of the built in modules .

### How do we use them ?
> We can import modules which are available under [standard library](https://docs.python.org/3/library/index.html) by using _from_ , _as_ and _import_  keyword .

```python
import module_name     # imports all the functions of math library
import module_name  as short_name       # same as above but shorting the name math to mt
```

> Importing specific fuctions from modules . For example ,

```python
from math import sqrt   # importing square root function from math library
from math import log    # importing log function

from math import *      # import all function from math library
```

###  math
> This module is used to access to the mathematical functions defined under standard library .

```python
import math

print(math.sqrt(16))    # >>> 4.0

print(math.factorial(4))        #  >>> 24

# parameters (x,base)
print(math.log(8,2))      # >>> 3.0

# parameters (element)
print(math.log2(8))     # >>> 3.0     

# math.radians(x) converts x into radians and math.sin gives sin of math.randian(x) radians .
print(math.sin(math.radians(90)))      # >>> 1.0
```
[more functions ](https://docs.python.org/3/library/math.html)

### random

> This module implements pseudo-random number generators for various distributions.

```python
from random import *    

# we don't have to do random.uniform(x,y) anymore . prints random floating x such that 1.5<= x <5.5
print(uniform( 1.5, 5.5))       # >>> 5.139972864965343

#prints random floating x such that 0.0<= x <1.0
print(random())          # >>> 0.5898863000736234

# prints random integer x , where 0<=x <10
print(randrange(10))    # >>> 4

# prints random integer x , where a<=x <b
print(randrange(2,10))  # >>> 5

# Single random element from a sequence
print(choice(['win', 'lose', 'draw']))        # >>>'draw'

languages = ["scala","bf","c++","java"]
# Shuffle a list
shuffle(languages)
print(languages)        # >>> ['bf', 'c++', 'java', 'scala']

# Four samples without replacement
print(sample([10, 20, 30, 40, 50], k=4))        # >>> [30, 40, 20, 50]

```

[more functions](https://docs.python.org/3/library/random.html)

### sys

> This module provides access to some variables used or maintained by the interpreter and to functions that interact strongly with the interpreter. It is always available.

[more functions](https://docs.python.org/3/library/sys.html)

### os

> This module provides a portable way of using operating system dependent functionality.

```python
import os
#changes current working directory to test directory inside current directory
os.chdir("./test")     

os.getlogin()   # >>> 'Nishchith'                  

# path of current working directory
os.getcwd()     # >>> './GitHub/intro-to-programming'

```

[more functions](https://docs.python.org/3/library/os.html)
