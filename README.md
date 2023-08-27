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

global x # local scope is changed to global variable

import datetime
print(datetime.datetime.now());

min(5, 10) # 5
max(5, 10) # 10
pow(2, 3) # 8

import math
math.sqrt(4)     # 2
math.ceil(1.4)   # 2
math.floor(1.4)  # 1

import json
json.dumps(x, indent=4, sort_keys=True) # convert to valid json

x = 12
try:
  if x <= 12:
    raise Exception("Exception")
  print("Lorum Ipsum")
except Exception as e:
  print("Something wrong " + str(e))
finally:
  print("Done")

username = input("Enter username:")

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
newSet = set((myTuple))
len(chSet)
for ch in chSet: print(ch) # b a c
chSet.add(d) # existing can't be changed but could add
chSet.update({'a', 'a', 'f'}) # chset -> {'c', 'f', 'b', 'a'} join sets
chSet.remove('b')
chSet.remove('z') # error
chSet.discard('z') # no error if elem not found
chSet.pop()

mySet = chSet.union({'a', 'a', 'f'}) # chset is not mutated
mySet = chSet.intersection(mySet) # a b c -> common in both set
mySet = chSet.symmetric_difference(mySet) # f -> not common in both set
mySet = chSet.difference(mySet) # omit element if exist other set

chSet.clear()
del chSet

### Dict

myDict = {'name': 'John', 'age': 18}
myDict = dict(name = 'John', age = 18) # {'name': 'John', 'age': 18}
len(myDict)
myDict.get('name') / myDict['name'] # John
myDict.keys() # dict_keys(['name', 'age'])
myDict.values() # dict_values(['John', 18])
myDict.items() # dict_items([('name', 'John'), ('age', 18)])
myDict['car'] = 'Supra'
myDict.update({ 'country': 'IN', 'state': '' })
myDict.pop('state')
myDict.popitem() # remove last
del myDict['state']
del myDict
myDict.clear()

if 'name' in myDict: print('Yes')
for key, value in myDict.items(): print(key, value)
for key in myDict.keys(): print(key)
for val in myDict.values(): print(val)
newDict = myDict.copy() / dict(myDict)

myIterVar = ["a", "b", "c"]
myiter = iter(myIterVar);
next(myiter) # a
next(myiter) # b

### Condition & Loops

and/& , or/!, not/~
is, is not 
in, not in

a = 12; b = 23;

if b > a:
  print('Good Evening')
elif b == a:
  print('Good Noon')
elif b < a:
  print('Good Morning')
else:
  print('Error')

print('Day') if b < 18 else print('Night') # shorthand

while a < b: 
  print(a); a+= 1;
  if a > 15: break;

for ch in myList: print(ch)

### Function, Lambda

def myFunction(): print('Hello')
def myFunction_args(*args): print(args[1])              # args arguments like array / rest operator
def myFunction_kwargs(**kwargs): print(kwargs['age'])   # kwargs key value pair like object
myFunction_args("John", "18")                 # 18
myFunction_kwargs(name = "John", age = "18")  # 18

def addTo(y):
  return lambda x: print(y+x) # lambda is anonymous function
add_10 = addTo(10);
print(add_10(9)) # 19

### Class

class Breed:
  def __init__(self, type, an_breed):
    self.an_breed = an_breed

  def breed(self):
    print(self.type + " breed is "+ self.an_breed)

class Animal(Breed):
  
  def __init__(self, type, breed):
    super().__init__(type, breed)   # Inheritance
    self.type = type          # self.type -> public
    # self.__type = type      # self.__type -> protected

  def sound(self):
    if self.type == 'dog':
      print(self.type + " bark")
    elif self.type == 'cat':
      print(self.type + " meow")
    else:
      print(self.type + " unknown sound")

  def diet(an):
    if an.type == 'dog':
      print(an.type + " NonVeg")
    else:
      print(an.type + " unknown diet")

dog = Animal('dog', 'Lab');
dog.sound();
dog.diet();
dog.breed();

```
# Misc
find vs index : if substring is not found then index throw error, find return -1 



