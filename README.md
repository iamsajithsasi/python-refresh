# Codes
`python

sampleString = 'Hello world';
print(sampleString[:3]) # Hel
print(sampleString[2:3]) # l
print(sampleString[2:]) # llo world

print(sampleString.upper())
print(sampleString.lower())
print(sampleString.strip())
print(sampleString.replace('l', 'e')) # Heeeo wored
print(sampleString.split(' ')) # ['Hello', 'world']

sampleString = 'Hello {}'
print(sampleString.format("World")) # Hello World
sampleString = 'Hello {} {}'
print(sampleString.format("My", "World")) # Hello My World

sampleString = 'Hello world';
print(sampleString.find("wo")) # 6: index from 0

print(bool("Hello"))    # True
print(bool(15))         # True
print(bool("Hello"))    # True
print(bool(''))         # False
print(bool(None))       # False
print(bool([]))         # False
print(bool([1,2]))      # True
print(bool({}))         # False

print(isinstance(sampleString, int)) # False
print(isinstance(sampleString, str)) # True

myList = ["apple", "banana", "cherry"]
print(isinstance(myList, list)) # True
print(len(myList)) # 3

"""
List        ordered and changeable.               Allows duplicate.
Tuple       ordered and unchangeable.             Allows duplicate.
Set         unordered, unchangeable*, unindexed.  No duplicate.
Dictionary  ordered** and changeable.             No duplicate.
"""








`

# Python Refresh from basics
```
# Int
num = int(0) # similarly, str, float, bool, list, tuple, dict, set

# String
name = str("Your code has {} bug") 
# .split(","), .slice[2:5], .lower()/caffold(), .upper(), .strip(), .replace("h", "j"), count("a"), find("a") / index("a"), startwith(), endswith()
print(name.format(num))

# Boolean
isReady = bool(False)
isSame = bool(10 is 5)

# list: an array
my_array = [2,3,5]
my_array = list((2,3,5))

# tuple: an array but not editable
my_array_tup = tuple((2,3,5))

# dict: an object
my_dict = {'name': 'John', 'age': 36}
my_dict = dict(name="John", age=36)







# Misc
# find vs index : if substring is not found then index throw error, find return -1 
```
