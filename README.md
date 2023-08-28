# How to Write Code 

**1. It should read like a Story**

:smile:Good Code                  |            :cry:Bad Code: 
```
guess_count = 0                           
guess_limit = 3                         # i = 0 
while guess_count < guess_limit:        # while i < 3:
```

**2. Don't duplicate yourself**

:cry:Bad Example with many times .upper() method

```
user_input = str(input("> "))

    if user_input.upper() == "HELP":
        print(help_txt)

    elif user_input.upper() == "START":
        print(start_txt)

    elif user_input.upper() == "STOP":
        print(stop_txt)
```

:smile:Good Example with upper method directly defined @ the input

```
 user_input = str(input("> ")).upper()

    if user_input == "HELP":
        print(help_txt)

    elif user_input == "START":
        print(start_txt)

    elif user_input == "STOP":
        print(stop_txt)
```

# Convert Value

**Convert a value to a different type**

```
int(Value)     # convert to integer - whole number
float(Value)   # convert to float - floating point number
bool(Value)    # convert to boolean - True or False
str(Value)     # convert to string - text
list(Value)    # convert to list - mutable sequence
```

**Example:** Convert a string to a integer 

```
first_nr = float(input("Give me a first Number: "))     # Convert the input to a float
second_nr = float(input("Give me a second Number: "))   # Convert the input to a float

sum = str(first_nr + second_nr)                         # Convert the sum to a string
print("Sum: " + sum)                                    # Print the sum
```

# Functions

**A function is a block of code which only runs when it is called.**

**Example:** A function that prints a message

```
def greet(name):                        # def = define a function
    return f"Hello, {name}!"            # What the function does

result = greet("Alice")                 # Call the function with a value "Alice"
print(result)  # Output: Hello, Alice!  # Print the result
```

# Modules / Methods

**Methods are functions associated with specific objects or classes, designed to operate on those objects' data and behavior.**

> They get called with a dot, like this: object.method()

```
"Python for Beginners"      # is an object of the class "String".
course = "Python for Beginners"
course.                     # To see all the methods of the class "String" you can use the dot.
course.upper()              # This method converts the string to uppercase.
course.lower()              # This method converts the string to lowercase.
```


**Example:** Upper Method

```
course = 'Python for Beginners'
BIG = course.upper()            
print(BIG)                              # PYTHON FOR BEGINNERS
print(course)                           # Python for Beginners

BIG = course.replace('for' , '4')       # Replace "for" with 4
print(BIG)                              # Python 4 Beginners
```

**Example:** Find Method

```
course = 'Python for Beginners'
# Index   0123456789

Find = course.find('n')      # Find the first n in the string and show the index
print(Find)                  # 5


```

**Example:** Use the function to get more information about the method

```
numbers = [5,2,1,7,4]
numbers.append(20)                      # Inseret number in the End
numbers.insert(1,22)                    # Insert number in index 1
numbers.remove(1)                       # Remove number 4
#numbers.clear()                        # Removes all numbers
numbers.pop()                           # Removes last number in the list
print(numbers)

print(numbers.index(2))                 # Shows the index of number 2
print(2 in numbers)                     # Shows a Boolean Value True or False
print(numbers.count(5))                 # Counts how many 5s there are
print(numbers.sort())                   # Sorts the list (does not show value)
numbers.sort()

print(numbers)                          # Now its prints the sorted list
numbers2 = numbers.copy()               # Copy the list into a new one
```


# Find [Value] in String

**Checks if the substring 'for' is present within the string 'Python for Beginners'.**

> Answer always: True or False

```
course = 'Python for Beginners'     # String
print('for' in course)              # search for 'for' in the variable course
# Output: True
```

# Arithmetic Operators  

**Arithmetic Operators are used to perform mathematical operations like addition, subtraction, multiplication, etc.**

```
+   # Addition
-   # Subtraction
*   # Multiplication
/   # Division
//  # Floor Division   # Rounded to integer Number  -> 10 // 3 = 3
%   # Modulus          # Leftover of the division   -> 10 % 3 (=9) = 1
**  # Exponent         # Zehn hoch drei             ->10 ** 3 = 1000
```

# Augmented Assignment Operator

**When you want to perform an operation and update a variable in a single step.**

```
x = 10

x += 3      # Equivalent to: x = x + 3
x -= 3      # Equivalent to: x = x - 3
x *= 3      # Equivalent to: x = x * 3

print("x after using -=:", x)  
```

# Boolean Expressions -> True or False 

**expressions that evaluate to either True or False**

```
==  # Equal
!=  # Not Equal
>   # Greater Than
<   # Less Than
>=  # Greater Than or Equal To
```

**Example:** Simple Boolean Expression asking: is 10 bigger than 3
```
x = 10
y = 5

print(x < y)        # False
```


# Logical Operators -> True or False Result

**Logical Operators are used to determine whether they are true or false**

```
and         # True if both are True
or          # True if one of them is True
not         # True if the opposite is True
```

**Example:** Using Logical Operators and, or, not
```
price = 15

# Price is bigger than 10 and smaller than 30
print(price > 10 and price < 30)            # True

# Price is bigger than 10 or smaller than 30 
print(price > 10 or price < 30)             # True

# Price is NOT the same as 10
print(not price == 10)                      # True
```

# If Statements

**If Statements are used to check conditions and change the behavior of the program accordingly.**

```
if          # if the condition is True, the code below will be executed
elif        # if the first condition is False, the second condition will be checked
else        # if all conditions are False, the code below will be executed
```

**Example** If Statements with 3 Conditions
```
temperature = 5

if temperature > 30:
    print("It's a hot day")
    print('Drink some water')
elif temperature > 25: # When the first if is not applyed (Temp warmer than 30) This conditions starts (temp warmer than 25)
    print('Its a pleasent day')
elif temperature > 10:
    print('Its quite cold')
else:
    print('Man its cold')

print('done')
```

**Example:** If Statements with Boolean Expressions
```
has_high_income = True
has_high_credit = False

if has_high_income and has_high_credit:
    print(f"Your good to go because your income is: {has_high_income} and your credit limit {has_high_credit}")

elif not has_high_income and has_high_credit:
    print(f'Your income is not enough')

elif has_high_credit == False and has_high_credit == True:
    print(f'Your credit is not enough')

elif has_high_income and not has_high_credit:
    print("Your credit limit is not sufficient.")

else:
    print(f'Both is not enough')
```


# While Loops

**A While loop will go through and do some task until a condition is met.**

**Example:** While i is smaller than 15 do print "*" multiplied with i and add 1 to i 

```
i = 1
while i <= 15:          # While i is smaller than 15 
    print(i * '*')      # Print "*" multiplied with i
    i += 1              # Add 1 to i
print('finish')         # Print finish when the loop is done
```


Example 2 While **True** do following until **break**
```
while True:
    user_input = str(input("> ")).upper()

    if user_input == "HELP":
        print(help_txt)

    elif user_input == "QUIT":
        print("you Quit")
        break

    else:
        print("I don't understand that...")
```


# Break -> Breaks the Loop

**The break command can exit a while loop**

**Example:** Break the loop when the user guess right


```
    if guess_number == secret_number:
        print("You win!")
        break
```

# Lists

**A List is a data structure to store a collection of values.**

**Example:** A List with 5 Numbers
```
numbers = [1, 2, 3, 4, 5]   # List of numbers
numbers.append(6)           # add 6 to the list
```

**Example:** A List with 5 Strings
```
names = ['John', 'Bob', 'Mosh'] # List of names
names[0] = 'Jan'                # Change the first name to Jan

print(names[-1])                # Shows the last name in the list
print(names[0:2])               # Shows the first 2 names in the list
```
# List Methods 

**A Method is a function that belongs to an object**

**Example:** Lists are always in [] not in () would be a tupple
```
numbers = [1,2,3,4,5,]      # List of numbers
numbers.append(6)           # Adds 6 to the list
numbers.insert(0, 10 )      # inserts 10 into the first position
numbers.remove(2)           # Removes the number 2

print(10 in numbers)        # Shows it there is a 10 true or false
print(len(numbers))         # Shows how many numbers
numbers.clear()             # clears all the Numbers
```	

# For Loops

**A For loop will go through and do some task for each item in a list, tuble, string.**

> for item in list -> item will be set to a Value of the list and change it every time it runs

**Example:** Simple For loop with a list
```
price = [10, 20, 30]            # List of prices
total = 0                       # Variable for the total

for item in price:              # For loop for i in price
#   total = total + item        # bad way to write it Adds total to the item and saves it in new total
    total += item               # good way to write it Add the item to the total

print(f"Total: {total}")        # Total: 60
```

**Example:** compare **for** and **while loop**
```
numbers = [1,2,3,4,5,6]
for item in numbers:
    print(item)

print('while loop')
i = 0
while i < len(numbers):
    print (numbers [i])
    i += 1
```

# Range Function

**Range is a function that generates a sequence of numbers**

**Example:** Create a list with the range function
```
for number in range(10):        # Starts with 0 and ends with 9
    print(number)

for number in range(1,100):     # Starts with 1 and ends with 100
    print(number)

```

# Tuples (Immutable Lists) ()

**Tuples are immutable lists this means can not be changed -> with () instead of []**

**Example:** a Tuple
```
numbers = (1,2,3)

# tuples are immutable
numbers.append(6)  # AttributeError: 'tuple' object has no attribute 'append'
```

# Index

**Index is the position of an item in a list**

**Example:** Index of a String

```
course = 'Python for Beginners'
#         012345 678 9      # Shows the Index of the String
print (course[:5])          # Shows the first 5 Index -> Pytho

name = 'Jennifer'
#       0123456             # Shows the Index of the String
print(name[1:-1])           # starts from 1 until the last one
```

# Formatted Strings

**Example:**  Formatted Strings with f'{}' and .format() 

> f'{Variable}' is the way to format strings 

```
first = 'Dany'
last =  'Ambuehl'

msg = f'{first} [{last}] is a coder' # prefix the string with a f and than add Values with {}

print(msg)          # Dany [Ambuehl] is a coder
```

**Example:**  String a Letter more than just a line

```
txt = '''

This is a big Text Message 
to you boby
thx '''
```

# Math Module

**You can import a module, like here the math module "import math"**

**Example:** How to use the math module
```
# Import the math module
import math             # Google : python 3 math module to find all functionality of the module

# Use the math module
print(math.ceil(2.9))   # Round up
print(math.floor(2.9))  # Round down

x = 2.9
rounded = round(x)
print(rounded)
```

# Nested Loops

**Example:** A For loop in a For loop prints every value of the matrix
```
matrix = [
    [1,2,3],    # RAW 0
    [4,5,6],    # RAW 1
    [7,8,9]     # RAW 2
#   Nr0,Nr1,Nr2
]

# Nested for loop
for row in matrix:             # For every row in the matrix
    for value in row:          # For every value in the row 
        print(value)           # Print the value
```
# Matrix

**Matrix is typically represented as a two-dimensional array or list of lists**

**Example:** Of a Matrix with 3 RAWs and 3 NRs
```
matrix = [
    [1,2,3],    # RAW 0
    [4,5,6],    # RAW 1
    [7,8,9]     # RAW 2
#   Nr0,Nr1,Nr2
]

matrix[2][1] = 20       # Change the value of the matrix RAW 2, NR 1 = 20
matrix[2]               # Access the RAW 2, 4,5,6

```

# Unpacking 

**Store every value of the list in a separate Variable**

```	
coordinates = (1,2,3)
x = coordinates[0]      # We can store every value of the list in a Variable to work with it afterwards.
y = coordinates[1]
z = coordinates[2]

x,y,z = coordinates     # "Unpack" the coordinates into this 3 variables 
```

# Dictionaries

**A dictionary is a data structure that stores key-value pairs.** 
It's like a list, but instead of indexes, you have keys that can be of any type. but not duplicate

```
costumer = {
    "name": "Dany Ambühl",
    "age" : 30,
    "is verified": True
}
costumer["name"] = "Monika Ambühl"          # Change Key
costumer["birth"] = "1989"                  # Add Key

print(costumer.get("spitzname", "däny"))

print(costumer["name"])
```

If you search for a key that **does not exist**, you will get an **Error**.

```
print(costumer["live"])  -> Error
```

To avoid this, you can use the **get method**. If the key does not exist, you will get **None** return.

```
print(costumer.get("live"))  -> None
```

> None is a special value in Python that represents the absence of a value.

You can also specify a **default value** to return if the key does not exist.

```
print(costumer.get("spitzname", "kein Spitzname"))
```

**Example:** Script to convert numbers into words with for loop and dictionary
```
numbers= {
    "0" : "Zero",
    "1" : "One",
    "2" : "Two",
    "3" : "Three",
    "4" : "Four",
    "5" : "Five",
    "6" : "Six",
    "7" : "Seven",
    "8" : "Eight",
    "9" : "Nine"
}

output = ""
phone = input("Phone: ")                        # Variable für Input

for value in phone:                             # For every i in Input ->
    output += numbers.get(value, "!") + " "     # Add numbers.get (input) , set it to ! when it does not exist and add (+) " " space.
print(output)

private = numbers.get("1", "!")                 # Gets the String 1 of the numberslist and writes a ! if it doesnt exists. 
print(private)
```

