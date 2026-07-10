General purpose language

Has large standard library - databases, automation, web scraping, text processing, image processing, machine learning, data analytics 

For DS - Pandas, numpy, scipy, matpotlib

For AI - Tensorflow, pytorch, keras, scikit-learn

For NLP - NLTK. Natural language tool kit


## Jupyter notebook

File --> rename
Run button
Menu bar --> run shtcut --> shift + enter
+ - to add new cell
edit --> delete shtcut --> dd, move cells

Tool bar --> + --> select notebook ,a lternativvely --> file --new launcher--> new notebook can be moved --> side by side

Jupyter --> supports presenting data
Markdown to add titles and text 
Slide functionality --> deliver code, visualization, text, outputs of code

Shutting down notebooks --> helps releasing memory
Stop icon on the side bar --> second icon from the top

Terminate all session at once or all session at once individually

After shutdown --> no kernak at the top right --> no longer active --> can be closed

Hands on Coding

Print('hello world)

To check the python version
Import sys
Print(sys.version)

sys - built-in module that contains many system-specific parameters and functions

Before using it, we must import it

# for commenting - means python ignore everything past #


Python interpreted language 

Compiled language --> examine entire program --> able to warn whole class of error prior to execution

Python interprets your scripts line by line as it executes it. Stops executing the entire program when it encounters an error


Data types: 

Integer, float, string

int - eg 1,2,3
float - eg 11.1, 22.2
Str - hello world

Integer - ( - to + values) finite range of integers

Float - real number - contains number between the integers as well -- superset of integers


Typecasting
Changing expression type

Integer to float : eg float(2) : 2

Float to Integer: int(1.1): 1. Must be careful as we'll lose some information 

If string contains integer can be converted to int.  for eg int('1) : 1

Convert string that has not integer value
Int('A') - error

Into to string, float to string
Str(1): "1" str(1.1): "1.1"

Boolean data type

Can take on two values
First value is True -- uppercase T
Book can also be false

Type (True): book

int/float(True): 1
Int/float(false): 0

Bool(1): true 
Bool(2): false

Python object oriented Language 
Most common object types..string,float,integers

type command - to check the type of expression For example type(12). Result int


import sys
Sys.float.info

Gives largest and smallest number that can be represented 


Expressions and variables

expression - type of operation python performs

For example :  basic arithmatic operation 10+20+30+40 - 100

Number 10 - operand
+ - operators

+,-,*,/

/ - returns float
// - returns integer - rounded down to nearest integer

For example 25/6 = 4.1
25//6 = 4

Follows arithmatic rules parenthesis first then division, multiplication, subtraction, addition 

(),/,*,-,+

Variables:


Variables to store values

a = 1 
x = 1+2
y = x/2


String operations

String - sequence of characters
Contain within quotes..both single and double
'vijay', "Vijay"

String can be space/digits/special characters

Bind string to a varia le
Name = 'Vijay'

Each element in the sequence can be accessed using an index represented by the array of numbers

Name[0] : V
Name[5]: Y

Negative indexing
Last value is indexed to -1 and first to -5

Name[-1]: Y
Name[-5]: V

Bind string to another variable
Name[0:2] = Vi
Name[4:5] = Jy

Stride values
Name[::2]: IA

Slicing 
Name[0:3:5]: VJY

Len('vijay') = 5 to obtain length of a string

Concatenate/combine string (+)

Statement = Name +"is the best"

Statement = "Vijay is the best"

Replicate values of a string

3*string, 3*Vijay: Vijay Vijay Vijay

Values of string cannot be changed
Name[0] = 'T' error

But new string by setting it to original variable

For example
Name = Name+'is the best'
Name = "Vijay is the best"

Strings are immutable

Escape sequences
\ - meant to proceed escape sequences 
Escape sequences are strings that are difficult to inpu

For example
\n - new line
Print("Vijay is the \n best"

Output: Vijay is the
                Best
\t - tab
Print("Vijay is the \t best")

O/P: Vijay is the        best

\\ - to place backslash in the string also r infront of the string

r - will tell python that string will be display as raw string
Print("Vijay is the \\ best")
Print(r"Vijay is the \\ best")

O/P: Vijay is the \ best

String methods

Sequence methods - applied methods that work on list and tuples

String methods - works on strings

Apply a method to a string A to give a different resulr string B

Eg: 

METHOD upper - Converts lower case characters to upper case characters 

A= "Vijay is the best"
B. A.upper()
B = "VIJAY IS THE BEST"

METHOD Replace - Replace Strings
A="Vijay is the best"
B=A.replace('Vijay','Ajith')
B= "Ajith is the best"

Method FIND - Find Substrings

Name.find('IJ'): 2
o/p is the first index of the sequence
If the substring is not in the string the o/p.is negative (-1)

METHOD SPLIT:

Splits the string at the specified separator, and returns a list.

Syntax

string.split(separator, maxsplit)

Parameters

separator (optional): This is the delimiter at which the string will be split. If not provided, the default separator is any whitespace.

maxsplit (optional): This specifies the maximum number of splits to perform. If not provided, there is no limit on the number of splits.

Eg:

name = "The BodyGuard"
split_string = (name.split())
split_string

O/P: ['The', 'Bodyguard']

split_string = (name.split('e', 2))
O/P: ['Th', 'BodyGuard']

Strip - removes leading/trailing whitespace 

Eg:

String = " Hello "
trimmed = string.strip()

O/P
Hello


RegEx - [ shortform of Regular Expression] - tool for matching and handling strings

Functions:
Search
Split
Findall
Sub

Built-in module in Python - re - need to import to work with regular expressions

import re

Search() - searches for specific patterns with a string. 

re.search()

Eg:
s1 = "The BodyGuard is the best album"
# Define the pattern to search for
pattern = r"Body"
# Use the search() function to search for the pattern in the string
result = re.search(pattern, s1)
# Check if a match was found
if result:
print("Match found!")
else:
print("Match not found.

O/P
Match found!

Special sequences ( refer pics at top)

Eg. For search

pattern = r"\d\d\d\d\d\d\d\d\d\d" # Matches any ten consecutive digits
text = "My Phone number is 1234567890"
match = re.search(pattern, text)
if match:
print("Phone number found:", match.group())
else:
print("No match")

O/P: Phone number found: 1234567890

match.group() method - to retrieve the part of the string where the regular expressions mattern matched

When functions re.search() or re.match is used, they return a match object if the pattern is found. match.group() is then used to get the matched text

Eg. For findall

pattern = r"\W" # Matches any non-word
character
text = "Hello, world!"
matches = re.findall (pattern, text)
print("Matches:", matches)

O/P:
Matches: [',' , ' ', '!']

\W - matched any character that is not a word character.

findall() function finds all occurances of a specified pattern within a string

Eg. Split()

RegEx split() function splits a string into an array of substrings based on a specified pattern

# Use the split function to split the string by the "\s"
split_array = re.split(r"\s", text)
# The split_array contains all the substrings, split by whitespace characters print(split_array)

O/P:
['Hello' , 'World']

\s - RegEx pattern that matches any whitespace character (spaces, tabs, newlines etc.).

Eg. For Sub()

Used to replace all occurances of a pattern in a string with specified replacement 

# Define the regular expression pattern to search for pattern = r"World"

# Define the replacement string

replacement = "Vijay"

# Use the sub function to replace the pattern with the replacement string

new_string = re.sub(pattern, replacement, text, flags=re. IGNORECASE)

# The new_string contains the original string with the pattern replaced by the r print(new_string

O/P
Hello Vijay!


Format strings

Way to inject variable into string in Python
Format strings and produce human readable o/p

String Interpolation(f-strings) - prefixed with f and use {} to enclose variables

Name = "Vijay"
Age = "24"
print(f"My name is {name} and I am {age} years old")

O/P
My name is Vijay and I am 24 years old

str.format()

{} Braces as placeholder for variables passd as arguments in the format() method

Name = "Vijay"
Age = "24"
print("My name is {} and I am {} years old".format(name,age))

O/P
My name is Vijay and I am 24 years old

%operator - % to replace variables 


Name = "Vijay"
Age = "24"
print("My name is %s and I am %d years old" %(name,age))

O/P
My name is Vijay and I am 24 years old

%s - placeholder for string
%d - placeholder for integer

%(name, age) - this is a tuple that contains name and age.

Additional

F-strings are also able to evaluate expressions inside the curly braces, which can be very handy. For example:

x = 10
y = 20
print(f" The sum of x and y is {x+y}.")

O/P
1The sum of x and y is 30.

Raw string (r' ')

Raw strings are a powerful tool for handling textual data, especially when dealing with escape characters.

By prefixing a string literal with the letter 'r', Python treats the string as raw, meaning it interprets backslashes as literal characters rather than escape sequences.

Eg:

Regular string:

regular_string = "C:\new_folder\file.txt"
print("Regular String:", regular_string)

O/P
Regular String: c:
ew_folderile.txt

In the regular string regular_string variable, the backslashes (\n) are interpreted as escape sequences.
Therefore, \n represents a newline character, which would lead to an incorrect file path representation.

Raw string 
raw_string = r"C:\new_folder\file.txt"
print("Raw String:", raw_string)

O/P
Raw String: c:\new_folder\file.txt

However, in the raw string raw_string, the backslashes are treated as literal characters. This means that \n is not interpreted as a newline character, but rather as two separate characters, \ and n. Consequently, the file path is represented exactly as it appearsGeneral purpose language

Has large standard library - databases, automation, web scraping, text processing, image processing, machine learning, data analytics 

For DS - Pandas, numpy, scipy, matpotlib

For AI - Tensorflow, pytorch, keras, scikit-learn

For NLP - NLTK. Natural language tool kit


Jupyter notebook

File --> rename
Run button
Menu bar --> run shtcut --> shift + enter
+ - to add new cell
edit --> delete shtcut --> dd, move cells

Tool bar --> + --> select notebook ,a lternativvely --> file --new launcher--> new notebook can be moved --> side by side

Jupyter --> supports presenting data
Markdown to add titles and text 
Slide functionality --> deliver code, visualization, text, outputs of code

Shutting down notebooks --> helps releasing memory
Stop icon on the side bar --> second icon from the top

Terminate all session at once or all session at once individually

After shutdown --> no kernak at the top right --> no longer active --> can be closed

Hands on Coding

Print('hello world)

To check the python version
Import sys
Print(sys.version)

sys - built-in module that contains many system-specific parameters and functions

Before using it, we must import it

# for commenting - means python ignore everything past #


Python interpreted language 

Compiled language --> examine entire program --> able to warn whole class of error prior to execution

Python interprets your scripts line by line as it executes it. Stops executing the entire program when it encounters an error


Data types: 

Integer, float, string

int - eg 1,2,3
float - eg 11.1, 22.2
Str - hello world

Integer - ( - to + values) finite range of integers

Float - real number - contains number between the integers as well -- superset of integers


Typecasting
Changing expression type

Integer to float : eg float(2) : 2

Float to Integer: int(1.1): 1. Must be careful as we'll lose some information 

If string contains integer can be converted to int.  for eg int('1) : 1

Convert string that has not integer value
Int('A') - error

Into to string, float to string
Str(1): "1" str(1.1): "1.1"

Boolean data type

Can take on two values
First value is True -- uppercase T
Book can also be false

Type (True): book

int/float(True): 1
Int/float(false): 0

Bool(1): true 
Bool(2): false

Python object oriented Language 
Most common object types..string,float,integers

type command - to check the type of expression For example type(12). Result int


import sys
Sys.float.info

Gives largest and smallest number that can be represented 


Expressions and variables

expression - type of operation python performs

For example :  basic arithmatic operation 10+20+30+40 - 100

Number 10 - operand
+ - operators

+,-,*,/

/ - returns float
// - returns integer - rounded down to nearest integer

For example 25/6 = 4.1
25//6 = 4

Follows arithmatic rules parenthesis first then division, multiplication, subtraction, addition 

(),/,*,-,+

Variables:


Variables to store values

a = 1 
x = 1+2
y = x/2


String operations

String - sequence of characters
Contain within quotes..both single and double
'vijay', "Vijay"

String can be space/digits/special characters

Bind string to a varia le
Name = 'Vijay'

Each element in the sequence can be accessed using an index represented by the array of numbers

Name[0] : V
Name[5]: Y

Negative indexing
Last value is indexed to -1 and first to -5

Name[-1]: Y
Name[-5]: V

Bind string to another variable
Name[0:2] = Vi
Name[4:5] = Jy

Stride values
Name[::2]: IA

Slicing 
Name[0:3:5]: VJY

Len('vijay') = 5 to obtain length of a string

Concatenate/combine string (+)

Statement = Name +"is the best"

Statement = "Vijay is the best"

Replicate values of a string

3*string, 3*Vijay: Vijay Vijay Vijay

Values of string cannot be changed
Name[0] = 'T' error

But new string by setting it to original variable

For example
Name = Name+'is the best'
Name = "Vijay is the best"

Strings are immutable

Escape sequences
\ - meant to proceed escape sequences 
Escape sequences are strings that are difficult to inpu

For example
\n - new line
Print("Vijay is the \n best"

Output: Vijay is the
                Best
\t - tab
Print("Vijay is the \t best")

O/P: Vijay is the        best

\\ - to place backslash in the string also r infront of the string

r - will tell python that string will be display as raw string
Print("Vijay is the \\ best")
Print(r"Vijay is the \\ best")

O/P: Vijay is the \ best

String methods

Sequence methods - applied methods that work on list and tuples

String methods - works on strings

Apply a method to a string A to give a different resulr string B

Eg: 

METHOD upper - Converts lower case characters to upper case characters 

A= "Vijay is the best"
B. A.upper()
B = "VIJAY IS THE BEST"

METHOD Replace - Replace Strings
A="Vijay is the best"
B=A.replace('Vijay','Ajith')
B= "Ajith is the best"

Method FIND - Find Substrings

Name.find('IJ'): 2
o/p is the first index of the sequence
If the substring is not in the string the o/p.is negative (-1)

METHOD SPLIT:

Splits the string at the specified separator, and returns a list.

Syntax

string.split(separator, maxsplit)

Parameters

separator (optional): This is the delimiter at which the string will be split. If not provided, the default separator is any whitespace.

maxsplit (optional): This specifies the maximum number of splits to perform. If not provided, there is no limit on the number of splits.

Eg:

name = "The BodyGuard"
split_string = (name.split())
split_string

O/P: ['The', 'Bodyguard']

split_string = (name.split('e', 2))
O/P: ['Th', 'BodyGuard']

Strip - removes leading/trailing whitespace 

Eg:

String = " Hello "
trimmed = string.strip()

O/P
Hello


RegEx - [ shortform of Regular Expression] - tool for matching and handling strings

Functions:
Search
Split
Findall
Sub

Built-in module in Python - re - need to import to work with regular expressions

import re

Search() - searches for specific patterns with a string. 

re.search()

Eg:
s1 = "The BodyGuard is the best album"
# Define the pattern to search for
pattern = r"Body"
# Use the search() function to search for the pattern in the string
result = re.search(pattern, s1)
# Check if a match was found
if result:
print("Match found!")
else:
print("Match not found.

O/P
Match found!

Special sequences ( refer pics at top)

Eg. For search

pattern = r"\d\d\d\d\d\d\d\d\d\d" # Matches any ten consecutive digits
text = "My Phone number is 1234567890"
match = re.search(pattern, text)
if match:
print("Phone number found:", match.group())
else:
print("No match")

O/P: Phone number found: 1234567890

match.group() method - to retrieve the part of the string where the regular expressions mattern matched

When functions re.search() or re.match is used, they return a match object if the pattern is found. match.group() is then used to get the matched text

Eg. For findall

pattern = r"\W" # Matches any non-word
character
text = "Hello, world!"
matches = re.findall (pattern, text)
print("Matches:", matches)

O/P:
Matches: [',' , ' ', '!']

\W - matched any character that is not a word character.

findall() function finds all occurances of a specified pattern within a string

Eg. Split()

RegEx split() function splits a string into an array of substrings based on a specified pattern

# Use the split function to split the string by the "\s"
split_array = re.split(r"\s", text)
# The split_array contains all the substrings, split by whitespace characters print(split_array)

O/P:
['Hello' , 'World']

\s - RegEx pattern that matches any whitespace character (spaces, tabs, newlines etc.).

Eg. For Sub()

Used to replace all occurances of a pattern in a string with specified replacement 

# Define the regular expression pattern to search for pattern = r"World"

# Define the replacement string

replacement = "Vijay"

# Use the sub function to replace the pattern with the replacement string

new_string = re.sub(pattern, replacement, text, flags=re. IGNORECASE)

# The new_string contains the original string with the pattern replaced by the r print(new_string

O/P
Hello Vijay!























Format strings

Way to inject variable into string in Python
Format strings and produce human readable o/p

String Interpolation(f-strings) - prefixed with f and use {} to enclose variables

Name = "Vijay"
Age = "24"
print(f"My name is {name} and I am {age} years old")

O/P
My name is Vijay and I am 24 years old

str.format()

{} Braces as placeholder for variables passd as arguments in the format() method

Name = "Vijay"
Age = "24"
print("My name is {} and I am {} years old".format(name,age))

O/P
My name is Vijay and I am 24 years old

%operator - % to replace variables 


Name = "Vijay"
Age = "24"
print("My name is %s and I am %d years old" %(name,age))

O/P
My name is Vijay and I am 24 years old

%s - placeholder for string
%d - placeholder for integer

%(name, age) - this is a tuple that contains name and age.

Additional

F-strings are also able to evaluate expressions inside the curly braces, which can be very handy. For example:

x = 10
y = 20
print(f" The sum of x and y is {x+y}.")

O/P
1The sum of x and y is 30.

Raw string (r' ')

Raw strings are a powerful tool for handling textual data, especially when dealing with escape characters.

By prefixing a string literal with the letter 'r', Python treats the string as raw, meaning it interprets backslashes as literal characters rather than escape sequences.

Eg:

Regular string:

regular_string = "C:\new_folder\file.txt"
print("Regular String:", regular_string)

O/P
Regular String: c:
ew_folderile.txt

In the regular string regular_string variable, the backslashes (\n) are interpreted as escape sequences.
Therefore, \n represents a newline character, which would lead to an incorrect file path representation.

Raw string 
raw_string = r"C:\new_folder\file.txt"
print("Raw String:", raw_string)

O/P
Raw String: c:\new_folder\file.txt

However, in the raw string raw_string, the backslashes are treated as literal characters. This means that \n is not interpreted as a newline character, but rather as two separate characters, \ and n. Consequently, the file path is represented exactly as it appears