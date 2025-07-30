
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


### ⚒️ Bitwise “&” Operator

Summary:
Bitwise operators are similar to logical operators, but instead of operating on boolean values, they apply the same logic to all the bits in a value by column. For example, say you had the numbers `5` and `7` represented in binary. You could perform a bitwise AND operation and the result would be `5`.

Example:

0101 is 5
0111 is 7


0101
&
0111

equals

0101


Summary:
A `1` in binary is the same as `True`, while `0` is `False`. So really a bitwise operation is just a bunch of logical operations that are completed in tandem by column.

Example:

0 & 0 = 0

1 & 1 = 1

1 & 0 = 0


Summary:
Ampersand `&` is the bitwise AND operator in Python. "AND" is the _name_ of the bitwise operation, while ampersand `&` is the _symbol_ for that operation. For example, `5 & 7 = 5`, while `5 & 2 = 0`.

Example:

0101 is 5
0010 is 2


0101
&
0010

equals

0000



0b0101 & 0b0111
equals 5

binary_five = 0b0101
binary_seven = 0b0111
binary_five & binary_seven
equals 5


### 🛠️ Bitwise “|” Operator

Summary:
As you may have guessed, the bitwise "or" operator is similar to the bitwise "and" operator in that it works on binary rather than boolean values. However, the bitwise "or" operator "or"s the bits together. Here's an example:

Example:

0101 is 5
0111 is 7


0101 | 0111

equals

0111


Summary:
A `1` in binary is the same as `True`, while `0` is `False`. So a bitwise operation is just a bunch of logical operations that are completed in tandem. When two binary numbers are "or"ed together, the result has a `1` in any place where _either_ of the input numbers has a `1` in that place.

`|` is the bitwise "or" operator in Python. `5 | 7 = 7` and `5 | 2 = 7` as well!

Example:

0101 is 5
0010 is 2


0101 | 0010

equals

0111


### ➡️ Converting Binary

Summary:
The built-in int function can convert a binary string to an integer. It takes a second argument that specifies the base of the number (binary is base 2). For example:

Example:

"100" -> 4
"101" -> 5
"10010" -> 18


this is a binary string
binary_string = "100"

convert binary string to integer
num = int(binary_string, 2)
print(num)
4


