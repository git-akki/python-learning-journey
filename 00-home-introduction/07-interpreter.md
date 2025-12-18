# Python Interpreter

Python is an **interpreter-based language**, which means Python code is executed **step by step** by a program called the *Python interpreter*.

You don’t run Python code directly on the computer —
the interpreter runs it **for you**.

---

## Where Is the Python Interpreter?
- On **Linux / macOS**, Python is usually available as `python` or `python3`
- On **Windows**, Python runs using `python.exe`

You normally don’t need to know the exact file location —  
what matters is that the `python` command works in your terminal.

---

## How the Python Interpreter Works (Simple View)

When you run Python code, this is what happens internally:

1. Python reads your code line by line
2. It checks whether the syntax is valid  
   *(syntax = rules of writing code)*
3. The code is converted into **bytecode**  
   *(bytecode = an internal, simplified form of code)*
4. The **Python Virtual Machine (PVM)** executes that bytecode

You don’t see these steps — Python handles them automatically.

---

## Two Ways to Use the Python Interpreter

Python can be used in **two main modes**.

---

## 1️⃣ Interactive Mode (REPL)

REPL stands for:
**Read → Evaluate → Print → Loop**

You start it by running:
```bash
python
