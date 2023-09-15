Python Cheat Sheet
==================

### Data Types

| Type  | Brackets  | Example           | Description               | Methods                                               |   Notes                                               |
| ----  | -------   | -------           | -----------               | -------                                               |   -----                                               |
| int   |           | 1                 | Integer                   |                                                       |                                                       |  
| float | .         | 1.0               | Floating point number     |                                                       |
| str   | "" ''     | "Hello"           | String                    | .upper() .lower() .title() .replace                   |
| bool  |           | True              | Boolean                   |
| list  | []        | [1, 2, 3]         | List of values            | .append() .insert() .remove() .pop() .sort() .index() |
| tuple | ()        | (1, 2, 3)         | Immutable list of values  | .index() .count()                                     |
| dict  | {}        | {"a": 1, "b": 2}  | key-value pairs           | .keys() .values() .items() .pop() .get()              | can not be changed but can be added or remove   Ture and 1 == Same  |
| set   | {}        | {1, 2, 3}         | collection unique values  |


### Functions

```python
len() # length of a string or list
type() # type of a variable
print() # print to console
input() # get input from user
range() # generate a range of numbers
enumerate() # get index and value of a list
zip() # combine two lists
format() # format a string
sum()   # sum of a list
round() # round a number
```
# String

```python
str = "Hello World"                           # Create a string
str[0]                                        # Get first character                          # H
str[-1]                                       # Get last character                           # d
str[0:5]                                      # Get first 5 characters                       # Hello
str[6:]                                       # Get characters from 6 to end                 # World
str[-5:]                                      # Get last 5 characters                        # World
str[0:5:2]                                    # Get every second character from 0 to 5       # Hlo
str.upper()                                   # Convert to upper case                        # HELLO WORLD
str.lower()                                   # Convert to lower case                        # hello world
str.title()                                   # Convert to title case                        # Hello World
str.replace("H", "J")                         # Replace characters                           # Jello World
str.split(" ")                                # Split string into list                       # ["Hello", "World"]
str.strip()                                   # Remove whitespace from beginning and end     # Hello World
str.startswith("H")                           # Check if string starts with H                # True
str.endswith("rld")                           # Check if string ends with d                  # True
str.find("World")                             # Find index of first occurrence of World      # 6
str.count("l")                                # Count number of occurrences of l             # 3
str.len()                                     # Get length of string                         # 11
str.isalpha()                                 # Check if string is alphabetic                # False
str.isnumeric()                               # Check if string is numeric                   # False
'Hello' in str                                # Check if string contains Hello               # True
'Hello' not in str                            # Check if string does not contain Hello       # False
str + ":" + str                               # Concatenate strings                          # Hello World:Hello World
str * 2                                       # Repeat string                                # Hello WorldHello World
f'Fuck {str}  !'                              # Formate the String                           # Fuck Hello World !
```

## Dictionary

```python
dict = {"a": 1, "b": 2, "c": 3}              # Create a dictionary              
dict["a"]                                    # Get value of key                 # 1
dict.get("a")                                # Get value of key                 # 1
dict["d"] = 4                                # Add new key-value pair           # {"a": 1, "b": 2, "c": 3, "d": 4}
dic.keys()                                   # Get all keys                     # ["a", "b", "c", "d", "e"]
dict.update({"d": 4, "e": 5})                # Add new key-value pairs          # {"a": 1, "b": 2, "c": 3, "d": 4, "e": 5}
dict.pop("a")                                # Remove key-value pair            # {"b": 2, "c": 3, "d": 4, "e": 5}
dict.items()                                 # Get key-value pairs              # [("a", 1), ("b", 2), ("c", 3), ("d", 4), ("e", 5)]

##### Loop ######
dict = {"a": 1, "b": 2, "c": 3}              # Create a dictionary
for value in dict.keys():                    # dict_keys(['a', 'b', 'c'])
    print(dict.get(value))                   # 1 2 3  # or with print(dict[value]) 
```

## Set


```python
set = {1, 2, 3, 'banana'}                     # Create a set
set = {1, 2, 5, 'Tree'}                       # Create a set
print("banana" in set)                        # Check if value is in set                    # True
len(set)                                      # Get length of set                           # 4
set.add("orange")                             # Add value to set                            # {1, 2, 3, 'banana', 'orange'}
set.update(["orange", "mango", "grapes"])     # Add multiple values to set                  # {1, 2, 3, 'banana', 'orange', 'mango', 'grapes'}
set.remove("banana")                          # Remove value from set                       # {1, 2, 3, 'orange', 'mango', 'grapes'}           # If value does not exist, remove() will raise an error
set.discard("banana")                         # Remove value from set                       # {1, 2, 3, 'orange', 'mango', 'grapes'}           # If value does not exist, discard() will NOT raise an error
set.pop()                                     # Remove random value from set                # {2, 3, 'orange', 'mango', 'grapes'}
set3 = set.union(set2) # set3 = set | set2    # Return a set containing the union of sets   # {1, 2, 3, 'banana', 'orange', 'mango', 'grapes', 'apple', 'cherry'}       
set.intersection(set2)                        # contains the items that exist in both set   # {1, 2,}
set.difference(set2)                          # contains the items that only exist in set   # {3, 'banana'}
set.isdisjoint(set2)                          # Return True if no items in set is present in set2
set.issubset(set2)                            # Return True if all items set are present in set2
set.issuperset(set2)                          # Return True if all items set2 are present in set

##### Loop ######
set = {1, 2, 3, 'banana'}                     # Create a set
for value in set:                             # Loop through set
    print(value)                              # 1 2 3 banana
```