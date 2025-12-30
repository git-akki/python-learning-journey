Python Data Types — Core Concepts & Notes 🧠🐍

In Python, everything is an object.
Data types are actually classes, and variables are references to objects.

Python is dynamically typed, meaning:

The data type is decided at runtime, not beforehand.

📦 What Are Data Types?

Data types define:

What kind of data is stored

What operations are allowed on it

You can check a data type using:

type(value)

🗂️ Built-in Data Types in Python
🔢 Numeric Types

int → Whole numbers

float → Decimal numbers

complex → Numbers with imaginary part (j)

bool → True / False

a = 10
b = 3.14
c = 5 + 6j
d = True

🧵 String Type (str)

Sequence of Unicode characters

Immutable (cannot be changed)

text = "Hello World"
print(text[0])      # H
print(text[2:5])    # llo
print(text * 2)     # Repetition
print(text + "!")   # Concatenation


Quotes supported:

'single'

"double"

'''triple''' (multi-line)

🔁 Sequence Data Types
📋 List (list)

Ordered

Mutable (can change)

Can hold mixed data types

lst = [1, "Python", 3.11]
lst[1] = "AI"

📦 Tuple (tuple)

Ordered

Immutable

Read-only list

tup = (1, "Python", 3.11)


⚠️ Cannot modify tuple elements.

🔢 Range (range)

Generates a sequence of numbers

Commonly used in loops

for i in range(1, 5, 2):
    print(i)

🧬 Binary Data Types

Used for files, images, network data.

bytes

Immutable

b = b"Hello"

bytearray

Mutable

ba = bytearray(b"Hello")
ba[0] = 72

memoryview

View into memory (no copy)

data = bytearray(b"Hello")
view = memoryview(data)

🗝️ Dictionary (dict)

Key–value pairs

Unordered

Mutable

user = {"name": "Akash", "age": 21}
print(user["name"])


Keys must be immutable (int, str, tuple).

🔢 Set Types
set

Unordered

No duplicates

Mutable

skills = {"Python", "AI", "Backend"}

frozenset

Immutable set

✅ Boolean Type (bool)

Represents truth values.

True   # 1
False  # 0


Falsy values:

0

None

""

[], (), {}

🚫 None Type (NoneType)

Represents absence of value.

x = None
print(type(x))  # NoneType

🔍 Getting Data Type
type(123)        # int
type(3.14)       # float
type("Hello")    # str
type([1, 2, 3])  # list

🔄 Dynamic Typing in Python

Same variable → different types at different times.

x = 10
x = "Hello"


✔ No error
✔ Type decided at runtime

🧱 Primitive vs Non-Primitive
Primitive Types

int

float

bool

str

Non-Primitive Types

list

tuple

dict

set

🔁 Type Conversion (Casting)

Convert using type functions:

int("3")     # 3
float("3.5") # 3.5
str(10)      # "10"


Common conversion functions:

int()

float()

str()

list()

tuple()

set()

dict()

🧠 Key Takeaways

Python is object-based

Variables are references, not boxes

Lists → mutable, Tuples → immutable

Dictionaries use keys, not indexes

Sets remove duplicates automatically

Data types change dynamically

Readability > rigidity

Understand data types deeply — they shape how you design programs.