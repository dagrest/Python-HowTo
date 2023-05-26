# Unpack TUPLE + unpack TUPLE with *

### Unpack tuple to initialize several variables:  
```python
person = ['james', 25, 'secret service']
name, age, occupation = person
# name='james, age=25, occupation='secret service'
```  
  
### Add * before variable to unpack all other values into this variable
```python
programming_languages = ['C', 'C++', 'C#', 'Java', 'Pyhton', 'Go']
first, second, *others = programming_languages
# first='C', second='C++'
# others = ['C#', 'Java', 'Pyhton', 'Go']
```
  
### List generator | Dictionary/Set genarator
```python
# Generate list in one line

mylist = [expression for i in iterable if condition]

mylist1 = [i for i in range(1,4)]              # [1,2,3]

mylist2 = [i*2 for i in range(1,4)]            # [2,4,6]

mylist3 = [i**2 for i in range(1,4)]           # [1,4,9]

mylist4 = [i for i in range(1,4) if i%2==1]    # [1,3] - even numbers
```

```python
# Same for Set and Dictionary

set1 = {i for i in range(1,4)}          # {1,2,3}

d1 = {i:i**2 for i in range(1,4)}       # {1:1, 2:4, 3:9}
```
  
### Ternary opearator
```python
score = 57
if score > 90:
  grade = 'A*'
elif score > 50:
  grade = 'pass'
else:
  grade = 'fail'

# grade = 'pass'

# Regualr block: if-elif-else

score = 57
grade = 'A*' if score>90 else 'pass' if score>50 else 'fail'

# grade = 'pass'
```
  
### 'Magic' methods in Python classes
```python
class Dog():
  def __init__(self, name, age):
    self.name = name
    self.age = age

  def __str__(self):
    return f'Dog(name={self.name}, age={self.age})'

  def __gt__(self, otherDog):
    return self.age > otherDog.age
    
    
# __str__ defines output, when str(dog) called, happens when the Dog objects are prined
dog = Dog('rocky', 4)
print(dog)    # Dog(name=rocky, age=4)


# __gt__ defines actions, when we are going to compare two dogs with '>' operator
dog1 = Dog('rocky', 4)
dog2 = Dog('fifi', 2)
print(dog1 > dog2)      # True
```



```python
```
