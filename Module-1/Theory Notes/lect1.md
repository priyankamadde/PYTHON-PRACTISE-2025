# Python Basics
Programming Flow
Programming → Translator → Machine Code

Translators: Compiler / Interpreter

# What is Python?
Simple & easy to learn

Free & Open Source

High-Level Language

Developed by Guido van Rossum

Portable (works on multiple platforms)

Example:

Ex - print("Hello World")

# Python Character Set
Letters: A to Z, a to z

Digits: 0 to 9

Special Symbols: +, -, *, /, %, etc.

Whitespaces: space, tab, carriage return, newline, formfeed

Other Characters: Supports all ASCII and Unicode characters as part of data or literals

# Variables
A variable is a name given to a memory location in a program.

Example:
name = "Shradha"
age = 23
price = 25.99

# Rules for Identifiers

Must start with a letter or underscore _

Cannot start with a digit

Can contain letters, digits, and underscores

Case-sensitive (name and Name are different)

Cannot be a Python keyword

# Data Types
Integer – whole numbers (10, -5)

String – sequence of characters ("hello", 'world')

Float – decimal numbers (3.14, -0.5)

Boolean – True or False

None – represents no value

# Keywords
Reserved words in Python

Must be typed exactly as defined (case-sensitive)

Example: False (uppercase F) is valid, but false is not

# Comments in Python
Single Line Comment: #

# This is a single line comment
Multi-Line Comment: Multiple # or '''...''' / """..."""

# Types of Operators
- An operator is a symbol that performs a certain operation between operands.
Arithmetic Operators
+, -, *, /, %, **

Relational / Comparison Operators
==, !=, >, <, >=, <=

Assignment Operators
=, +=, -=, *=, /=, %=, **=

Logical Operators
not, and, or


# Type Conversion (Implicit)
a, b = 1, 2.0
sum_val = a + b  # 1 is converted to float automatically:

a, b = 1, "2"
sum_val = a + b  # TypeError: unsupported operand types

# Type Casting (Explicit)

a, b = 1, "2"
c = int(b)  # converting "2" to integer
sum_val = a + c

# Input in Python

input()              # always returns a string
int(input())         # converts input to integer
float(input())       # converts input to float

# Example Programs

# 1] Input 2 numbers & print their sum

a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
print("Sum:", a + b)

# 2] Input side of a square & print its area
side = float(input("Enter side length of square: "))
area = side ** 2
print("Area of square:", area)

# 3] Input 2 floating point numbers & print their average
x = float(input("Enter first number: "))
y = float(input("Enter second number: "))
average = (x + y) / 2
print("Average:", average)

# 4] Input 2 integers and print True if first ≥ second

a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
print(a >= b)