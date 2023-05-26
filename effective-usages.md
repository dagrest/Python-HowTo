# 1. Unpack TUPLE + unpack TUPLE with *

* ### Unpack tuple to initialize several variables:  
```python
person = ['james', 25, 'secret service']
name, age, occupation = person
# name='james, age=25, occupation='secret service'
```  
  
* ### Add * before variable to unpack all other values into this variable
```python
programming_languages = ['C', 'C++', 'C#', 'Java', 'Pyhton', 'Go']
first, second, *others = programming_languages
# first='C', second='C++'
# others = ['C#', 'Java', 'Pyhton', 'Go']
```
  
# 2. List generator | Dictionary/Set genarator

* ### Generate list in one line
```python
mylist = [expression for i in iterable if condition]

mylist1 = [i for i in range(1,4)]              # [1,2,3]

mylist2 = [i*2 for i in range(1,4)]            # [2,4,6]

mylist3 = [i**2 for i in range(1,4)]           # [1,4,9]

mylist4 = [i for i in range(1,4) if i%2==1]    # [1,3] - even numbers
```

* ### Same for Set and Dictionary
```python
set1 = {i for i in range(1,4)}          # {1,2,3}

d1 = {i:i**2 for i in range(1,4)}       # {1:1, 2:4, 3:9}
```
  
# 3. Ternary opearator

* ### Regualr block: if-elif-else
```python
score = 57
if score > 90:
  grade = 'A*'
elif score > 50:
  grade = 'pass'
else:
  grade = 'fail'

# grade = 'pass'
```
* ### if-elif-else in one line using ternary operator
```python
score = 57
grade = 'A*' if score>90 else 'pass' if score>50 else 'fail'

# grade = 'pass'
```
  
# 4. 'Magic' methods in Python classes
```python
class Dog():
  def __init__(self, name, age):
    self.name = name
    self.age = age

  def __str__(self):
    return f'Dog(name={self.name}, age={self.age})'

  def __gt__(self, otherDog):
    return self.age > otherDog.age
```    
   
* ### `__str__` defines output, when str(dog) called, happens when the Dog objects are prined
```python
dog = Dog('rocky', 4)
print(dog)    # Dog(name=rocky, age=4)
```

* ### `__gt__` defines actions, when we are going to compare two dogs with '>' operator
```python
dog1 = Dog('rocky', 4)
dog2 = Dog('fifi', 2)
print(dog1 > dog2)      # True
```
  
# 5. `**args & **kwargs`

* ### `*args` allows to functions receive any number of values, that will be stored in args
```python
def test(a, b, *args):
  print(f'{a=} {b=} {args=}')

test(1,2,3,4,5)  # a=1 b=2 args=(3,4,5)
```
* ### `**kwargs` allows to functions receive any number of key-values parameters, that will be stored in kwargs
```python
def test(a, b, **kwargs):
  print(f'{a=} {b=} {kwargs=}')

test(a=1, b=2, c=3, d=4)    # a=1 b=2 kwargs={'c': 3, 'd': 4}
```

# 6. Work with several .py files
How to import function from another file
* ### helper.py file
```python
def test():
  print('test is called')
```
* ### main.py file
```python
from helper import test
test()    # test is called
```

# 7. `if __name__ == ‘__main__’`
Run specified code (`if __name__ == ‘__main__’`) only if the file containing this `if` statement was run directly
* ### helper.py file
```python
# helper.py
def test123():
  print('test123 is called')

if __name__ == '__main__':
  # this line only runs if we run helper.py DIRECTLY
  print('print statement from helper.py')
```
* ### main.py file
```python
# main.py
from helper import *

test123()    # test123 is called
```

# 8. True | False values
* ### 0, if falsy, and evaluated as False
```python
if 0: print('this wont print')
```
* ### non-null values evaluated as True
```python
if 1: print('this prints')
if 2: print('this prints')
if 100: print('this prints')
if -1: print('this prints')
if 3.14: print('this prints')
```
* ### empty sequences are falsy and evaluated as False
```python
if '': print('this wont print')
if []: print('this wont print')
if {}: print('this wont print')
if set(): print('this wont print')
```
* ### non-empty sequences are truthy and evaluated as True
```python
if 'a': print('this prints')
if [1]: print('this prints')
if {2:3}: print('this prints')
if {1,2}: print('this prints')
```
* ### None is flasy and evaluated as False
```python
obj = None
if obj: print('this wont print')
```
* ### object are truthy and evaluated as True
```python
obj = Dog()
if obj: print('this prints')
```


```python
```
