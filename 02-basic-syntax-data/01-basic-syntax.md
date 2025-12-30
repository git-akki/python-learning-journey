Got it 👍
Below is **everything merged into ONE single Markdown file**, **clean**, **complete**, and **ready to paste directly** into `README.md` or `05-python-syntax.md`.

No extra wrappers. No missing sections. No broken formatting.

---

# Python Syntax — Notes & Fundamentals 🐍

This section covers the **core syntax rules of Python**.
Python is designed to be **simple, readable, and strict where it matters**.

These notes focus on **understanding**, not memorizing.

---

## 📌 How to Run Python Code

Python can be executed in **two modes**.

---

### 1️⃣ Interactive Mode

Used for quick testing and experimentation.

```bash
python
>>> print("Hello, World!")
```

* Executes one line at a time
* `>>>` is the Python prompt
* Best for learning & debugging

---

### 2️⃣ Script Mode

Used for real programs.

```python
# test.py
print("Hello, World!")
```

Run with:

```bash
python test.py
```

You can also make a script executable on Linux/macOS using shebang:

```python
#!/usr/bin/python3
print("Hello, World!")
```

```bash
chmod +x test.py
./test.py
```

---

## 🏷️ Python Identifiers (Names)

Identifiers are names used for:

* variables
* functions
* classes
* modules
* objects

### Rules

* Must start with a letter (`A–Z`, `a–z`) or `_`
* Can contain letters, digits, and `_`
* Cannot contain special symbols like `$ @ %`
* Case-sensitive (`name` ≠ `Name`)

### Naming Conventions

* `my_variable` → variables & functions
* `MyClass` → class names
* `_internal_var` → internal/private use
* `__special__` → Python-defined (do not create your own)

---

## 🔒 Python Reserved Words (Keywords)

These words are **reserved** and cannot be used as identifiers.

```text
and, as, assert, break, class, continue,
def, del, elif, else, except, False,
finally, for, from, global, if, import,
in, is, lambda, None, nonlocal, not,
or, pass, raise, return, True, try,
while, with, yield
```

* Keywords are **always lowercase**
* Used by Python internally

---

## 📐 Indentation (Very Important)

Python uses **indentation instead of braces `{}`** to define blocks.

```python
if True:
    print("True")
else:
    print("False")
```

### Rules

* Indentation defines code blocks
* All lines in a block must use the **same spacing**
* Incorrect indentation causes errors

👉 This makes Python readable but strict.

---

## ➿ Multi-Line Statements

### Using backslash (`\`)

```python
total = a + \
        b + \
        c
```

### Using brackets (recommended)

```python
days = [
    "Monday",
    "Tuesday",
    "Wednesday",
    "Thursday"
]
```

Brackets automatically allow line breaks.

---

## 🧵 Strings & Quotes

Python supports:

* `'single quotes'`
* `"double quotes"`
* `'''triple quotes'''` or `"""triple quotes"""`

```python
word = "Hello"

paragraph = """This is a paragraph.
It spans multiple lines.
Triple quotes allow this."""
```

Strings in Python are **Unicode by default**.

---

## 💬 Comments

Comments explain code and are ignored by Python.

### Single-line comment

```python
# This is a comment
```

### Inline comment

```python
name = "Akash"  # user name
```

### Multi-line (doc-style)

```python
"""
This is a
multi-line comment.
"""
```

---

## ⬜ Blank Lines

* Blank lines are ignored by Python
* Improve readability
* Required to terminate multi-line input in interactive mode

---

## ⏸️ Waiting for User Input

Used to pause execution (mostly in scripts):

```python
input("Press Enter to exit")
```

---

## ➕ Multiple Statements on One Line

Allowed, but **not recommended**:

```python
import sys; x = "foo"; print(x)
```

Readable code > short code.

---

## 🧱 Code Blocks (Suites)

A **suite** is a block of statements following headers like
`if`, `while`, `for`, `def`, `class`.

```python
if x > 0:
    print("Positive")
elif x == 0:
    print("Zero")
else:
    print("Negative")
```

### Rules

* Header ends with `:`
* Followed by an indented block

---

## 🖥️ Command Line Arguments (Intro)

Check Python help:

```bash
python -h
```

Run a script:

```bash
python script.py
```

Advanced CLI handling will be covered later (`argparse`, `sys.argv`).

---

## 🧠 Key Takeaways

* Python prioritizes **readability**
* Indentation is part of syntax
* Fewer symbols → clearer structure
* Code blocks are defined by spacing
* Write code for **humans first**

> **Simple code scales better than clever code.**

---

If you want, next we can:

* add **real backend examples**
* connect syntax rules to **FastAPI**
* continue with **Variables, Data Types, or Control Flow**

You’re building **solid fundamentals** — this is the right pace 💪
