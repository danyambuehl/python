Python Cheat Sheet
==================

### Data Types

| Type  | Brackets  | Example           | Description               | Methods                                               |
| ----  | -------   | -------           | -----------               | -------                                               |
| int   |           | 1                 | Integer                   | 
| float | .         | 1.0               | Floating point number     |                                                       |
| str   | "" ''     | "Hello"           | String                    | .upper() .lower() .title() .replace                   |
| bool  |           | True              | Boolean                   |
| list  | []        | [1, 2, 3]         | List of values            | .append() .insert() .remove() .pop() .sort() .index() |
| tuple | ()        | (1, 2, 3)         | Immutable list of values  | .index() .count()                                     |
| dict  | {}        | {"a": 1, "b": 2}  | key-value pairs           | .keys() .values() .items() .pop() .get()              |
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
```

```
dict = {"a": 1, "b": 2, "c": 3}              # Create a dictionary
for value in dict.keys():                    # dict_keys(['a', 'b', 'c'])
    print(dict.get(value))                   # 1 2 3  # or with print(dict[value]) 
```