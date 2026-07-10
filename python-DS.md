Data structures:

Lists
Tuples
Dictionaries 
Sets

Tuples & Lists - called as compound data types - key types of data structures 

Tuples: 

- ordered sequence 
- written as comma separated elements within paranthesis

Eg . Ratings = (1,2,3,4,5,6,7,8)

All type of data type(string,int,float) can be contained in tuple but the type of the variable is a tuple

Tuple1 = ('Vijay', 1, 1.1)
type(tuple1) = tuple

Each element of a tuple can be accessed via an index

0 - 'Vijay'
1 - 1
2 - 1.1

tuple1[0] = 'Vijay'
tuple1[1] = 1
tuple1[2] = 1.1

Negative index

-3 - 'Vijay'
-2  - 1
-1 - 1.1

tuple1[-3] = 'Vijay'
tuple1[-1] = 1
tuple1[-2] = 1.1

Concatenate tuples:

tuple2 = tuple1 + ('Ajith', 1.2)
O/P
('Vijay', 1, 1.1, Ajith, 1.2)

Slicing tuple:
tuple2[0:3]: ('Vijay', 1, 1.1)


Length of a tuple:
len('Vijay', 1, 1.1, Ajith, 1.2): 5

Tuples are immutable - can't be changed
Values in tuples cannot be changed

Ratings1 = (1,2,3,4,5)
Ratings1 = Ratings

Each variable does not contain a tuple but refrences the same immutable tuple object

Rating[0] = 4 is not impossible since tuple is immutable

To manipulate a tuple - we must use create new tuple

Eg.
Ratings = (1,2,3,4,5)
Ratungssorted = sorted(Ratings)

Input is the original tuple but the output is a new tuple.

Nestings - tuple containing other tuples as well as other data types

Eg.
NT = (1,2,("pop", "rock"), (3,4), ("disco", (1,2)))

Indexing:
0 - 1
1 - 2
2 - ("pop", "rock")
3 - (3,4)
4 - ("disco", (1,2))

tuple[2]: ("pop", "rock")
0 - pop
1 - rock

Indexing directly to tuple variable
NT[2][1]: "rock"

Access different characters in a string
NT[2][1][0]: r

Tuple1 = ('Vijay', 1, 1.1)
Find the index of 'j' in Vijay
"Vijay".find('j')

Lists: 

- also an ordered sequence 
- represented with square brackets 
- lists are like tuples but lists are mutable

L = [' Vijay', 1, 1.1]

List can contain strings, float, int, nest list, nest tuples and other data structures.

Indexing          Negative Indexing
L[0]: Vijay       L[-3]: Vijay
L[1]: 1               L[-2]: 1
L[2]: 1.1            L[-1]: 1.1

Slicing

L2= [' Vijay', 1, 1.1, 'Ajith', 2]
L2[3:5]: [Ajith', 2]

Concatenate 
L1 = L + ['Ajith', 2]
L1 = [' Vijay', 1, 1.1, 'Ajith', 2]


L = [' Vijay', 1, 1.1]

L.extend(['Ajith', 2]) - To concatenate/add values to the existing list since lists are mutable
O/P:
L = [' Vijay', 1, 1.1, 'Ajith', 2]

L.append(['Ajith', 2])- one element is added to the list
O/P:
L = [' Vijay', 1, 1.1, ['Ajith', 2]]

Elements in Lists can be changed
L = [' Vijay', 1, 1.1]
L[0] = 'Ajith'
L = [' Ajith', 1, 1.1]

Delete an element of the list with del command
del(L[0])
L = [1,1.1]

Split() - Convert a string to a list 
Eg.
"Hello" " World".split()
["Hard", "Rock"]

"A,B,C,D.split(",")
["A","B","C","D"]

Aliasing - multiple names referencing to a same object 

A = [' Vijay', 1, 1.1]
B = A

Both A&B reference same list

B[0] = 'Vijay'
If value of A is changed,  value of B will change as a consequence
A[0] = 'Ajith'
B[0] = 'Ajith'

Clone list A

A = [' Vijay', 1, 1.1]
B = A[:] - copy of A

Now if we change value of A, B will not change

Help command - to get more information on list, tuples and many other objects in Python 
Eg.
help(A), help[A]


Dictionaries 
- type of collection in python
- list has indexes and elements. Eg 0 - 'Vijay'
- dictionary has keys and values key 0: value 1
- keys are like address but it doesn't have to be integers - characters 
- values are similar to elements in a list

Eg. Aadhar number. Aadhar number is a unique number which will be the key and the details of the people will be the values associated with it


To create a dictionary:
- curly brackets
- keys are the first elements 
- keys have to be immutable and unique
- Values can be immutable, mutable and duplicates 
- each key and value pair separated by comma

{"key1":1, "key2":"2","key3":[3,3,3],"key4":[4,4,4],('key5'):5}

Eg.

DICT nu nvc = {"Thriller": 1982, "Back in black: 1980"}

Key is used to look up the value

DICT[KEY]: VALUE

DICT["Back in black"]: 1980

DICT['Graduation'] = 2007
{"Thriller": "1982", "Back in black: "1980", "Graduation": "2007"}

del(DICT["Thriller"]) to delete an entry
O/P:
{"Back in black: "1980", "Graduation": "2007"}

"Back in Black" in DICT - To verify if value is in the dictionary - if present - true else - False
O/P 
True

DICT.keys() - method to see all the keys in a dictionary 
O/P - object with all the keys
["Back in black, "Graduation"]

DICT.values() - method/function to see all the values in a dictionary 
O/P - object with all the keys
["1980", "2007"]

Sets:

- type of collection
- input different Python types
- they are unordered, do not record element position 
- only have unique elements. Only one of a particular element in a set
- curly brackets 

Set1 = {"Vijay", "Ajith", "Surya", "Vijay"}

When actual set is create duplicate items are removed

Set1 = {"Vijay", "Ajith", "Surya"}

Convert list to set using set() function - called typecasting

List = ["Vijay", "Ajith", "Surya", "Vijay"]
Name = set(List)
O/P
Name: {"Vijay", "Ajith", "Surya"}

Set Operations:

Add an item
A= {"Vijay", "Ajith", "Surya"}
A.add("Kamal")
O/P
{"Vijay", "Ajith", "Surya", "Kamal"}

Remove an item
A.remove("Kamal")
O/P
{"Vijay", "Ajith", "Surya"}

In command
Vijay In A - True
Kamal In A - False

Mathematical Set Operations

Sets can be easily viewed with Venn diagram

A = {"Vijay", "Ajith", "Surya"}
B = {"Vijay", "Ajith", "Kamal"}

Intersection 
C = A & B
& - common in two sets
O/P
C = {"Vijay", "Ajith"}


Union - all elements in A and B 
A.union(B)
O/P
A = {"Vijay", "Ajith", "Surya", "Kamal"}

Difference: element in A without common
A.difference(B)
O/P
A = {"Surya"}

B.difference(A) - element in B without common
{"Kamal"}

Subset
A = {"Vijay", "Ajith", "Surya"}
C = {"Vijay", "Ajith"}

C.issubset(A) - True