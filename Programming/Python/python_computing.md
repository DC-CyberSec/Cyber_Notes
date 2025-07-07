
### 1️⃣ Python Numbers

Summary:
Python uses whole numbers and decimals referred to as Integers and Floats respectively. These let Python compute mathematical operations such as addition, subtraction and so on. Because Python is so good at mathematical operations it is the go to language for data analysis, machine learning, and other heavy computing tasks.

### ➗ Floor Division

Summary: 
Floor division is like normal division except the result is floored afterward, which means the result is rounded down to the nearest integer. The `//` operator is used for floor division.

Example:

7 // 3
#2 (an integer, rounded down from 2.333)
-7 // 3
#"-3" (an integer, rounded down from -2.333)

### 📈 Exponents

Summary:
Python has built-in support for exponents - something most languages require a `math` library for.

Example:

reads as "three squared" or
"three raised to the second power"
3 ** 2
9

### ➕ Plus Equals

Summary:
Python makes reassignment easy when doing math. In JavaScript or Go, you might be familiar with the `++` syntax for incrementing a number variable by 1. In Python, we use the `+=` in-place operator instead. 

Example:

star_rating = 4
star_rating += 1
star_rating is now 5

star_rating = 4
star_rating -= 1
star_rating is now 3

star_rating = 4
star_rating *= 2
star_rating is now 8

star_rating = 4
star_rating /= 2
star_rating is now 2.0

### ⚗️ Scientific Notation

Summary:
As we covered earlier, a `float` is a positive or negative number **with a fractional part**.

You can add the letter `e` or `E` followed by a positive or negative integer to specify that you're using scientific notation.

If you're not familiar with scientific notation, it's a way of expressing numbers that are too large or too small to conveniently write normally.

In a nutshell, the number following the `e` specifies how many places to move the decimal to the right for a positive number, or to the left for a negative number.

Example:

print(16e3)
Prints 16000.0

print(7.1e-2)
Prints 0.071

##### Underscores for Readability

Summary:
Python also allows you to represent large numbers in the decimal format using underscores as the delimiter instead of commas to make it easier to read.

Example:

num = 16_000
print(num)
Prints 16000

num = 16_000_000
print(num)
Prints 16000000

### 👨‍💻 Logical Operators

Summary:
You're probably familiar with the logical operators `and` and `or`.

Logical operators deal with boolean values, `True` and `False`.

The logical `and` operator requires that _both_ inputs are `True` to return `True`. The logical `or` operator only requires that _at least one_ input is `True` to return `True`.

Example:

True and True == True
True and False == False
False and False == False

True or True == True
True or False == True
False or False == False

##### Python Syntax

Example:

print(True and True)
prints True

print(True or False)
prints True


##### Nesting With Parentheses

Summary:
We can nest logical expressions using parentheses.

Example:

print((True or False) and False)

First, we evaluate the expression in the parentheses, `(True or False)`. It evaluates to `True`:

print(True and False)

`True and False` evaluates to `False`:

print(False)

So, `print((True or False) and False)` prints "False" to the console.

##### Not

Summary:
We skipped a very important logical operator - `not`. The `not` operator reverses the result. It returns `False` if the input was `True` and vice-versa.

Example:

print(not True)
Prints: False

print(not False)
Prints: True

### 1️⃣ Binary Numbers

Summary:
Binary numbers are just "base 2" numbers. They work the same way as "normal" base 10 numbers, but with two symbols instead of ten.

- Base-2 (binary) symbols: `0` and `1`
- Base-10 (decimal) symbols: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`

Each `1` in a binary number represents an ever-greater multiple of 2. In a 4-digit number, that means you have the eights place, the fours place, the twos place, and the ones place. Similar to how in decimal you would have the thousands place, the hundreds place, the tens place, and the ones place.

Example:

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/OOUTUVo-904x350.png)

##### Binary in Python

Summary:
You can write an integer in Python using binary syntax using the `0b` prefix:

Example:

print(0b0001)
Prints 1

print(0b0101)
Prints 5

