## Assigning Variables

### Number Data Type - Integer
```python
number = 42 
x = 10
```
### Number Data Type - Float
```python
pi = 3.12 
```
### Boolean Data Type
```python
is_raining = False
```
### String Data Type
```python
name = "John Doe" 
```

## Comparators
### Comparator Table
| Description             | Sign |
| ----------------------- | ---- |
| Is equals to            | ==   |
| Is not equals to        | !=   |
| Is greater than         | >    |
| Is greater or equals to | >=   |
| Is lesser than          | <    |
| Is lesser or equals to  | <=   |

### AND Truth Table
| x     | y     | result |
| ----- | ----- | ------ |
| True  | True  | True   |
| True  | False | False  |
| False | True  | False  |
| False | False | False  

### OR Truth Table
| x     | y     | result |
| ----- | ----- | ------ |
| True  | True  | True   |
| True  | False | True   |
| False | True  | True   |
| False | False | False  |

## Branching
### If
```Python
if ( condition ):
	print("Hello")
```
### If-Else
```python
if ( condition ):
	print("Hello")
else:
	print("Goodbye")
```
### If-Elif-Else
```python
if ( condition 1 ):
	print("Hello")
elif ( condition 2 ):
	print("Ola")
elif ( condition 3 ):
	print("Bonjour")
else:
	print("Goodbye")
```

## Loops/Automation
### While Loop - Using Sentinel Variable
```python
sentinel = 0
while ( condition ):
	sentinel = sentinel + 1
```
### While Loop - Non-Deterministic 
```python
user_input = input("Enter something: ")
while ( condition ):
	user_input = input("Enter something: ")
```
### For Loop
```python
for i in range(10):
	print(i)
```
>`range()` function can take in up to three parameters. 

## List
### Declaration
```python
random_list = ["john", 21, 3.14, True]
```
### Accessing List
```python
random_list = ["john", 21, 3.14, True]
name = random_list[0]
print(name)
```

### Iterating with While Loop
```python
random_list = ["john", 21, 3.14, True]

index = 0
while index < len(random_list):
	print(random_list[index])
	index = index + 1
```

### Iterating with For Loop
```python
random_list = ["john", 21, 3.14, True]

for i in random_list:
	print(i)
```