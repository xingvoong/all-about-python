# all-about-python
a repo where I note cool and interesting that I learn about python


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
