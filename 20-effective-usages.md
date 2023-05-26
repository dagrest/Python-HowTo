# Unpack TUPLE + unpack TUPLE with *

### Unpack tuple to initialize several variables:  
```python
person = ['james', 25, 'male']
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

```python
```
