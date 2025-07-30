
# 🐍 Python Scope – Learning Notes

## 👀 Scope

Summary:
Refers to _where_ a variable or function name is available to be used.

Example:

def subtract(x, y):
    return x - y

result = subtract(5, 3)
print(x)
ERROR! "name 'x' is not defined"

## 🌏 Global Scope

Summary:
When we define a variable or a function, that name is accessible in _every other place_ in our program, even within other functions.

Example: 

pi = 3.14

def get_area_of_circle(radius):
    return pi * radius * radius

