<h1 align="center"><a href="#"> Strings </a></h1>

<h2>Introduction</h2>

>Python has a built-in string class named "str" with many handy features (there is an older module named "string" which you should not use). Python strings are "immutable" which means they cannot be changed after they are created. Since strings can't be changed, we construct *new* strings as we go to represent computed values. 

>So, for example the expression ('hello' + 'there') takes in the 2 strings 'hello' and 'there' and builds a new string 'hellothere'.

>Characters in a string can be accessed using the standard [ ] syntax. Python uses zero-based indexing, so if str is 'hello' str[1] is 'e'. If the index is out of bounds for the string, Python raises an error. The handy "slice" syntax (below) also works to extract any substring from a string. The len(string) function returns the length of a string. The [ ] syntax and the len() function actually work on any sequence type -- strings, lists, etc. Python tries to make its operations work consistently across different types. The '+' operator can concatenate two strings.

>Notice in the code below that variables are not pre-declared -- just assign to them and go.

 _**Example**_
```python
s = 'hi'
print s[1]          ## i
print len(s)        ## 2
print s + ' there'  ## hi there
```

>The str() function converts values to a string form so they can be combined with other strings.

 _**Example**_
```python
pi = 3.14
##text = 'The value of pi is ' + pi      ## NO, does not work
text = 'The value of pi is '  + str(pi)  ## yes
```

<h2>String Methods</h2>

>Here are some of the most common string methods. A method is like a function, but it runs "on" an object.

<h2>Functions</h2>

| <center>Function </center>                          | <center>What it does</center>  
| :-------------                                      | :-------------                   
| <a>s.lower(), s.upper()</a>                         | Returns the lowercase or uppercase version of the string
| <a>s.strip()</a>                                    |Returns a string with whitespace removed from the start and end       
| <a>s.isalpha(), s.isdigit(), s.isspace()</a>        |Tests if all the string chars are in the various character classes    
| <a>s.startswith('other'), s.endswith('other')</a>   |Tests if the string starts or ends with the given other string     
| <a>s.find('other')</a>                              |Searches for the given other string (not a regular expression) within s, and returns the first index where it begins or -1 if not found       
| <a>s.replace('old', 'new') </a>                     |Returns a string where all occurrences of 'old' have been replaced by 'new'     
| <a>s.split('delim') </a>                            |Returns a list of substrings separated by the given delimiter. The delimiter is not a regular expression, it's just text. 'aaa,bbb,ccc'.split(',') -> ['aaa', 'bbb', 'ccc']. As a convenient special case s.split() (with no arguments) splits on all whitespace chars.
| <a>s.join(list) </a>                                |Opposite of split(), joins the elements in the given list together using the string as the delimiter. e.g. '---'.join(['aaa', 'bbb', 'ccc']) -> aaa---bbb---ccc



<h2>String Slices</h2>  

>The "slice" syntax is a handy way to refer to sub-parts of sequences -- typically strings and lists. The slice s[start:end] is the elements beginning at start and extending up to but not including end. Suppose we have s = "Hello"

| <center>Function </center>       | <center>What it does</center>  
| :-------------                   | :-------------                   
| <a>s[1:4] </a>                   | is 'ell' -- chars starting at index 1 and extending up to but not including index 4
| <a>s[1:]</a>                     | is 'ello' -- omitting either index defaults to the start or end of the string      
| <a>s[:]</a>                      | is 'Hello' -- omitting both always gives us a copy of the whole thing (this is the pythonic way to copy a sequence like a string or list)    
| <a>s[1:100]</a>                  | an index that is too big is truncated down to the string length  



>The standard zero-based index numbers give easy access to chars near the start of the string. As an alternative, Python uses negative numbers to give easy access to the chars at the end of the string: s[-1] is the last char 'o', s[-2] is 'l' the next-to-last char, and so on. Negative index numbers count back from the end of the string:

| <center>Function </center>    | <center>What it does</center>  
| :-------------                | :-------------                   
| <a>s[-1] </a>                 | is 'o' -- last char (1st from the end)
| <a>s[-4]</a>                  | is 'e' -- 4th from the end      
| <a>s[:-3]</a>                 | is 'He' -- going up to but not including the last 3 chars    
| <a>s[-3:]</a>  
| is 'llo' -- starting with the 3rd char from the end and extending to the end of the string 


<h2>String %</h2>

>Python has a printf()-like facility to put together a string. The % operator takes a printf-type format string on the left (%d int, %s string, %f/%g floating point), and the matching values in a tuple on the right (a tuple is made of values separated by commas, typically grouped inside parentheses):

 _**Example**_
```python
## % operator
text = "%d little pigs come out or I'll %s and %s and %s" % (3, 'huff', 'puff', 'blow down')
```

>The above line is kind of long -- suppose you want to break it into separate lines. You cannot just split the line after the '%' as you might in other languages, since by default Python treats each line as a separate statement (on the plus side, this is why we don't need to type semi-colons on each line). To fix this, enclose the whole expression in an outer set of parenthesis -- then the expression is allowed to span multiple lines. This code-across-lines technique works with the various grouping constructs detailed below: ( ), [ ], { }.

 _**Example**_
```python
## add parens to make the long-line work:
text = ("%d little pigs come out or I'll %s and %s and %s" %
(3, 'huff', 'puff', 'blow down'))
```
