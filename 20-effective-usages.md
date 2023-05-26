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
