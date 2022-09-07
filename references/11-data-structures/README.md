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

New values can be added using `append()`. For lists `extend()` can be used for combining lists and other data structures. `pop()` removes items from the list using the index. Values being added and removed makes lists *changeable*. The List is also seen with duplicates without throwing any errors.

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
a
1
b
2
c
```

Items can be checked using `in`.

```
number = [1, 2, 3]
if 1 in number:
    print(True)
```

```
True
```

Lists are useful tools for storing values that need to be ordered and values are planned to be added during the program's runtime. The drawbacks of using a List is increasing runtime when finding values and making changes as it increases it size.

## `tuple`

Tuples are *ordered*, *unchangeable*, *allow duplicates*.

Tuples are similar to Lists. The main difference is values cannot be added, removed or changed. Tuples can be created using `()` or can be converted with `tuple()`

```python3
number = (1, 2, 3)
number2 = tuple([1, 2, 3])
```

Tuples are useful when when you don't want an index object to be changeable. For example

```python3
id = ("Nathan St. John", 67437)
```

## `set`

Sets are *unordered*, *changeable* but items within cannot be changed, and *doesn't allow duplicates*

## `dict`