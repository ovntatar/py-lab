# py-lab
#

https://www.w3schools.com/python/default.asp
https://www.designveloper.com/blog/python-best-practices/
https://therenegadecoder.com/code/python-code-snippets-for-everyday-problems/


### Built-in Data Types
In programming, data type is an important concept.

Variables can store data of different types, and different types can do different things.

Python has the following data types built-in by default, in these categories:

Text Type:	str
Numeric Types:	int, float, complex
Sequence Types:	list, tuple, range
Mapping Type:	dict
Set Types:	set, frozenset
Boolean Type:	bool
Binary Types:	bytes, bytearray, memoryview



x = 5
print(type(x))



x = "Hello World"	str
x = 20	int
x = 20.5	float
x = 1j	complex
x = ["apple", "banana", "cherry"]	list
x = ("apple", "banana", "cherry")	tuple
x = range(6)	range
x = {"name" : "John", "age" : 36}	dict
x = {"apple", "banana", "cherry"}	set
x = frozenset({"apple", "banana", "cherry"})	frozenset
x = True	bool
x = b"Hello"	bytes
x = bytearray(5)	bytearray
x = memoryview(bytes(5))	memoryview



### Python Numbers
There are three numeric types in Python:

int
float
complex
Variables of numeric types are created when you assign a value to them:

Example
x = 1    # int
y = 2.8  # float
z = 1j   # complex


### Python Casting
Specify a Variable Type
There may be times when you want to specify a type on to a variable. This can be done with casting. Python is an object-orientated language, and as such it uses classes to define data types, including its primitive types.

Casting in python is therefore done using constructor functions:

int() - constructs an integer number from an integer literal, a float literal (by removing all decimals), or a string literal (providing the string represents a whole number)
float() - constructs a float number from an integer literal, a float literal or a string literal (providing the string represents a float or an integer)
str() - constructs a string from a wide variety of data types, including strings, integer literals and float literals
Example
Integers:

x = int(1)   # x will be 1
y = int(2.8) # y will be 2
z = int("3") # z will be 3


### Many Values to Multiple Variables
Python allows you to assign values to multiple variables in one line:

Example
x, y, z = "Orange", "Banana", "Cherry"
print(x)
print(y)
print(z)
Note: Make sure the number of variables matches the number of values, or else you will get an error.

One Value to Multiple Variables
And you can assign the same value to multiple variables in one line:

Example
x = y = z = "Orange"
print(x)
print(y)
print(z)


Unpack a Collection
If you have a collection of values in a list, tuple etc. Python allows you extract the values into variables. This is called unpacking.

Example
Unpack a list:

fruits = ["apple", "banana", "cherry"]
x, y, z = fruits
print(x)
print(y)
print(z)



### Output Variables
The Python print statement is often used to output variables.

To combine both text and a variable, Python uses the + character:

Example
x = "awesome"
print("Python is " + x)
You can also use the + character to add a variable to another variable:

Example
x = "Python is "
y = "awesome"
z =  x + y
print(z)
For numbers, the + character works as a mathematical operator:

Example
x = 5
y = 10
print(x + y)


### Python - Global Variables
Global Variables
Variables that are created outside of a function (as in all of the examples above) are known as global variables.

Global variables can be used by everyone, both inside of functions and outside.

Example
Create a variable outside of a function, and use it inside the function

x = "awesome"

def myfunc():
  print("Python is " + x)

myfunc()
If you create a variable with the same name inside a function, this variable will be local, and can only be used inside the function. The global variable with the same name will remain as it was, global and with the original value.

Example
Create a variable inside a function, with the same name as the global variable

x = "awesome"

def myfunc():
  x = "fantastic"
  print("Python is " + x)

myfunc()

print("Python is " + x)
The global Keyword
Normally, when you create a variable inside a function, that variable is local, and can only be used inside that function.

To create a global variable inside a function, you can use the global keyword.

Example
If you use the global keyword, the variable belongs to the global scope:

def myfunc():
  global x
  x = "fantastic"

myfunc()

print("Python is " + x)
Also, use the global keyword if you want to change a global variable inside a function.

Example
To change the value of a global variable inside a function, refer to the variable by using the global keyword:

x = "awesome"

def myfunc():
  global x
  x = "fantastic"

myfunc()

print("Python is " + x)


### Python - Slicing Strings
Slicing
You can return a range of characters by using the slice syntax.

Specify the start index and the end index, separated by a colon, to return a part of the string.

Example
Get the characters from position 2 to position 5 (not included):

b = "Hello, World!"
print(b[2:5])
Note: The first character has index 0.

Slice From the Start
By leaving out the start index, the range will start at the first character:

Example
Get the characters from the start to position 5 (not included):

b = "Hello, World!"
print(b[:5])
Slice To the End
By leaving out the end index, the range will go to the end:

Example
Get the characters from position 2, and all the way to the end:

b = "Hello, World!"
print(b[2:])
Negative Indexing
Use negative indexes to start the slice from the end of the string:
Example
Get the characters:

From: "o" in "World!" (position -5)

To, but not included: "d" in "World!" (position -2):

b = "Hello, World!"
print(b[-5:-2])


### Python - Modify Strings
Python has a set of built-in methods that you can use on strings.

Upper Case
Example
The upper() method returns the string in upper case:

a = "Hello, World!"
print(a.upper())
Lower Case
Example
The lower() method returns the string in lower case:

a = "Hello, World!"
print(a.lower())
Remove Whitespace
Whitespace is the space before and/or after the actual text, and very often you want to remove this space.

Example
The strip() method removes any whitespace from the beginning or the end:

a = " Hello, World! "
print(a.strip()) # returns "Hello, World!"
Replace String
Example
The replace() method replaces a string with another string:

a = "Hello, World!"
print(a.replace("H", "J"))
Split String
The split() method returns a list where the text between the specified separator becomes the list items.

Example
The split() method splits the string into substrings if it finds instances of the separator:

a = "Hello, World!"
print(a.split(",")) # returns ['Hello', ' World!']



### Python - String Concatenation
String Concatenation
To concatenate, or combine, two strings you can use the + operator.

Example
Merge variable a with variable b into variable c:

a = "Hello"
b = "World"
c = a + b
print(c)
Example
To add a space between them, add a " ":

a = "Hello"
b = "World"
c = a + " " + b
print(c)


### Python - Format - Strings
String Format
As we learned in the Python Variables chapter, we cannot combine strings and numbers like this:

Example
age = 36
txt = "My name is John, I am " + age
print(txt)
But we can combine strings and numbers by using the format() method!

The format() method takes the passed arguments, formats them, and places them in the string where the placeholders {} are:

Example
Use the format() method to insert numbers into strings:

age = 36
txt = "My name is John, and I am {}"
print(txt.format(age))
The format() method takes unlimited number of arguments, and are placed into the respective placeholders:

Example
quantity = 3
itemno = 567
price = 49.95
myorder = "I want {} pieces of item {} for {} dollars."
print(myorder.format(quantity, itemno, price))
You can use index numbers {0} to be sure the arguments are placed in the correct placeholders:

Example
quantity = 3
itemno = 567
price = 49.95
myorder = "I want to pay {2} dollars for {0} pieces of item {1}."
print(myorder.format(quantity, itemno, price))


### Escape Characters
Other escape characters used in Python:

Code	Result	Try it
\'	Single Quote	
\\	Backslash	
\n	New Line	
\r	Carriage Return	
\t	Tab	
\b	Backspace	
\f	Form Feed	
\ooo	Octal value	
\xhh	Hex value



The format() method allows you to format selected parts of a string.

Sometimes there are parts of a text that you do not control, maybe they come from a database, or user input?

To control such values, add placeholders (curly brackets {}) in the text, and run the values through the format() method:

Example
Add a placeholder where you want to display the price:

price = 49
txt = "The price is {} dollars"
print(txt.format(price))
You can add parameters inside the curly brackets to specify how to convert the value:

Example
Format the price to be displayed as a number with two decimals:

txt = "The price is {:.2f} dollars"
Check out all formatting types in our String format() Reference.

Multiple Values
If you want to use more values, just add more values to the format() method:

print(txt.format(price, itemno, count))
And add more placeholders:

Example
quantity = 3
itemno = 567
price = 49
myorder = "I want {} pieces of item number {} for {:.2f} dollars."
print(myorder.format(quantity, itemno, price))
Index Numbers
You can use index numbers (a number inside the curly brackets {0}) to be sure the values are placed in the correct placeholders:

Example
quantity = 3
itemno = 567
price = 49
myorder = "I want {0} pieces of item number {1} for {2:.2f} dollars."
print(myorder.format(quantity, itemno, price))
Also, if you want to refer to the same value more than once, use the index number:

Example
age = 36
name = "John"
txt = "His name is {1}. {1} is {0} years old."
print(txt.format(age, name))
Named Indexes
You can also use named indexes by entering a name inside the curly brackets {carname}, but then you must use names when you pass the parameter values txt.format(carname = "Ford"):

Example
myorder = "I have a {carname}, it is a {model}."
print(myorder.format(carname = "Ford", model = "Mustang"))


### Python Booleans
Booleans represent one of two values: True or False.

Boolean Values
In programming you often need to know if an expression is True or False.

You can evaluate any expression in Python, and get one of two answers, True or False.

When you compare two values, the expression is evaluated and Python returns the Boolean answer:

Example
print(10 > 9)
print(10 == 9)
print(10 < 9)
When you run a condition in an if statement, Python returns True or False:

Example
Print a message based on whether the condition is True or False:

a = 200
b = 33

if b > a:
  print("b is greater than a")
else:
  print("b is not greater than a")
Evaluate Values and Variables
The bool() function allows you to evaluate any value, and give you True or False in return,

Example
Evaluate a string and a number:

print(bool("Hello"))
print(bool(15))
Example
Evaluate two variables:

x = "Hello"
y = 15

print(bool(x))
print(bool(y))


Python Operators
Python Operators
Operators are used to perform operations on variables and values.

In the example below, we use the + operator to add together two values:

Example
print(10 + 5)
Python divides the operators in the following groups:

Arithmetic operators
Assignment operators
Comparison operators
Logical operators
Identity operators
Membership operators
Bitwise operators
Python Arithmetic Operators
Arithmetic operators are used with numeric values to perform common mathematical operations:

Operator	Name	Example	Try it
+	Addition	x + y	
-	Subtraction	x - y	
*	Multiplication	x * y	
/	Division	x / y	
%	Modulus	x % y	
**	Exponentiation	x ** y	
//	Floor division	x // y	
Python Assignment Operators
Assignment operators are used to assign values to variables:

Operator	Example	Same As	Try it
=	x = 5	x = 5	
+=	x += 3	x = x + 3	
-=	x -= 3	x = x - 3	
*=	x *= 3	x = x * 3	
/=	x /= 3	x = x / 3	
%=	x %= 3	x = x % 3	
//=	x //= 3	x = x // 3	
**=	x **= 3	x = x ** 3	
&=	x &= 3	x = x & 3	
|=	x |= 3	x = x | 3	
^=	x ^= 3	x = x ^ 3	
>>=	x >>= 3	x = x >> 3	
<<=	x <<= 3	x = x << 3



### Python Comparison Operators
Comparison operators are used to compare two values:

Operator	Name	Example	Try it
==	Equal	x == y
!=	Not equal	x != y
>	Greater than	x > y
<	Less than	x < y
>=	Greater than or equal to	x >= y
<=	Less than or equal to	x <= y
Python Logical Operators
Logical operators are used to combine conditional statements:

Operator	Description	Example	Try it
and 	Returns True if both statements are true	x < 5 and  x < 10
or	Returns True if one of the statements is true	x < 5 or x < 4
not	Reverse the result, returns False if the result is true	not(x < 5 and x < 10)
Python Identity Operators
Identity operators are used to compare the objects, not if they are equal, but if they are actually the same object, with the same memory location:

Operator	Description	Example	Try it
is 	Returns True if both variables are the same object	x is y
is not	Returns True if both variables are not the same object	x is not y
Python Membership Operators
Membership operators are used to test if a sequence is presented in an object:

Operator	Description	Example	Try it
in 	Returns True if a sequence with the specified value is present in the object	x in y
not in	Returns True if a sequence with the specified value is not present in the object	x not in y
Python Bitwise Operators
Bitwise operators are used to compare (binary) numbers:

Operator	Name	Description
& 	AND	Sets each bit to 1 if both bits are 1
|	OR	Sets each bit to 1 if one of two bits is 1
 ^	XOR	Sets each bit to 1 if only one of two bits is 1
~ 	NOT	Inverts all the bits
<<	Zero fill left shift	Shift left by pushing zeros in from the right and let the leftmost bits fall off
>>	Signed right shift	Shift right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off


### Python Lists
mylist = ["apple", "banana", "cherry"]
List
Lists are used to store multiple items in a single variable.

Lists are one of 4 built-in data types in Python used to store collections of data, the other 3 are Tuple, Set, and Dictionary, all with different qualities and usage.

Lists are created using square brackets:

Example
Create a List:

thislist = ["apple", "banana", "cherry"]
print(thislist)
List Items
List items are ordered, changeable, and allow duplicate values.

List items are indexed, the first item has index [0], the second item has index [1] etc.

Ordered
When we say that lists are ordered, it means that the items have a defined order, and that order will not change.

If you add new items to a list, the new items will be placed at the end of the list.

Note: There are some list methods that will change the order, but in general: the order of the items will not change.

Changeable
The list is changeable, meaning that we can change, add, and remove items in a list after it has been created.

Allow Duplicates
Since lists are indexed, lists can have items with the same value:

Example
Lists allow duplicate values:

thislist = ["apple", "banana", "cherry", "apple", "cherry"]
print(thislist)


### Python - Access List Items
Access Items
List items are indexed and you can access them by referring to the index number:

Example
Print the second item of the list:

thislist = ["apple", "banana", "cherry"]
print(thislist[1])
Note: The first item has index 0.

Negative Indexing
Negative indexing means start from the end

-1 refers to the last item, -2 refers to the second last item etc.

Example
Print the last item of the list:

thislist = ["apple", "banana", "cherry"]
print(thislist[-1])
Range of Indexes
You can specify a range of indexes by specifying where to start and where to end the range.

When specifying a range, the return value will be a new list with the specified items.

Example
Return the third, fourth, and fifth item:

thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(thislist[2:5])
Note: The search will start at index 2 (included) and end at index 5 (not included).

Remember that the first item has index 0.

By leaving out the start value, the range will start at the first item:

Example
This example returns the items from the beginning to, but NOT including, "kiwi":

thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(thislist[:4])
By leaving out the end value, the range will go on to the end of the list:

Example
This example returns the items from "cherry" to the end:

thislist = ["apple", "banana", "cherry", "orange", "kiwi", "melon", "mango"]
print(thislist[2:])



### Python - Change List Items
Change Item Value
To change the value of a specific item, refer to the index number:

Example
Change the second item:

thislist = ["apple", "banana", "cherry"]
thislist[1] = "blackcurrant"
print(thislist)
Change a Range of Item Values
To change the value of items within a specific range, define a list with the new values, and refer to the range of index numbers where you want to insert the new values:

Example
Change the values "banana" and "cherry" with the values "blackcurrant" and "watermelon":

thislist = ["apple", "banana", "cherry", "orange", "kiwi", "mango"]
thislist[1:3] = ["blackcurrant", "watermelon"]
print(thislist)
If you insert more items than you replace, the new items will be inserted where you specified, and the remaining items will move accordingly:

Example
Change the second value by replacing it with two new values:

thislist = ["apple", "banana", "cherry"]
thislist[1:2] = ["blackcurrant", "watermelon"]
print(thislist)
Note: The length of the list will change when the number of items inserted does not match the number of items replaced.

If you insert less items than you replace, the new items will be inserted where you specified, and the remaining items will move accordingly:

Example
Change the second and third value by replacing it with one value:

thislist = ["apple", "banana", "cherry"]
thislist[1:3] = ["watermelon"]
print(thislist)
Insert Items
To insert a new list item, without replacing any of the existing values, we can use the insert() method.

The insert() method inserts an item at the specified index:

Example
Insert "watermelon" as the third item:

thislist = ["apple", "banana", "cherry"]
thislist.insert(2, "watermelon")
print(thislist)


### Python - Add List Items
Append Items
To add an item to the end of the list, use the append() method:

Example
Using the append() method to append an item:

thislist = ["apple", "banana", "cherry"]
thislist.append("orange")
print(thislist)
Insert Items
To insert a list item at a specified index, use the insert() method.

The insert() method inserts an item at the specified index:

Example
Insert an item as the second position:

thislist = ["apple", "banana", "cherry"]
thislist.insert(1, "orange")
print(thislist)
Note: As a result of the examples above, the lists will now contain 4 items.

Extend List
To append elements from another list to the current list, use the extend() method.

Example
Add the elements of tropical to thislist:

thislist = ["apple", "banana", "cherry"]
tropical = ["mango", "pineapple", "papaya"]
thislist.extend(tropical)
print(thislist)
The elements will be added to the end of the list.

Add Any Iterable
The extend() method does not have to append lists, you can add any iterable object (tuples, sets, dictionaries etc.).

Example
Add elements of a tuple to a list:

thislist = ["apple", "banana", "cherry"]
thistuple = ("kiwi", "orange")
thislist.extend(thistuple)
print(thislist)



### Python - Remove List Items
Remove Specified Item
The remove() method removes the specified item.

Example
Remove "banana":

thislist = ["apple", "banana", "cherry"]
thislist.remove("banana")
print(thislist)
Remove Specified Index
The pop() method removes the specified index.

Example
Remove the second item:

thislist = ["apple", "banana", "cherry"]
thislist.pop(1)
print(thislist)
If you do not specify the index, the pop() method removes the last item.

Example
Remove the last item:

thislist = ["apple", "banana", "cherry"]
thislist.pop()
print(thislist)
The del keyword also removes the specified index:

Example
Remove the first item:

thislist = ["apple", "banana", "cherry"]
del thislist[0]
print(thislist)
The del keyword can also delete the list completely.

Example
Delete the entire list:

thislist = ["apple", "banana", "cherry"]
del thislist
Clear the List
The clear() method empties the list.

The list still remains, but it has no content.

Example
Clear the list content:

thislist = ["apple", "banana", "cherry"]
thislist.clear()
print(thislist)




### Python - Loop Lists
Loop Through a List
You can loop through the list items by using a for loop:

Example
Print all items in the list, one by one:

thislist = ["apple", "banana", "cherry"]
for x in thislist:
  print(x)
Learn more about for loops in our Python For Loops Chapter.

Loop Through the Index Numbers
You can also loop through the list items by referring to their index number.

Use the range() and len() functions to create a suitable iterable.

Example
Print all items by referring to their index number:

thislist = ["apple", "banana", "cherry"]
for i in range(len(thislist)):
  print(thislist[i])
The iterable created in the example above is [0, 1, 2].

ADVERTISEMENT


Using a While Loop
You can loop through the list items by using a while loop.

Use the len() function to determine the length of the list, then start at 0 and loop your way through the list items by refering to their indexes.

Remember to increase the index by 1 after each iteration.

Example
Print all items, using a while loop to go through all the index numbers

thislist = ["apple", "banana", "cherry"]
i = 0
while i < len(thislist):
  print(thislist[i])
  i = i + 1
Learn more about while loops in our Python While Loops Chapter.

Looping Using List Comprehension
List Comprehension offers the shortest syntax for looping through lists:

Example
A short hand for loop that will print all items in a list:

thislist = ["apple", "banana", "cherry"]
[print(x) for x in thislist]



### Python - List Comprehension
List Comprehension
List comprehension offers a shorter syntax when you want to create a new list based on the values of an existing list.

Example:

Based on a list of fruits, you want a new list, containing only the fruits with the letter "a" in the name.

Without list comprehension you will have to write a for statement with a conditional test inside:

Example
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = []

for x in fruits:
  if "a" in x:
    newlist.append(x)

print(newlist)
With list comprehension you can do all that with only one line of code:

Example
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]

newlist = [x for x in fruits if "a" in x]

print(newlist)
ADVERTISEMENT


The Syntax
newlist = [expression for item in iterable if condition == True]
The return value is a new list, leaving the old list unchanged.

Condition
The condition is like a filter that only accepts the items that valuate to True.

Example
Only accept items that are not "apple":

newlist = [x for x in fruits if x != "apple"]
The condition if x != "apple"  will return True for all elements other than "apple", making the new list contain all fruits except "apple".

The condition is optional and can be omitted:

Example
With no if statement:

newlist = [x for x in fruits]
Iterable
The iterable can be any iterable object, like a list, tuple, set etc.

Example
You can use the range() function to create an iterable:

newlist = [x for x in range(10)]
Same example, but with a condition:

Example
Accept only numbers lower than 5:

newlist = [x for x in range(10) if x < 5]
Expression
The expression is the current item in the iteration, but it is also the outcome, which you can manipulate before it ends up like a list item in the new list:

Example
Set the values in the new list to upper case:

newlist = [x.upper() for x in fruits]
You can set the outcome to whatever you like:

Example
Set all values in the new list to 'hello':

newlist = ['hello' for x in fruits]
The expression can also contain conditions, not like a filter, but as a way to manipulate the outcome:

Example
Return "orange" instead of "banana":

newlist = [x if x != "banana" else "orange" for x in fruits]



### Python - Sort Lists
Sort List Alphanumerically
List objects have a sort() method that will sort the list alphanumerically, ascending, by default:

Example
Sort the list alphabetically:

thislist = ["orange", "mango", "kiwi", "pineapple", "banana"]
thislist.sort()
print(thislist)
Example
Sort the list numerically:

thislist = [100, 50, 65, 82, 23]
thislist.sort()
print(thislist)
Sort Descending
To sort descending, use the keyword argument reverse = True:

Example
Sort the list descending:

thislist = ["orange", "mango", "kiwi", "pineapple", "banana"]
thislist.sort(reverse = True)
print(thislist)
Example
Sort the list descending:

thislist = [100, 50, 65, 82, 23]
thislist.sort(reverse = True)
print(thislist)



### Python - Copy Lists
Copy a List
You cannot copy a list simply by typing list2 = list1, because: list2 will only be a reference to list1, and changes made in list1 will automatically also be made in list2.

There are ways to make a copy, one way is to use the built-in List method copy().

Example
Make a copy of a list with the copy() method:

thislist = ["apple", "banana", "cherry"]
mylist = thislist.copy()
print(mylist)
Another way to make a copy is to use the built-in method list().

Example
Make a copy of a list with the list() method:

thislist = ["apple", "banana", "cherry"]
mylist = list(thislist)
print(mylist)


### Python - Join Lists
Join Two Lists
There are several ways to join, or concatenate, two or more lists in Python.

One of the easiest ways are by using the + operator.

Example
Join two list:

list1 = ["a", "b", "c"]
list2 = [1, 2, 3]

list3 = list1 + list2
print(list3)
Another way to join two lists are by appending all the items from list2 into list1, one by one:

Example
Append list2 into list1:

list1 = ["a", "b" , "c"]
list2 = [1, 2, 3]

for x in list2:
  list1.append(x)

print(list1)
Or you can use the extend() method, which purpose is to add elements from one list to another list:

Example
Use the extend() method to add list2 at the end of list1:

list1 = ["a", "b" , "c"]
list2 = [1, 2, 3]

list1.extend(list2)
print(list1)



#### Python Tuples
mytuple = ("apple", "banana", "cherry")
Tuple
Tuples are used to store multiple items in a single variable.

Tuple is one of 4 built-in data types in Python used to store collections of data, the other 3 are List, Set, and Dictionary, all with different qualities and usage.

A tuple is a collection which is ordered and unchangeable.

Tuples are written with round brackets.

Example
Create a Tuple:

thistuple = ("apple", "banana", "cherry")
print(thistuple)
Tuple Items
Tuple items are ordered, unchangeable, and allow duplicate values.

Tuple items are indexed, the first item has index [0], the second item has index [1] etc.

Ordered
When we say that tuples are ordered, it means that the items have a defined order, and that order will not change.

Unchangeable
Tuples are unchangeable, meaning that we cannot change, add or remove items after the tuple has been created.

Allow Duplicates
Since tuple are indexed, tuples can have items with the same value:

Example
Tuples allow duplicate values:

thistuple = ("apple", "banana", "cherry", "apple", "cherry")
print(thistuple)



### Python - Access Tuple Items
Access Tuple Items
You can access tuple items by referring to the index number, inside square brackets:

Example
Print the second item in the tuple:

thistuple = ("apple", "banana", "cherry")
print(thistuple[1])
Note: The first item has index 0.

Negative Indexing
Negative indexing means start from the end.

-1 refers to the last item, -2 refers to the second last item etc.

Example
Print the last item of the tuple:

thistuple = ("apple", "banana", "cherry")
print(thistuple[-1])
Range of Indexes
You can specify a range of indexes by specifying where to start and where to end the range.

When specifying a range, the return value will be a new tuple with the specified items.

Example
Return the third, fourth, and fifth item:

thistuple = ("apple", "banana", "cherry", "orange", "kiwi", "melon", "mango")
print(thistuple[2:5])

### Python - Update Tuples
Tuples are unchangeable, meaing that you cannot change, add, or remove items once the tuple is created.

But there are some workarounds.

Change Tuple Values
Once a tuple is created, you cannot change its values. Tuples are unchangeable, or immutable as it also is called.

But there is a workaround. You can convert the tuple into a list, change the list, and convert the list back into a tuple.

Example
Convert the tuple into a list to be able to change it:

x = ("apple", "banana", "cherry")
y = list(x)
y[1] = "kiwi"
x = tuple(y)

print(x)
Add Items
Once a tuple is created, you cannot add items to it.

Example
You cannot add items to a tuple:

thistuple = ("apple", "banana", "cherry")
thistuple.append("orange") # This will raise an error
print(thistuple)
Just like the workaround for changing a tuple, you can convert it into a list, add your item(s), and convert it back into a tuple.

Example
Convert the tuple into a list, add "orange", and convert it back into a tuple:

thistuple = ("apple", "banana", "cherry")
y = list(thistuple)
y.append("orange")
thistuple = tuple(y)


### Python - Unpack Tuples
Unpacking a Tuple
When we create a tuple, we normally assign values to it. This is called "packing" a tuple:

Example
Packing a tuple:

fruits = ("apple", "banana", "cherry")
But, in Python, we are also allowed to extract the values back into variables. This is called "unpacking":

Example
Unpacking a tuple:

fruits = ("apple", "banana", "cherry")

(green, yellow, red) = fruits

print(green)
print(yellow)
print(red)
Note: The number of variables must match the number of values in the tuple, if not, you must use an asterix to collect the remaining values as a list.

ADVERTISEMENT


Using Asterisk*
If the number of variables is less than the number of values, you can add an * to the variable name and the values will be assigned to the variable as a list:

Example
Assign the rest of the values as a list called "red":

fruits = ("apple", "banana", "cherry", "strawberry", "raspberry")

(green, yellow, *red) = fruits

print(green)
print(yellow)
print(red)
If the asterix is added to another variable name than the last, Python will assign values to the variable until the number of values left matches the number of variables left.

Example
Add a list of values the "tropic" variable:

fruits = ("apple", "mango", "papaya", "pineapple", "cherry")

(green, *tropic, red) = fruits

print(green)
print(tropic)
print(red)


### Python - Loop Tuples
Loop Through a Tuple
You can loop through the tuple items by using a for loop.

Example
Iterate through the items and print the values:

thistuple = ("apple", "banana", "cherry")
for x in thistuple:
  print(x)
Learn more about for loops in our Python For Loops Chapter.

Loop Through the Index Numbers
You can also loop through the tuple items by referring to their index number.

Use the range() and len() functions to create a suitable iterable.

Example
Print all items by referring to their index number:

thistuple = ("apple", "banana", "cherry")
for i in range(len(thistuple)):
  print(thistuple[i])


### Python - Join Tuples
Join Two Tuples
To join two or more tuples you can use the + operator:

Example
Join two tuples:

tuple1 = ("a", "b" , "c")
tuple2 = (1, 2, 3)

tuple3 = tuple1 + tuple2
print(tuple3)
Multiply Tuples
If you want to multiply the content of a tuple a given number of times, you can use the * operator:

Example
Multiply the fruits tuple by 2:

fruits = ("apple", "banana", "cherry")
mytuple = fruits * 2

print(mytuple)


### Python Sets
myset = {"apple", "banana", "cherry"}
Set
Sets are used to store multiple items in a single variable.

Set is one of 4 built-in data types in Python used to store collections of data, the other 3 are List, Tuple, and Dictionary, all with different qualities and usage.

A set is a collection which is both unordered and unindexed.

Sets are written with curly brackets.

Example
Create a Set:

thisset = {"apple", "banana", "cherry"}
print(thisset)
Note: Sets are unordered, so you cannot be sure in which order the items will appear.

Set Items
Set items are unordered, unchangeable, and do not allow duplicate values.

Unordered
Unordered means that the items in a set do not have a defined order.

Set items can appear in a different order every time you use them, and cannot be referred to by index or key.

Unchangeable
Sets are unchangeable, meaning that we cannot change the items after the set has been created.

Once a set is created, you cannot change its items, but you can add new items.

Duplicates Not Allowed
Sets cannot have two items with the same value.

Example
Duplicate values will be ignored:

thisset = {"apple", "banana", "cherry", "apple"}

print(thisset)


### Python - Access Set Items
Access Items
You cannot access items in a set by referring to an index or a key.

But you can loop through the set items using a for loop, or ask if a specified value is present in a set, by using the in keyword.

Example
Loop through the set, and print the values:

thisset = {"apple", "banana", "cherry"}

for x in thisset:
  print(x)
Example
Check if "banana" is present in the set:

thisset = {"apple", "banana", "cherry"}

print("banana" in thisset)


### Python - Add Set Items
Add Items
Once a set is created, you cannot change its items, but you can add new items.

To add one item to a set use the add() method.

Example
Add an item to a set, using the add() method:

thisset = {"apple", "banana", "cherry"}

thisset.add("orange")

print(thisset)
Add Sets
To add items from another set into the current set, use the update() method.

Example
Add elements from tropical and thisset into newset:

thisset = {"apple", "banana", "cherry"}
tropical = {"pineapple", "mango", "papaya"}

thisset.update(tropical)

print(thisset)
Add Any Iterable
The object in the update() method does not have be a set, it can be any iterable object (tuples, lists, dictionaries etc.).

Example
Add elements of a list to at set:

thisset = {"apple", "banana", "cherry"}
mylist = ["kiwi", "orange"]

thisset.update(mylist)

print(thisset)


### Python - Remove Set Items
Remove Item
To remove an item in a set, use the remove(), or the discard() method.

Example
Remove "banana" by using the remove() method:

thisset = {"apple", "banana", "cherry"}

thisset.remove("banana")

print(thisset)
Note: If the item to remove does not exist, remove() will raise an error.

Example
Remove "banana" by using the discard() method:

thisset = {"apple", "banana", "cherry"}

thisset.discard("banana")

print(thisset)
Note: If the item to remove does not exist, discard() will NOT raise an error.

You can also use the pop() method to remove an item, but this method will remove the last item. Remember that sets are unordered, so you will not know what item that gets removed.

The return value of the pop() method is the removed item.

Example
Remove the last item by using the pop() method:

thisset = {"apple", "banana", "cherry"}

x = thisset.pop()

print(x)

print(thisset)
Note: Sets are unordered, so when using the pop() method, you do not know which item that gets removed.

Example
The clear() method empties the set:

thisset = {"apple", "banana", "cherry"}

thisset.clear()

print(thisset)
Example
The del keyword will delete the set completely:

thisset = {"apple", "banana", "cherry"}

del thisset

print(thisset)


### Python - Loop Sets
Loop Items
You can loop through the set items by using a for loop:

Example
Loop through the set, and print the values:

thisset = {"apple", "banana", "cherry"}

for x in thisset:
  print(x)


Python - Join Sets
Join Two Sets
There are several ways to join two or more sets in Python.

You can use the union() method that returns a new set containing all items from both sets, or the update() method that inserts all the items from one set into another:

Example
The union() method returns a new set with all items from both sets:

set1 = {"a", "b" , "c"}
set2 = {1, 2, 3}

set3 = set1.union(set2)
print(set3)
Example
The update() method inserts the items in set2 into set1:

set1 = {"a", "b" , "c"}
set2 = {1, 2, 3}

set1.update(set2)
print(set1)
Note: Both union() and update() will exclude any duplicate items.

Keep ONLY the Duplicates
The intersection_update() method will keep only the items that are present in both sets.

Example
Keep the items that exist in both set x, and set y:

x = {"apple", "banana", "cherry"}
y = {"google", "microsoft", "apple"}

x.intersection_update(y)

print(x)
The intersection() method will return a new set, that only contains the items that are present in both sets.

Example
Return a set that contains the items that exist in both set x, and set y:

x = {"apple", "banana", "cherry"}
y = {"google", "microsoft", "apple"}

z = x.intersection(y)

print(z)
Keep All, But NOT the Duplicates
The symmetric_difference_update() method will keep only the elements that are NOT present in both sets.

Example
Keep the items that are not present in both sets:

x = {"apple", "banana", "cherry"}
y = {"google", "microsoft", "apple"}

x.symmetric_difference_update(y)

print(x)
The symmetric_difference() method will return a new set, that contains only the elements that are NOT present in both sets.

Example
Return a set that contains all items from both sets, except items that are present in both:

x = {"apple", "banana", "cherry"}
y = {"google", "microsoft", "apple"}

z = x.symmetric_difference(y)

print(z)


Python Dictionaries
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
Dictionary
Dictionaries are used to store data values in key:value pairs.

A dictionary is a collection which is ordered*, changeable and does not allow duplicates.

As of Python version 3.7, dictionaries are ordered. In Python 3.6 and earlier, dictionaries are unordered.

Dictionaries are written with curly brackets, and have keys and values:

Example
Create and print a dictionary:

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(thisdict)
Dictionary Items
Dictionary items are ordered, changeable, and does not allow duplicates.

Dictionary items are presented in key:value pairs, and can be referred to by using the key name.

Example
Print the "brand" value of the dictionary:

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(thisdict["brand"])
Ordered or Unordered?
As of Python version 3.7, dictionaries are ordered. In Python 3.6 and earlier, dictionaries are unordered.

When we say that dictionaries are ordered, it means that the items have a defined order, and that order will not change.

Unordered means that the items does not have a defined order, you cannot refer to an item by using an index.

Changeable
Dictionaries are changeable, meaning that we can change, add or remove items after the dictionary has been created.

Duplicates Not Allowed
Dictionaries cannot have two items with the same key:

Example
Duplicate values will overwrite existing values:

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964,
  "year": 2020
}
print(thisdict)


### Python - Access Dictionary Items
Accessing Items
You can access the items of a dictionary by referring to its key name, inside square brackets:

Example
Get the value of the "model" key:

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
x = thisdict["model"]
There is also a method called get() that will give you the same result:

Example
Get the value of the "model" key:

x = thisdict.get("model")
Get Keys
The keys() method will return a list of all the keys in the dictionary.

Example
Get a list of the keys:

x = thisdict.keys()
The list of the keys is a view of the dictionary, meaning that any changes done to the dictionary will be reflected in the keys list.

Example
Add a new item to the original dictionary, and see that the keys list gets updated as well:

car = {
"brand": "Ford",
"model": "Mustang",
"year": 1964
}

x = car.keys()

print(x) #before the change

car["color"] = "white"

print(x) #after the change
ADVERTISEMENT


Get Values
The values() method will return a list of all the values in the dictionary.

Example
Get a list of the values:

x = thisdict.values()
The list of the values is a view of the dictionary, meaning that any changes done to the dictionary will be reflected in the values list.

Example
Make a change in the original dictionary, and see that the values list gets updated as well:

car = {
"brand": "Ford",
"model": "Mustang",
"year": 1964
}

x = car.values()

print(x) #before the change

car["year"] = 2020

print(x) #after the change
Example
Add a new item to the original dictionary, and see that the values list gets updated as well:

car = {
"brand": "Ford",
"model": "Mustang",
"year": 1964
}

x = car.values()

print(x) #before the change

car["color"] = "red"

print(x) #after the change
Get Items
The items() method will return each item in a dictionary, as tuples in a list.

Example
Get a list of the key:value pairs

x = thisdict.items()
The returned list is a view of the items of the dictionary, meaning that any changes done to the dictionary will be reflected in the items list.

Example
Make a change in the original dictionary, and see that the items list gets updated as well:

car = {
"brand": "Ford",
"model": "Mustang",
"year": 1964
}

x = car.items()

print(x) #before the change

car["year"] = 2020

print(x) #after the change
Example
Add a new item to the original dictionary, and see that the items list gets updated as well:

car = {
"brand": "Ford",
"model": "Mustang",
"year": 1964
}

x = car.items()

print(x) #before the change

car["color"] = "red"

print(x) #after the change
Check if Key Exists
To determine if a specified key is present in a dictionary use the in keyword:

Example
Check if "model" is present in the dictionary:

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
if "model" in thisdict:
  print("Yes, 'model' is one of the keys in the thisdict dictionary")


### Python - Change Dictionary Items
Change Values
You can change the value of a specific item by referring to its key name:

Example
Change the "year" to 2018:

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict["year"] = 2018
Update Dictionary
The update() method will update the dictionary with the items from the given argument.

The argument must be a dictionary, or an iterable object with key:value pairs.

Example
Update the "year" of the car by using the update() method:

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.update({"year": 2020})


### Python - Add Dictionary Items
Adding Items
Adding an item to the dictionary is done by using a new index key and assigning a value to it:

Example
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict["color"] = "red"
print(thisdict)
Update Dictionary
The update() method will update the dictionary with the items from a given argument. If the item does not exist, the item will be added.

The argument must be a dictionary, or an iterable object with key:value pairs.

Example
Add a color item to the dictionary by using the update() method:

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.update({"color": "red"})


### Python - Remove Dictionary Items
Removing Items
There are several methods to remove items from a dictionary:

Example
The pop() method removes the item with the specified key name:

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.pop("model")
print(thisdict)
Example
The popitem() method removes the last inserted item (in versions before 3.7, a random item is removed instead):

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.popitem()
print(thisdict)
Example
The del keyword removes the item with the specified key name:

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
del thisdict["model"]
print(thisdict)
Example
The del keyword can also delete the dictionary completely:

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
del thisdict
print(thisdict) #this will cause an error because "thisdict" no longer exists.
Example
The clear() method empties the dictionary:

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.clear()
print(thisdict)


### Python - Loop Dictionaries
Loop Through a Dictionary
You can loop through a dictionary by using a for loop.

When looping through a dictionary, the return value are the keys of the dictionary, but there are methods to return the values as well.

Example
Print all key names in the dictionary, one by one:

for x in thisdict:
  print(x)
Example
Print all values in the dictionary, one by one:

for x in thisdict:
  print(thisdict[x])
Example
You can also use the values() method to return values of a dictionary:

for x in thisdict.values():
  print(x)
Example
You can use the keys() method to return the keys of a dictionary:

for x in thisdict.keys():
  print(x)
Example
Loop through both keys and values, by using the items() method:

for x, y in thisdict.items():
  print(x, y)

### Python - Copy Dictionaries
Copy a Dictionary
You cannot copy a dictionary simply by typing dict2 = dict1, because: dict2 will only be a reference to dict1, and changes made in dict1 will automatically also be made in dict2.

There are ways to make a copy, one way is to use the built-in Dictionary method copy().

Example
Make a copy of a dictionary with the copy() method:

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
mydict = thisdict.copy()
print(mydict)
Another way to make a copy is to use the built-in function dict().

Example
Make a copy of a dictionary with the dict() function:

thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
mydict = dict(thisdict)
print(mydict)

### Python - Nested Dictionaries
Nested Dictionaries
A dictionary can contain dictionaries, this is called nested dictionaries.

Example
Create a dictionary that contain three dictionaries:

myfamily = {
  "child1" : {
    "name" : "Emil",
    "year" : 2004
  },
  "child2" : {
    "name" : "Tobias",
    "year" : 2007
  },
  "child3" : {
    "name" : "Linus",
    "year" : 2011
  }
}
Or, if you want to add three dictionaries into a new dictionary:

Example
Create three dictionaries, then create one dictionary that will contain the other three dictionaries:

child1 = {
  "name" : "Emil",
  "year" : 2004
}
child2 = {
  "name" : "Tobias",
  "year" : 2007
}
child3 = {
  "name" : "Linus",
  "year" : 2011
}

myfamily = {
  "child1" : child1,
  "child2" : child2,
  "child3" : child3
}

### Python If ... Else
Python Conditions and If statements
Python supports the usual logical conditions from mathematics:

Equals: a == b
Not Equals: a != b
Less than: a < b
Less than or equal to: a <= b
Greater than: a > b
Greater than or equal to: a >= b
These conditions can be used in several ways, most commonly in "if statements" and loops.

An "if statement" is written by using the if keyword.

Example
If statement:

a = 33
b = 200
if b > a:
  print("b is greater than a")
In this example we use two variables, a and b, which are used as part of the if statement to test whether b is greater than a. As a is 33, and b is 200, we know that 200 is greater than 33, and so we print to screen that "b is greater than a".

Indentation
Python relies on indentation (whitespace at the beginning of a line) to define scope in the code. Other programming languages often use curly-brackets for this purpose.

Example
If statement, without indentation (will raise an error):

a = 33
b = 200
if b > a:
print("b is greater than a") # you will get an error
ADVERTISEMENT


Elif
The elif keyword is pythons way of saying "if the previous conditions were not true, then try this condition".

Example
a = 33
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
In this example a is equal to b, so the first condition is not true, but the elif condition is true, so we print to screen that "a and b are equal".

Else
The else keyword catches anything which isn't caught by the preceding conditions.

Example
a = 200
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
else:
  print("a is greater than b")
In this example a is greater than b, so the first condition is not true, also the elif condition is not true, so we go to the else condition and print to screen that "a is greater than b".

You can also have an else without the elif:

Example
a = 200
b = 33
if b > a:
  print("b is greater than a")
else:
  print("b is not greater than a")
Short Hand If
If you have only one statement to execute, you can put it on the same line as the if statement.

Example
One line if statement:

if a > b: print("a is greater than b")
Short Hand If ... Else
If you have only one statement to execute, one for if, and one for else, you can put it all on the same line:

Example
One line if else statement:

a = 2
b = 330
print("A") if a > b else print("B")
This technique is known as Ternary Operators, or Conditional Expressions.

You can also have multiple else statements on the same line:

Example
One line if else statement, with 3 conditions:

a = 330
b = 330
print("A") if a > b else print("=") if a == b else print("B")
And
The and keyword is a logical operator, and is used to combine conditional statements:

Example
Test if a is greater than b, AND if c is greater than a:

a = 200
b = 33
c = 500
if a > b and c > a:
  print("Both conditions are True")
Or
The or keyword is a logical operator, and is used to combine conditional statements:

Example
Test if a is greater than b, OR if a is greater than c:

a = 200
b = 33
c = 500
if a > b or a > c:
  print("At least one of the conditions is True")
Nested If
You can have if statements inside if statements, this is called nested if statements.

Example
x = 41

if x > 10:
  print("Above ten,")
  if x > 20:
    print("and also above 20!")
  else:
    print("but not above 20.")
The pass Statement
if statements cannot be empty, but if you for some reason have an if statement with no content, put in the pass statement to avoid getting an error.

Example
a = 33
b = 200

if b > a:
  pass

### Python While Loops
Python Loops
Python has two primitive loop commands:

while loops
for loops
The while Loop
With the while loop we can execute a set of statements as long as a condition is true.

Example
Print i as long as i is less than 6:

i = 1
while i < 6:
  print(i)
  i += 1
Note: remember to increment i, or else the loop will continue forever.

The while loop requires relevant variables to be ready, in this example we need to define an indexing variable, i, which we set to 1.

The break Statement
With the break statement we can stop the loop even if the while condition is true:

Example
Exit the loop when i is 3:

i = 1
while i < 6:
  print(i)
  if i == 3:
    break
  i += 1
ADVERTISEMENT


The continue Statement
With the continue statement we can stop the current iteration, and continue with the next:

Example
Continue to the next iteration if i is 3:

i = 0
while i < 6:
  i += 1
  if i == 3:
    continue
  print(i)
The else Statement
With the else statement we can run a block of code once when the condition no longer is true:

Example
Print a message once the condition is false:

i = 1
while i < 6:
  print(i)
  i += 1
else:
  print("i is no longer less than 6")


### Python For Loops
Python For Loops
A for loop is used for iterating over a sequence (that is either a list, a tuple, a dictionary, a set, or a string).

This is less like the for keyword in other programming languages, and works more like an iterator method as found in other object-orientated programming languages.

With the for loop we can execute a set of statements, once for each item in a list, tuple, set etc.

Example
Print each fruit in a fruit list:

fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x)
The for loop does not require an indexing variable to set beforehand.

Looping Through a String
Even strings are iterable objects, they contain a sequence of characters:

Example
Loop through the letters in the word "banana":

for x in "banana":
  print(x)
The break Statement
With the break statement we can stop the loop before it has looped through all the items:

Example
Exit the loop when x is "banana":

fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x)
  if x == "banana":
    break
Example
Exit the loop when x is "banana", but this time the break comes before the print:

fruits = ["apple", "banana", "cherry"]
for x in fruits:
  if x == "banana":
    break
  print(x)

### Python Functions
A function is a block of code which only runs when it is called.

You can pass data, known as parameters, into a function.

A function can return data as a result.

Creating a Function
In Python a function is defined using the def keyword:

Example
def my_function():
  print("Hello from a function")
Calling a Function
To call a function, use the function name followed by parenthesis:

Example
def my_function():
  print("Hello from a function")

my_function()
Arguments
Information can be passed into functions as arguments.

Arguments are specified after the function name, inside the parentheses. You can add as many arguments as you want, just separate them with a comma.

The following example has a function with one argument (fname). When the function is called, we pass along a first name, which is used inside the function to print the full name:

Example
def my_function(fname):
  print(fname + " Refsnes")

my_function("Emil")
my_function("Tobias")
my_function("Linus")


### Python Lambda
A lambda function is a small anonymous function.

A lambda function can take any number of arguments, but can only have one expression.

Syntax
lambda arguments : expression
The expression is executed and the result is returned:

Example
Add 10 to argument a, and return the result:

x = lambda a : a + 10
print(x(5))
Lambda functions can take any number of arguments:

Example
Multiply argument a with argument b and return the result:

x = lambda a, b : a * b
print(x(5, 6))
Example
Summarize argument a, b, and c and return the result:

x = lambda a, b, c : a + b + c
print(x(5, 6, 2))


### Python Arrays
Note: Python does not have built-in support for Arrays, but Python Lists can be used instead.

Arrays
Note: This page shows you how to use LISTS as ARRAYS, however, to work with arrays in Python you will have to import a library, like the NumPy library.

Arrays are used to store multiple values in one single variable:

Example
Create an array containing car names:

cars = ["Ford", "Volvo", "BMW"]
What is an Array?
An array is a special variable, which can hold more than one value at a time.

If you have a list of items (a list of car names, for example), storing the cars in single variables could look like this:

car1 = "Ford"
car2 = "Volvo"
car3 = "BMW"
However, what if you want to loop through the cars and find a specific one? And what if you had not 3 cars, but 300?

The solution is an array!

An array can hold many values under a single name, and you can access the values by referring to an index number.

Access the Elements of an Array
You refer to an array element by referring to the index number.

Example
Get the value of the first array item:

x = cars[0]
Example
Modify the value of the first array item:

cars[0] = "Toyota"
The Length of an Array
Use the len() method to return the length of an array (the number of elements in an array).

Example
Return the number of elements in the cars array:

x = len(cars)

Looping Array Elements
You can use the for in loop to loop through all the elements of an array.

Example
Print each item in the cars array:

for x in cars:
  print(x)
Adding Array Elements
You can use the append() method to add an element to an array.

Example
Add one more element to the cars array:

cars.append("Honda")
Removing Array Elements
You can use the pop() method to remove an element from the array.

Example
Delete the second element of the cars array:

cars.pop(1)
You can also use the remove() method to remove an element from the array.

Example
Delete the element that has the value "Volvo":

cars.remove("Volvo")


### Python Classes and Objects
Python Classes/Objects
Python is an object oriented programming language.

Almost everything in Python is an object, with its properties and methods.

A Class is like an object constructor, or a "blueprint" for creating objects.

Create a Class
To create a class, use the keyword class:

Example
Create a class named MyClass, with a property named x:

class MyClass:
  x = 5
Create Object
Now we can use the class named MyClass to create objects:

Example
Create an object named p1, and print the value of x:

p1 = MyClass()
print(p1.x)
The __init__() Function
The examples above are classes and objects in their simplest form, and are not really useful in real life applications.

To understand the meaning of classes we have to understand the built-in __init__() function.

All classes have a function called __init__(), which is always executed when the class is being initiated.

Use the __init__() function to assign values to object properties, or other operations that are necessary to do when the object is being created:

Example
Create a class named Person, use the __init__() function to assign values for name and age:

class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

p1 = Person("John", 36)

print(p1.name)
print(p1.age)
Note: The __init__() function is called automatically every time the class is being used to create a new object.

ADVERTISEMENT


Object Methods
Objects can also contain methods. Methods in objects are functions that belong to the object.

Let us create a method in the Person class:

Example
Insert a function that prints a greeting, and execute it on the p1 object:

class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

  def myfunc(self):
    print("Hello my name is " + self.name)

p1 = Person("John", 36)
p1.myfunc()
Note: The self parameter is a reference to the current instance of the class, and is used to access variables that belong to the class.

The self Parameter
The self parameter is a reference to the current instance of the class, and is used to access variables that belongs to the class.

It does not have to be named self , you can call it whatever you like, but it has to be the first parameter of any function in the class:

Example
Use the words mysillyobject and abc instead of self:

class Person:
  def __init__(mysillyobject, name, age):
    mysillyobject.name = name
    mysillyobject.age = age

  def myfunc(abc):
    print("Hello my name is " + abc.name)

p1 = Person("John", 36)
p1.myfunc()
Modify Object Properties
You can modify properties on objects like this:

Example
Set the age of p1 to 40:

p1.age = 40
Delete Object Properties
You can delete properties on objects by using the del keyword:

Example
Delete the age property from the p1 object:

del p1.age
Delete Objects
You can delete objects by using the del keyword:

Example
Delete the p1 object:

del p1
The pass Statement
class definitions cannot be empty, but if you for some reason have a class definition with no content, put in the pass statement to avoid getting an error.

Example
class Person:
  pass

### Python Inheritance
Python Inheritance
Inheritance allows us to define a class that inherits all the methods and properties from another class.

Parent class is the class being inherited from, also called base class.

Child class is the class that inherits from another class, also called derived class.

Create a Parent Class
Any class can be a parent class, so the syntax is the same as creating any other class:

Example
Create a class named Person, with firstname and lastname properties, and a printname method:

class Person:
  def __init__(self, fname, lname):
    self.firstname = fname
    self.lastname = lname

  def printname(self):
    print(self.firstname, self.lastname)

#Use the Person class to create an object, and then execute the printname method:

x = Person("John", "Doe")
x.printname()
Create a Child Class
To create a class that inherits the functionality from another class, send the parent class as a parameter when creating the child class:

Example
Create a class named Student, which will inherit the properties and methods from the Person class:

class Student(Person):
  pass
Note: Use the pass keyword when you do not want to add any other properties or methods to the class.

Now the Student class has the same properties and methods as the Person class.

Example
Use the Student class to create an object, and then execute the printname method:

x = Student("Mike", "Olsen")
x.printname()


### Python Iterators
Python Iterators
An iterator is an object that contains a countable number of values.

An iterator is an object that can be iterated upon, meaning that you can traverse through all the values.

Technically, in Python, an iterator is an object which implements the iterator protocol, which consist of the methods __iter__() and __next__().

Iterator vs Iterable
Lists, tuples, dictionaries, and sets are all iterable objects. They are iterable containers which you can get an iterator from.

All these objects have a iter() method which is used to get an iterator:

Example
Return an iterator from a tuple, and print each value:

mytuple = ("apple", "banana", "cherry")
myit = iter(mytuple)

print(next(myit))
print(next(myit))
print(next(myit))
Even strings are iterable objects, and can return an iterator:

Example
Strings are also iterable objects, containing a sequence of characters:

mystr = "banana"
myit = iter(mystr)

print(next(myit))
print(next(myit))
print(next(myit))
print(next(myit))
print(next(myit))
print(next(myit))
Looping Through an Iterator
We can also use a for loop to iterate through an iterable object:

Example
Iterate the values of a tuple:

mytuple = ("apple", "banana", "cherry")

for x in mytuple:
  print(x)
Example
Iterate the characters of a string:

mystr = "banana"

for x in mystr:
  print(x)
The for loop actually creates an iterator object and executes the next() method for each loop.

ADVERTISEMENT


Create an Iterator
To create an object/class as an iterator you have to implement the methods __iter__() and __next__() to your object.

As you have learned in the Python Classes/Objects chapter, all classes have a function called __init__(), which allows you to do some initializing when the object is being created.

The __iter__() method acts similar, you can do operations (initializing etc.), but must always return the iterator object itself.

The __next__() method also allows you to do operations, and must return the next item in the sequence.

Example
Create an iterator that returns numbers, starting with 1, and each sequence will increase by one (returning 1,2,3,4,5 etc.):

class MyNumbers:
  def __iter__(self):
    self.a = 1
    return self

  def __next__(self):
    x = self.a
    self.a += 1
    return x

myclass = MyNumbers()
myiter = iter(myclass)

print(next(myiter))
print(next(myiter))
print(next(myiter))
print(next(myiter))
print(next(myiter))
StopIteration
The example above would continue forever if you had enough next() statements, or if it was used in a for loop.

To prevent the iteration to go on forever, we can use the StopIteration statement.

In the __next__() method, we can add a terminating condition to raise an error if the iteration is done a specified number of times:

Example
Stop after 20 iterations:

class MyNumbers:
  def __iter__(self):
    self.a = 1
    return self

  def __next__(self):
    if self.a <= 20:
      x = self.a
      self.a += 1
      return x
    else:
      raise StopIteration

myclass = MyNumbers()
myiter = iter(myclass)

for x in myiter:
  print(x)


### Python Scope
A variable is only available from inside the region it is created. This is called scope.

Local Scope
A variable created inside a function belongs to the local scope of that function, and can only be used inside that function.

Example
A variable created inside a function is available inside that function:

def myfunc():
  x = 300
  print(x)

myfunc()
Function Inside Function
As explained in the example above, the variable x is not available outside the function, but it is available for any function inside the function:

Example
The local variable can be accessed from a function within the function:

def myfunc():
  x = 300
  def myinnerfunc():
    print(x)
  myinnerfunc()

myfunc()


### Python Modules
What is a Module?
Consider a module to be the same as a code library.

A file containing a set of functions you want to include in your application.

Create a Module
To create a module just save the code you want in a file with the file extension .py:

Example
Save this code in a file named mymodule.py

def greeting(name):
  print("Hello, " + name)
Use a Module
Now we can use the module we just created, by using the import statement:

Example
Import the module named mymodule, and call the greeting function:

import mymodule

mymodule.greeting("Jonathan")
Note: When using a function from a module, use the syntax: module_name.function_name.

Variables in Module
The module can contain functions, as already described, but also variables of all types (arrays, dictionaries, objects etc):

Example
Save this code in the file mymodule.py

person1 = {
  "name": "John",
  "age": 36,
  "country": "Norway"
}
Example
Import the module named mymodule, and access the person1 dictionary:

import mymodule

a = mymodule.person1["age"]
print(a)
ADVERTISEMENT


Naming a Module
You can name the module file whatever you like, but it must have the file extension .py

Re-naming a Module
You can create an alias when you import a module, by using the as keyword:

Example
Create an alias for mymodule called mx:

import mymodule as mx

a = mx.person1["age"]
print(a)
Built-in Modules
There are several built-in modules in Python, which you can import whenever you like.

Example
Import and use the platform module:

import platform

x = platform.system()
print(x)
Using the dir() Function
There is a built-in function to list all the function names (or variable names) in a module. The dir() function:

Example
List all the defined names belonging to the platform module:

import platform

x = dir(platform)
print(x)
Note: The dir() function can be used on all modules, also the ones you create yourself.

Import From Module
You can choose to import only parts from a module, by using the from keyword.

Example
The module named mymodule has one function and one dictionary:

def greeting(name):
  print("Hello, " + name)

person1 = {
  "name": "John",
  "age": 36,
  "country": "Norway"
}
Example
Import only the person1 dictionary from the module:

from mymodule import person1

print (person1["age"])


### Python Datetime
Python Dates
A date in Python is not a data type of its own, but we can import a module named datetime to work with dates as date objects.

Example
Import the datetime module and display the current date:

import datetime

x = datetime.datetime.now()
print(x)
Date Output
When we execute the code from the example above the result will be:

2021-04-22 11:23:35.663335
The date contains year, month, day, hour, minute, second, and microsecond.

The datetime module has many methods to return information about the date object.

Here are a few examples, you will learn more about them later in this chapter:

Example
Return the year and name of weekday:

import datetime

x = datetime.datetime.now()

print(x.year)
print(x.strftime("%A"))
Creating Date Objects
To create a date, we can use the datetime() class (constructor) of the datetime module.

The datetime() class requires three parameters to create a date: year, month, day.

Example
Create a date object:

import datetime

x = datetime.datetime(2020, 5, 17)

print(x)
The datetime() class also takes parameters for time and timezone (hour, minute, second, microsecond, tzone), but they are optional, and has a default value of 0, (None for timezone).

ADVERTISEMENT


The strftime() Method
The datetime object has a method for formatting date objects into readable strings.

The method is called strftime(), and takes one parameter, format, to specify the format of the returned string:

Example
Display the name of the month:

import datetime

x = datetime.datetime(2018, 6, 1)

print(x.strftime("%B"))
A reference of all the legal format codes:

Directive	Description	Example	Try it
%a	Weekday, short version	Wed	
%A	Weekday, full version	Wednesday	
%w	Weekday as a number 0-6, 0 is Sunday	3	
%d	Day of month 01-31	31	
%b	Month name, short version	Dec	
%B	Month name, full version	December	
%m	Month as a number 01-12	12	
%y	Year, short version, without century	18	
%Y	Year, full version	2018	
%H	Hour 00-23	17	
%I	Hour 00-12	05	
%p	AM/PM	PM	
%M	Minute 00-59	41	
%S	Second 00-59	08	
%f	Microsecond 000000-999999	548513	
%z	UTC offset	+0100	
%Z	Timezone	CST	
%j	Day number of year 001-366	365	
%U	Week number of year, Sunday as the first day of week, 00-53	52	
%W	Week number of year, Monday as the first day of week, 00-53	52	
%c	Local version of date and time	Mon Dec 31 17:41:00 2018	
%x	Local version of date	12/31/18	
%X	Local version of time	17:41:00	
%%	A % character	%	
%G	ISO 8601 year	2018	
%u	ISO 8601 weekday (1-7)	1	
%V	ISO 8601 weeknumber (01-53)	01	



Python Math
Python has a set of built-in math functions, including an extensive math module, that allows you to perform mathematical tasks on numbers.

Built-in Math Functions
The min() and max() functions can be used to find the lowest or highest value in an iterable:

Example
x = min(5, 10, 25)
y = max(5, 10, 25)

print(x)
print(y)
The abs() function returns the absolute (positive) value of the specified number:

Example
x = abs(-7.25)

print(x)
The pow(x, y) function returns the value of x to the power of y (xy).

Example
Return the value of 4 to the power of 3 (same as 4 * 4 * 4):

x = pow(4, 3)

print(x)
The Math Module
Python has also a built-in module called math, which extends the list of mathematical functions.

To use it, you must import the math module:

import math
When you have imported the math module, you can start using methods and constants of the module.

The math.sqrt() method for example, returns the square root of a number:

Example
import math

x = math.sqrt(64)

print(x)
The math.ceil() method rounds a number upwards to its nearest integer, and the math.floor() method rounds a number downwards to its nearest integer, and returns the result:

Example
import math

x = math.ceil(1.4)
y = math.floor(1.4)

print(x) # returns 2
print(y) # returns 1
The math.pi constant, returns the value of PI (3.14...):

Example
import math

x = math.pi

print(x)


### Python JSON
JSON is a syntax for storing and exchanging data.

JSON is text, written with JavaScript object notation.

JSON in Python
Python has a built-in package called json, which can be used to work with JSON data.

Example
Import the json module:

import json
Parse JSON - Convert from JSON to Python
If you have a JSON string, you can parse it by using the json.loads() method.

The result will be a Python dictionary.

Example
Convert from JSON to Python:

import json

# some JSON:
x =  '{ "name":"John", "age":30, "city":"New York"}'

# parse x:
y = json.loads(x)

# the result is a Python dictionary:
print(y["age"])
Convert from Python to JSON
If you have a Python object, you can convert it into a JSON string by using the json.dumps() method.

Example
Convert from Python to JSON:

import json

# a Python object (dict):
x = {
  "name": "John",
  "age": 30,
  "city": "New York"
}

# convert into JSON:
y = json.dumps(x)

# the result is a JSON string:
print(y)
ADVERTISEMENT


You can convert Python objects of the following types, into JSON strings:

dict
list
tuple
string
int
float
True
False
None
Example
Convert Python objects into JSON strings, and print the values:

import json

print(json.dumps({"name": "John", "age": 30}))
print(json.dumps(["apple", "bananas"]))
print(json.dumps(("apple", "bananas")))
print(json.dumps("hello"))
print(json.dumps(42))
print(json.dumps(31.76))
print(json.dumps(True))
print(json.dumps(False))
print(json.dumps(None))
When you convert from Python to JSON, Python objects are converted into the JSON (JavaScript) equivalent:

Python	JSON
dict	Object
list	Array
tuple	Array
str	String
int	Number
float	Number
True	true
False	false
None	null
Example
Convert a Python object containing all the legal data types:

import json

x = {
  "name": "John",
  "age": 30,
  "married": True,
  "divorced": False,
  "children": ("Ann","Billy"),
  "pets": None,
  "cars": [
    {"model": "BMW 230", "mpg": 27.5},
    {"model": "Ford Edge", "mpg": 24.1}
  ]
}

print(json.dumps(x))
Format the Result
The example above prints a JSON string, but it is not very easy to read, with no indentations and line breaks.

The json.dumps() method has parameters to make it easier to read the result:

Example
Use the indent parameter to define the numbers of indents:

json.dumps(x, indent=4)
You can also define the separators, default value is (", ", ": "), which means using a comma and a space to separate each object, and a colon and a space to separate keys from values:

Example
Use the separators parameter to change the default separator:

json.dumps(x, indent=4, separators=(". ", " = "))
Order the Result
The json.dumps() method has parameters to order the keys in the result:

Example
Use the sort_keys parameter to specify if the result should be sorted or not:

json.dumps(x, indent=4, sort_keys=True)


### Python RegEx
A RegEx, or Regular Expression, is a sequence of characters that forms a search pattern.

RegEx can be used to check if a string contains the specified search pattern.

RegEx Module
Python has a built-in package called re, which can be used to work with Regular Expressions.

Import the re module:

import re
RegEx in Python
When you have imported the re module, you can start using regular expressions:

Example
Search the string to see if it starts with "The" and ends with "Spain":

import re

txt = "The rain in Spain"
x = re.search("^The.*Spain$", txt)
RegEx Functions
The re module offers a set of functions that allows us to search a string for a match:

Function	Description
findall	Returns a list containing all matches
search	Returns a Match object if there is a match anywhere in the string
split	Returns a list where the string has been split at each match
sub	Replaces one or many matches with a string
ADVERTISEMENT


Metacharacters
Metacharacters are characters with a special meaning:

Character	Description	Example	Try it
[]	A set of characters	"[a-m]"
\	Signals a special sequence (can also be used to escape special characters)	"\d"
.	Any character (except newline character)	"he..o"
^	Starts with	"^hello"
$	Ends with	"world$"
*	Zero or more occurrences	"aix*"
+	One or more occurrences	"aix+"
{}	Exactly the specified number of occurrences	"al{2}"
|	Either or	"falls|stays"
()	Capture and group
Special Sequences
A special sequence is a \ followed by one of the characters in the list below, and has a special meaning:

Character	Description	Example	Try it
\A	Returns a match if the specified characters are at the beginning of the string	"\AThe"
\b	Returns a match where the specified characters are at the beginning or at the end of a word
(the "r" in the beginning is making sure that the string is being treated as a "raw string")	r"\bain"
r"ain\b"
\B	Returns a match where the specified characters are present, but NOT at the beginning (or at the end) of a word
(the "r" in the beginning is making sure that the string is being treated as a "raw string")	r"\Bain"
r"ain\B"
\d	Returns a match where the string contains digits (numbers from 0-9)	"\d"
\D	Returns a match where the string DOES NOT contain digits	"\D"
\s	Returns a match where the string contains a white space character	"\s"
\S	Returns a match where the string DOES NOT contain a white space character	"\S"
\w	Returns a match where the string contains any word characters (characters from a to Z, digits from 0-9, and the underscore _ character)	"\w"
\W	Returns a match where the string DOES NOT contain any word characters	"\W"
\Z	Returns a match if the specified characters are at the end of the string	"Spain\Z"
Sets
A set is a set of characters inside a pair of square brackets [] with a special meaning:

Set	Description	Try it
[arn]	Returns a match where one of the specified characters (a, r, or n) are present
[a-n]	Returns a match for any lower case character, alphabetically between a and n
[^arn]	Returns a match for any character EXCEPT a, r, and n
[0123]	Returns a match where any of the specified digits (0, 1, 2, or 3) are present
[0-9]	Returns a match for any digit between 0 and 9
[0-5][0-9]	Returns a match for any two-digit numbers from 00 and 59
[a-zA-Z]	Returns a match for any character alphabetically between a and z, lower case OR upper case
[+]	In sets, +, *, ., |, (), $,{} has no special meaning, so [+] means: return a match for any + character in the string

The findall() Function
The findall() function returns a list containing all matches.

Example
Print a list of all matches:

import re

txt = "The rain in Spain"
x = re.findall("ai", txt)
print(x)
The list contains the matches in the order they are found.

If no matches are found, an empty list is returned:

Example
Return an empty list if no match was found:

import re

txt = "The rain in Spain"
x = re.findall("Portugal", txt)
print(x)

The search() Function
The search() function searches the string for a match, and returns a Match object if there is a match.

If there is more than one match, only the first occurrence of the match will be returned:

Example
Search for the first white-space character in the string:

import re

txt = "The rain in Spain"
x = re.search("\s", txt)

print("The first white-space character is located in position:", x.start())
If no matches are found, the value None is returned:

Example
Make a search that returns no match:

import re

txt = "The rain in Spain"
x = re.search("Portugal", txt)
print(x)

The split() Function
The split() function returns a list where the string has been split at each match:

Example
Split at each white-space character:

import re

txt = "The rain in Spain"
x = re.split("\s", txt)
print(x)
You can control the number of occurrences by specifying the maxsplit parameter:

Example
Split the string only at the first occurrence:

import re

txt = "The rain in Spain"
x = re.split("\s", txt, 1)
print(x)

The sub() Function
The sub() function replaces the matches with the text of your choice:

Example
Replace every white-space character with the number 9:

import re

txt = "The rain in Spain"
x = re.sub("\s", "9", txt)
print(x)
You can control the number of replacements by specifying the count parameter:

Example
Replace the first 2 occurrences:

import re

txt = "The rain in Spain"
x = re.sub("\s", "9", txt, 2)
print(x)

Match Object
A Match Object is an object containing information about the search and the result.

Note: If there is no match, the value None will be returned, instead of the Match Object.

Example
Do a search that will return a Match Object:

import re

txt = "The rain in Spain"
x = re.search("ai", txt)
print(x) #this will print an object
The Match object has properties and methods used to retrieve information about the search, and the result:

.span() returns a tuple containing the start-, and end positions of the match.
.string returns the string passed into the function
.group() returns the part of the string where there was a match
Example
Print the position (start- and end-position) of the first match occurrence.

The regular expression looks for any words that starts with an upper case "S":

import re

txt = "The rain in Spain"
x = re.search(r"\bS\w+", txt)
print(x.span())
Example
Print the string passed into the function:

import re

txt = "The rain in Spain"
x = re.search(r"\bS\w+", txt)
print(x.string)
Example
Print the part of the string where there was a match.

The regular expression looks for any words that starts with an upper case "S":

import re

txt = "The rain in Spain"
x = re.search(r"\bS\w+", txt)
print(x.group())


###  Python Try Except
The try block lets you test a block of code for errors.

The except block lets you handle the error.

The finally block lets you execute code, regardless of the result of the try- and except blocks.

Exception Handling
When an error occurs, or exception as we call it, Python will normally stop and generate an error message.

These exceptions can be handled using the try statement:

Example
The try block will generate an exception, because x is not defined:

try:
  print(x)
except:
  print("An exception occurred")
Since the try block raises an error, the except block will be executed.

Without the try block, the program will crash and raise an error:

Example
This statement will raise an error, because x is not defined:

print(x)
Many Exceptions
You can define as many exception blocks as you want, e.g. if you want to execute a special block of code for a special kind of error:

Example
Print one message if the try block raises a NameError and another for other errors:

try:
  print(x)
except NameError:
  print("Variable x is not defined")
except:
  print("Something else went wrong")
ADVERTISEMENT


Else
You can use the else keyword to define a block of code to be executed if no errors were raised:

Example
In this example, the try block does not generate any error:

try:
  print("Hello")
except:
  print("Something went wrong")
else:
  print("Nothing went wrong")
Finally
The finally block, if specified, will be executed regardless if the try block raises an error or not.

Example
try:
  print(x)
except:
  print("Something went wrong")
finally:
  print("The 'try except' is finished")
This can be useful to close objects and clean up resources:

Example
Try to open and write to a file that is not writable:

try:
  f = open("demofile.txt")
  f.write("Lorum Ipsum")
except:
  print("Something went wrong when writing to the file")
finally:
  f.close()
The program can continue, without leaving the file object open.

Raise an exception
As a Python developer you can choose to throw an exception if a condition occurs.

To throw (or raise) an exception, use the raise keyword.

Example
Raise an error and stop the program if x is lower than 0:

x = -1

if x < 0:
  raise Exception("Sorry, no numbers below zero")
The raise keyword is used to raise an exception.

You can define what kind of error to raise, and the text to print to the user.

Example
Raise a TypeError if x is not an integer:

x = "hello"

if not type(x) is int:
  raise TypeError("Only integers are allowed")



### Python File Open
File handling is an important part of any web application.

Python has several functions for creating, reading, updating, and deleting files.

File Handling
The key function for working with files in Python is the open() function.

The open() function takes two parameters; filename, and mode.

There are four different methods (modes) for opening a file:

"r" - Read - Default value. Opens a file for reading, error if the file does not exist

"a" - Append - Opens a file for appending, creates the file if it does not exist

"w" - Write - Opens a file for writing, creates the file if it does not exist

"x" - Create - Creates the specified file, returns an error if the file exists

In addition you can specify if the file should be handled as binary or text mode

"t" - Text - Default value. Text mode

"b" - Binary - Binary mode (e.g. images)

Syntax
To open a file for reading it is enough to specify the name of the file:

f = open("demofile.txt")
The code above is the same as:

f = open("demofile.txt", "rt")
Because "r" for read, and "t" for text are the default values, you do not need to specify them.


### Python File Write
Write to an Existing File
To write to an existing file, you must add a parameter to the open() function:

"a" - Append - will append to the end of the file

"w" - Write - will overwrite any existing content

Example
Open the file "demofile2.txt" and append content to the file:

f = open("demofile2.txt", "a")
f.write("Now the file has more content!")
f.close()

#open and read the file after the appending:
f = open("demofile2.txt", "r")
print(f.read())
Example
Open the file "demofile3.txt" and overwrite the content:

f = open("demofile3.txt", "w")
f.write("Woops! I have deleted the content!")
f.close()

#open and read the file after the appending:
f = open("demofile3.txt", "r")
print(f.read())
Note: the "w" method will overwrite the entire file.

Create a New File
To create a new file in Python, use the open() method, with one of the following parameters:

"x" - Create - will create a file, returns an error if the file exist

"a" - Append - will create a file if the specified file does not exist

"w" - Write - will create a file if the specified file does not exist

Example
Create a file called "myfile.txt":

f = open("myfile.txt", "x")
Result: a new empty file is created!

Example
Create a new file if it does not exist:

f = open("myfile.txt", "w")

### Python Delete File
Delete a File
To delete a file, you must import the OS module, and run its os.remove() function:

Example
Remove the file "demofile.txt":

import os
os.remove("demofile.txt")
Check if File exist:
To avoid getting an error, you might want to check if the file exists before you try to delete it:

Example
Check if file exists, then delete it:

import os
if os.path.exists("demofile.txt"):
  os.remove("demofile.txt")
else:
  print("The file does not exist")
Delete Folder
To delete an entire folder, use the os.rmdir() method:

Example
Remove the folder "myfolder":

import os
os.rmdir("myfolder")







