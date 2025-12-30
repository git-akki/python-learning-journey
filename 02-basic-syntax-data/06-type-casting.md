# Python Type Casting — Notes & Fundamentals 🔄🐍

Type casting means converting a value from one data type to another.

Python supports two kinds of type casting:

Implicit (automatic)

Explicit (manual)

🔄 Why Type Casting Is Needed

Sometimes:

User input comes as a string

You need it as a number

Or you want to convert numbers to text

Python gives built-in tools to do this safely.

1️⃣ Implicit Type Casting (Automatic)

Python automatically converts compatible types without data loss.

⚠️ Python is strongly typed:

It does NOT convert unrelated types automatically

Example: "10" + 5 ❌ (Error)

✔ Allowed Implicit Conversion

int → float

a = 10      # int
b = 10.5    # float

c = a + b   # int → float
print(c)    # 20.5

Boolean Conversion

True → 1

False → 0

a = True
b = 10.5
print(a + b)  # 11.5


🧠 Rule:

Smaller data type is upgraded to bigger one to avoid data loss.

2️⃣ Explicit Type Casting (Manual)

You explicitly tell Python what type you want.

Common casting functions:

int()

float()

str()

🔢 int() — Convert to Integer
Valid Conversions
int(10)        # 10
int(10.5)      # 10
int(True)      # 1
int("100")     # 100

Invalid Conversions ❌
int("10.5")        # ValueError
int("Hello")       # ValueError

Base Conversion (Advanced but Important)
int("110011", 2)   # Binary → 51
int("20", 8)       # Octal → 16
int("2A9", 16)     # Hex → 681

🔢 float() — Convert to Float
float(10)          # 10.0
float("9.99")      # 9.99
float("1.2e3")     # 1200.0


❌ Invalid:

float("1,234.5")   # ValueError (comma not allowed)

🧵 str() — Convert to String

Converts any object to readable string.

str(10)            # "10"
str(3.14)          # "3.14"
str(True)          # "True"
str([1, 2, 3])     # "[1, 2, 3]"
str({"a": 1})      # "{'a': 1}"


🧠 Expression is evaluated first:

str(2 / 5)         # "0.4"

🔁 Converting Sequence Types
String → List / Tuple
list("Hello")      # ['H', 'e', 'l', 'l', 'o']
tuple("Hello")     # ('H', 'e', 'l', 'l', 'o')

List ↔ Tuple
tuple([1, 2, 3])   # (1, 2, 3)
list((1, 2, 3))    # [1, 2, 3]

List / Tuple → String
str([1, 2, 3])     # "[1, 2, 3]"
str((1, 2, 3))     # "(1, 2, 3)"

🧰 Common Type Conversion Functions
Function	Purpose
int()	Convert to integer
float()	Convert to float
str()	Convert to string
complex()	Create complex number
list()	Convert to list
tuple()	Convert to tuple
set()	Convert to set
dict()	Create dictionary
repr()	Debug-style string
eval()	Execute string as code ⚠️
chr()	Int → character
ord()	Character → int
hex()	Int → hex
oct()	Int → octal

⚠️ eval() is dangerous — avoid unless necessary.

🧠 Key Takeaways

Python avoids unsafe automatic conversions

Implicit casting is limited and safe

Explicit casting gives full control

Casting always returns a new object

Data loss can happen (float → int)

Strong typing prevents silent bugs

Type casting is not magic — it’s controlled transformation.