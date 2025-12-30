# Python Private Variables & Encapsulation 🔐🐍

Python is an object-oriented programming language.
One of the core OOP principles it follows is Encapsulation.

Encapsulation means:

Hide internal data and expose only what is necessary.

🧠 What Are Private Variables?

Private variables are variables that are meant to be accessed only inside a class.

Direct access from outside the class is restricted

Helps protect data from accidental misuse

Access is usually provided via methods (getters / setters)

⚠️ Python does not enforce strict privacy like Java or C++
Instead, it follows convention + name mangling

🏷️ Public vs Protected vs Private (Concept)
Type	Meaning	Who Can Access
Public	Open data	Anywhere
Protected (_var)	Internal use	Class + subclasses
Private (__var)	Hidden data	Class only

Think of it like:

Public → Public road 🚶

Protected → Home 🏠 (family only)

Private → Vault 🔒 (owner only)

🔐 Defining Private Variables

Use double underscore (__) before the variable name.

class MyClass:
    def __init__(self):
        self.__private_var = "I am Private"

    def show_private(self):
        return self.__private_var

obj = MyClass()

# print(obj.__private_var)  ❌ Error
print(obj.show_private())   # ✅ Allowed


✔ Direct access is blocked
✔ Access through method is allowed

🔍 Name Mangling (Important Concept)

Private variables are renamed internally by Python.

__private_var  →  _ClassName__private_var


Example:

class MyClass:
    def __init__(self):
        self.__private_var = "I am Private"

obj = MyClass()

print(obj._MyClass__private_var)  # ⚠️ Works (but not recommended)


⚠️ This breaks encapsulation
Use only for debugging or learning

🧩 Private Methods

Methods can also be private using __.

class MyClass:
    def __private_method(self):
        return "Private Method"

    def call_private(self):
        return self.__private_method()

obj = MyClass()

print(obj.call_private())              # ✅
# print(obj.__private_method())        ❌
print(obj._MyClass__private_method())  # ⚠️ Works via name mangling

🏦 Real-World Example: Bank Account

Private variables protect sensitive data like balance.

class BankAccount:
    def __init__(self, balance):
        self.__balance = balance

    def deposit(self, amount):
        self.__balance += amount

    def get_balance(self):
        return self.__balance

account = BankAccount(1000)

# account.__balance = 5000 ❌ Not allowed
account.deposit(500)

print(account.get_balance())  # ✅ 1500


✔ Balance cannot be modified directly
✔ Only controlled through methods

This is real encapsulation.

🧪 Getter & Setter Pattern (Concept)

Getter → read private data

Setter → update private data safely

def get_balance(self):
    return self.__balance

def set_balance(self, value):
    if value >= 0:
        self.__balance = value

📊 Public vs Protected vs Private (Quick Table)
Feature	Public	Protected	Private
Prefix	var	_var	__var
Access	Everywhere	Class + subclass	Class only
Safety	Low	Medium	High
Enforcement	None	Convention	Name mangling
🧠 Key Takeaways

Python uses convention, not strict access control

__ triggers name mangling

Encapsulation = control access

Private ≠ completely hidden

Avoid accessing mangled names in real code

Encapsulation is about discipline, not force.