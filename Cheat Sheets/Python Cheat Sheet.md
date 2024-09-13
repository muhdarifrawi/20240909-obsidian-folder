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
also_name = 'Jane Doe'
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

## String
### Selecting character via index
```Python
simple_quote = "This is just a simple quote."

print(simple_quote[13])
```
### String Iteration
```Python
simple_quote = "This is just a simple quote."

```
### String Slicing
```Python
simple_quote = "This is just a simple quote."

sliced_1 = simple_quote[0:9] # can also be writen as [:9]
sliced_2 = simple_quote[3:9]
sliced_3 = simple_quote[3:]
sliced_4 = simple_quote[3:18:2]
sliced_5 = simple_quote[3::2]
sliced_6 = simple_quote[::-1]
```

### String Escape Sequences
```python

```

### String Methods
#### Check String Length

#### Stripping excess spaces on left and right



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

for j in range(5,20):
	print(j)

for k in range(2,30,2):
	print(k)
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

### Iterating search
```Python
random_numbers = [2,4,6,8,10,12]

if 6 in random_numbers:
	print("found")
else:
	print("not found")
```

### List Methods
#### Checking List Length
```Python
number_seq = [1,3,5,7,9,12,15]

string_length = len(number_seq)
```
#### Adding into List
```Python
number_seq = [1,3,5,7,9,12,15]

number_seq.append(42)
```

#### Removing from List
```Python
number_seq = [1,3,5,7,9,12,15]

number_seq.remove(12)
```