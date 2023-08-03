# Datatype

All problems about datatype.


## Shallow-copy and Deep-copy


When it comes to deep copy and shallow copy, the differences can be compared based on data types, copy principles, and copy functions. Here is a table in Markdown format that summarizes the differences between deep copy and shallow copy:

|                     | Data Types              | Copy Principle                                                                                                                    | Copy Function                                                          |
| ------------------- | ----------------------- | -------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- |
| Deep Copy           | Mutable and Immutable Data Types   | Create a new object and recursively copy all nested objects of the original object. The new object is completely independent from the original object, and modifications to the copy won't affect the original object. | `copy.deepcopy()`                                                       |
| Shallow Copy        | Mutable Data Types             | Create a new object where a part of it shares the same reference as the original object. Only the first level of the original object is copied, and nested objects are still shared. Modifications to the copy will affect the original object.                   | `copy.copy()`                                                           |
| Immutable Data Types | Not applicable         | Not applicable                                                                                                                    | Not applicable                                                          |
|                     | Strings, Numbers, and other Immutable Objects | Whether it's a deep copy or shallow copy, a new object will be created. However, for immutable objects that cannot be modified, there is no difference between deep copy and shallow copy.                           |                                                                      |

This table provides an overview of the differences between deep copy and shallow copy based on different data types, copy principles, and the use of copy functions. Please note that the mentioned copy functions refer to the `copy` module provided by the Python standard library.

Following is code about this feature:

```Python
import copy

nested_array = [1, 2, 7, [4, 9, 6]]

shallow_copy = copy.copy(nested_array)

deep_copy = copy.deepcopy(nested_array)

# Original array: [1, 2, 7, [4, 9, 6]] 2456116559808
print("Original array:", nested_array, id(nested_array), "\n")
# Shallow copy before modifying: [1, 2, 7, [4, 9, 6]] 140724048356296
print("Shallow copy before modifying:", shallow_copy, id(shallow_copy[3]), "\n")
nested_array[3].append(512)
# Shallow copy after modifying: [1, 2, 7, [4, 9, 6, 512]] 140724048356296 
print("Shallow copy after modifying:", shallow_copy, id(shallow_copy[3]), "\n")
# original array: [1, 2, 7, [4, 9, 6]] 2456116539264 
print("Original array:", deep_copy, id(deep_copy), "\n")
nested_array[3][2] = 1024
# Original array after modifying by deep copying: [1, 2, 7, [4, 9, 1024, 512]] 2456116559808
print("Original array after modifying by deep copying:", nested_array, id(nested_array), "\n")
# original array after deep copying: [1, 2, 7, [4, 9, 6]] 2456116539264 
print("Original array after deep copying:", deep_copy, id(deep_copy), "\n")
```

## small integer caching

Original: [Pylong_Fromlong](https://docs.python.org/zh-cn/3/c-api/long.html#c.PyLong_FromLong)

Quote: [The reason of small integer caching](https://blog.finxter.com/python-small-integer-caching-versus-is/)

The range of caching is from -5 to 256. And the meaning of `is` mean to varaibles which possessed the same memory address. So, for those caching integer number, they are assigned memory address in advance. When we use assignment statement to assign number for variables, those variables will get the same memory address for the same value.

```Python
a, b = 256, 256
for i in range(250, 260):
    if a is not b:
        break
    a += 1
    b += 1
print("start point: ", a, "end point:", b)  # a = b = 257
```

## dict or set

### uniqueness of the key's logic

Althogh there are three object, such as number, complex, and float number, those objects have the same logic value.

```Shell
>>> collections = dict()
>>> temporary = 5 + 0j
>>> collections[5] = "Dog"
>>> collections[5]
'Dog'
>>> collections[5.0] = "Pear"
>>> collections[5.0]
'Pear'
>>> collections[temporary] = "King"
>>> collections[temporary]
'King'
>>> collections[5]
'King'
>>> collections[5.0]
'King'
>>> collections[temporary]
'King'
```


## Operator

all about operator in python.

### walrus operator

version: Python 3.8

PEP No: [572](https://peps.python.org/pep-0572/)

