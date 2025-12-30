# Python Variables — Notes & Fundamentals 🧠🐍

Python variables are **names (labels)** that point to **objects stored in memory**.
They help us store, reuse, and manipulate data in a program.

> In Python, **variables do not store values directly** — they reference objects.

---

## 📦 What is a Variable?

A variable is a **symbolic name** that refers to an object in memory.

```python
age = 18
name = "May"
```

* `age` → refers to integer object `18`
* `name` → refers to string object `"May"`

Python automatically allocates memory when you assign a value.

---

## 🧠 Memory & `id()` Function

Each object in Python lives at a **memory address**.

You can check it using `id()`:

```python
month = "May"
age = 18

print(id(month))
print(id(age))
```

* Same object → same `id`
* Variables are **references**, not boxes

---

## ✨ Creating Variables

No declaration needed.

```python
counter = 100
miles = 1000.5
name = "Zara"
```

* Left side → variable name
* Right side → object/value

---

## 🖨️ Printing Variables

```python
print(counter)
print(miles)
print(name)
```

Output:

```text
100
1000.5
Zara
```

---

## ❌ Deleting Variables

Use `del` to remove a variable reference.

```python
x = 10
del x
print(x)   # Error
```

Error:

```text
NameError: name 'x' is not defined
```

---

## 🔍 Checking Variable Type

Use `type()`:

```python
x = "Zara"
y = 10
z = 10.5

print(type(x))
print(type(y))
print(type(z))
```

Output:

```text
<class 'str'>
<class 'int'>
<class 'float'>
```

---

## 🔄 Type Casting (Explicit Conversion)

```python
x = str(10)     # "10"
y = int("10")   # 10
z = float(10)   # 10.0
```

Used when converting between data types.

---

## 🔤 Case Sensitivity

Python variables are **case-sensitive**:

```python
age = 20
Age = 30

print(age)  # 20
print(Age)  # 30
```

These are **different variables**.

---

## 🔁 Multiple Assignment

### Same value to multiple variables

```python
a = b = c = 10
```

### Different values in one line

```python
a, b, c = 10, 20, 30
```

### Mixed data types

```python
a, b, c = 1, 2, "Zara"
```

---

## 🏷️ Variable Naming Rules

### Rules

* Start with letter or `_`
* Cannot start with a number
* Only letters, numbers, `_`
* No special symbols (`$ % -`)
* Keywords not allowed

### Valid

```python
count = 10
_name = "Alex"
age2 = 25
salary_amount = 50000
```

### Invalid

```python
1count = 10
total-sum = 100
$price = 50
```

---

## 🧭 Naming Conventions

* **Snake case (recommended)**
  `price_per_litre`

* Camel case
  `pricePerLitre`

* Pascal case
  `PricePerLitre`

---

## 📐 Using Variables in Programs

```python
width = 10
height = 20

area = width * height
perimeter = 2 * (width + height)

print("Area =", area)
print("Perimeter =", perimeter)
```

---

## 🧩 Local Variables

Defined **inside a function**
Accessible **only inside that function**

```python
def add(x, y):
    result = x + y
    return result

print(add(5, 10))
```

---

## 🌍 Global Variables

Defined **outside functions**
Accessible everywhere

```python
x = 5
y = 10

def total():
    return x + y

print(total())
```

---

## 🔒 Constants in Python

Python has **no true constants**, but convention is:

```python
PI_VALUE = 3.14
MAX_USERS = 100
```

This is called **SCREAMING_SNAKE_CASE**.

---

## 🆚 Python vs C/C++ Variables (Key Difference)

### C/C++

* Variable = memory location
* `a = 10`, `b = 10` → different memory

### Python

* Variable = reference to object
* Multiple variables can point to same object

```python
a = b = 10
print(a is b)   # True
```

Python automatically removes unused objects via **garbage collection**.

---

## 🧠 Key Takeaways

* Variables are **references**, not containers
* Python handles memory automatically
* No declaration needed
* Types are dynamic
* Naming matters for readability
* Python favors simplicity & clarity

> **Understand references, and Python becomes much clearer.**
