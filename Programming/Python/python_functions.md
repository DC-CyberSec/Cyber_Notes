# 🐍 Python Functions – Learning Notes

## 🧩 Functions

Summary:
Functions encapsulate reusable logic. Defined with def, called with ().

Example:

def greet(name):
    return f"Hello, {name}"

print(greet("Alice"))  # Output: Hello, Alice

## ⚙️ Functions with Multiple Parameters

Summary:
Functions can take multiple inputs (parameters).

Example:

def add(a, b):
    return a + b

print(add(3, 4))  # Output: 7

## 📐 Function Declaration Order

Summary:
Functions and variables must be defined before they are used.

Incorrect:

say_hello()  # Error: function not defined yet

def say_hello():
    print("Hello")

## ❓ None Return in Functions

Summary:
If no return is specified, Python returns None.

Example:

def log_message(msg):
    print(msg)  # Returns None implicitly

## 🎁 Multiple Return Values

Summary:
Functions can return multiple values using commas. They are returned as a tuple.

Example:

def get_stats():
    return 80, 95

score, high_score = get_stats()

## 📥 Parameters vs Arguments

Summary:

    Parameters are placeholders in function definitions.

    Arguments are actual values passed during function calls.

Example:

def greet(name):  # name is a parameter
    print(f"Hello, {name}")

greet("Alice")  # "Alice" is an argument

## ⚙️ Default Function Arguments

Summary:
Functions can assign default values to parameters.

Rules:

    Default parameters must come after required ones.

Example:

def greet(name="Guest"):
    print(f"Hello, {name}")

greet()  # Hello, Guest
greet("Alice")  # Hello, Alice

