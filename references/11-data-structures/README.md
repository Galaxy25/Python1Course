# Data Stuctures

Data structures are important in organizing larger pools of data unlike variables. The different data structures in Python have different benefits and drawbacks depending on its use case.

## `list`

Lists are *ordered*, *changeable*, and *allows duplicates*.

Lists are created with `[]` or can be converted with `list()` if it is an iterable object

```python3
list1 = [1, 2, 3]
list2 = list("hello world")
list3 = list((1, 2, 3))
print(list1)
print(list2)
print(list3)
```

```
[1, 2, 3]
['h', 'e', 'l', 'l', 'o', ' ', 'w', 'o', 'r', 'l', 'd']
[1, 2, 3]
```

New values can be added using `append()`. For lists, `extend()` can be used for combining lists and other data structures. `pop()` removes items from the list using the index. Values being added and removed makes lists *changeable*. Multiple equivalent values can be stored in a list.

```python3
numbers = [1,2,3]
numbers.append(4)
print(numbers)
numbers.extend([5,6,7])
print(numbers)
numbers.pop(0)
print(numbers)
```

```
[1, 2, 3, 4]
[1, 2, 3, 4, 5, 6, 7]
[2, 3, 4, 5, 6, 7]
```

Specific values can be accessed using its index. Index starts at 0 and continues to the end of the list. List's index causes it to be *ordered* since values can before and after different values.

```python3
letters = ["a", "b", "c"]
for i in range(len(letters)):
    print(i)
    print(letters[i])
```

```
0
a
1
b
2
c
```

Items can be checked using `in`.

```python3
number = [1, 2, 3]
if 1 in number:
    print(True)
```

```
True
```

Lists are useful tools for storing values in a set order and allows new values to be added during its runtime. The drawbacks of using a list is increasing runtime when finding values and making changes as it increases it size.

## `tuple`

Tuples are *ordered*, *unchangeable*, *allow duplicates*.

Tuples are similar to lists. The main difference is values cannot be added, removed or changed. Tuples can be created using `()` or can be converted with `tuple()`

```python3
number = (1, 2, 3)
number2 = tuple([1, 2, 3])
```

Tuples are useful when when you don't want an index object to be changeable. For example

```python3
id = ("Nathan St. John", 67437)
```

## `set`

Sets are *unordered*, *changeable* but items within it cannot be changed, and *doesn't allow duplicates*

Sets are created using `{}` if it isn't empty and `set()` can be used to convert iterable objects.

```python3
number1 = set([1, 2, 3, 3, 3, 3])
number2 = {5,4,3}
```

When a empty `{}` is used. The compiler recognizes it as a dictionary because they use the same syntax.

```python3
set1 = {}
print(type(set1))
```

```
<class 'dict'>
```
Values can be added to set using `add()`. Values already in the set are ignored since it *doesn't allow duplicates*

```python3
letters = set("word")
letters.add("a")
print(letters)
letters.add("w")
print(letters)
```

```
{'o', 'a', 'd', 'r', 'w'}
{'o', 'a', 'd', 'r', 'w'}
```

Values can be removed using `remove()`. It throws an error if the value isn't in the set.

```python3
letters = set("word")
letters.remove("w")
print(letters)
letters.remove("w")
```

```
{'o', 'r', 'd'}
KeyError: 'w'
```

Items can be checked for by using `in`.

```
letters = set("word")
if "o" in letters:
    letters.remove("o")
if "a" in letters:
    letters.remove("a")
print(letters)
```

```
{'r', 'w', 'd'}
```

## `dict`