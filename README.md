# all-about-python
a repo where I note cool and interesting that I learn about python

## Table of Content:
### 1: Keywords
### 2: Built in functions
### 3: Mutation

## Key words
### yield
https://www.geeksforgeeks.org/use-yield-keyword-instead-return-keyword-python/

`yield` creates a sequence of values.  We can use `yield` when we want to iterate over a sequence but don't want to store the sequence in memory.
Each yield statement acts as a value of the sequence.  Meanwhile, `return` sends a value back to its caller.
A function that counts to 5 with `yield`
```
def countFive():
	yield 1
	yield 2
	yield 3
	yield 4
	yield 5

# driver code
for c in countFive():
	print(c)

```
```
1
2
3
4
5
```
A function that counts to ***n*** depends on driver code
```
def count():
	count = 1
	while True:
		yield count
		count += 1

# driver code
for num in count():
	if num > 6:
		break
	print(num)
```
```
1
2
3
4
5
6
```
## Built-in functions
### `all`:
return true if all the elements of a given iterable (dictionary, list, tuple, set, etc) are `True` or empty else return `False`.

- example: 
```
>>> ex1 = [4, 5, 1]
>>> print(all(ex1))
True
>>> ex2 = [0, 0, False]
>>> print(all(ex2))
False
```

leetcode problem uses all as part of the solution.
[Backspace String Compare](https://leetcode.com/problems/backspace-string-compare/)

### `intertools`
functions creating iterators for efficient looping

### `sort by elements in python tuples`
```
sorted([('abc', 121),('abc', 231),('abc', 148), ('abc',221)],key=lambda x: x[1], reverse=True)
```

To break tie
```
tuples.sort(key=lambda x: (x[0], x[1]))
```

## Mutation
- list and dictionary are mutable
- string is not mutable

mutable = it can change the original version after you pass it into another function

## Creating virtual machine
to create virtual env:

1: installing
	python3 -m pip install --user virtualenv
	
2: python3 -m venv env

3: source env/bin/activate
