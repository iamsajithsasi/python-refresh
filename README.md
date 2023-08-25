# Codes
```
sampleString = 'Hello world';
sampleString[:3]   # Hel
sampleString[2:3]  # l
sampleString[2:]   # llo world

sampleString.upper()
sampleString.lower()
sampleString.strip()
sampleString.replace('l', 'e')   # Heeeo wored
sampleString.split(' ')          # ['Hello', 'world']

sampleString = 'Hello {}'
sampleString.format("World")       # Hello World
sampleString = 'Hello {} {}'
sampleString.format("My", "World") # Hello My World

sampleString = 'Hello world';
sampleString.find("wo") # 6: index from 0

bool("Hello")    # True
bool(15)         # True
bool("Hello")    # True
bool('')         # False
bool(None)       # False
bool([])         # False
bool([1,2])      # True
bool({})         # False
isinstance(sampleString, int) # False
isinstance(sampleString, str) # True
isinstance([], list)          # True

"""
List    ordered and changeable.               Allows duplicate.
Tuple   ordered and unchangeable.             Allows duplicate.
Set     unordered, unchangeable*, unindexed.  No duplicate.
Dict    ordered** and changeable.             No duplicate.
"""

### List

myList = ["a", "b", "c"];
myList = list(("a", "b", "a", "d"))   # ['a', 'b', 'a', 'd']
len(myList)                           # 4
myList[2:3]                           # ['a']
myList[-3]                            # b
# myList[10]                          # list index out of range
"a" in myList                         # True

myList[2] = "c"              # ['a', 'b', 'c', 'd']
myList.insert(2, "insert")   # ['a', 'b', 'insert', 'c', 'd']
myList.remove("insert")      # ['a', 'b', 'c', 'd']
myList.append("e")           # ['a', 'b', 'c', 'd', 'e']

myList.extend(['a', 'f']) # ['a', 'b', 'c', 'd', 'e', 'a', 'f']
myList.pop(5)             # ['a', 'b', 'c', 'd', 'e', 'f']
myList.pop()              # ['a', 'b', 'c', 'd', 'e']

newList = myList.copy()
newList = list(myList)

for ch in myList: print(ch)                   # a b c d e
for ch_idx in range(len(myList)): print(ch)   # 0 1 2 3 4

newList = [ch for ch in myList]                          # ['a', 'b', 'c', 'd', 'e']
newList = [ch for ch in myList if ch != 'e']             # ['a', 'b', 'c', 'd']
newList = [ch  if ch == 'e' else '2' for ch in myList]   # ['2', '2', '2', '2', 'e']
newList = [ch  if ch != 'e' else '2'for ch in myList]    # ['a', 'b', 'c', 'd', '2']

myList.sort() # abc 123
myList.sort(reverse=True)
myList.sort(key=sortFn) 
myList.sort(key = str.lower) # sort uppercase as lowercase

myList.extend(newList)
myList + newList

myList.clear() # []
del myList

### Tuple
myTuple = ('a', 'b', 'c')         # ('a', 'b', 'c')
myTuple = tuple(('a', 'b', 'c'))  # ('a', 'b', 'c')
len(myTuple) # 3
myList = list(myTuple);
(a, *b) = myTuple # a -> a ; b -> [b, c]
myTuple = aTuple + bTuple

### sets
chSet = {'a', 'b', 'c'}
set((myTuple))
```

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
