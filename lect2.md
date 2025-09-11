# 📒 Python Notes — Strings & Conditional Statements

# 1. Strings

A string is a data type that stores a sequence of characters.
Example:

str1 = "hello"
str2 = "world"
print(str1 + str2)  # Output: helloworld

# 🔹 Basic Operations

Concatenation → "hello" + "world" → "helloworld"

Length → len(str) returns the number of characters in the string.

Example:

str1 = "Apna College"
print(len(str1))  # Output: 12

# 🔹 Indexing

Strings are indexed starting from 0.

Negative indexing starts from -1 (last character).

Example:

str1 = "Apna_College"
print(str1[0])   # Output: A
print(str1[-1])  # Output: e


 ⚠ Strings are immutable → str1[0] = 'B' ❌ (Not allowed)

# 🔹 Slicing

Format:

str[start_index : end_index]  # end_index is excluded


Examples:

str1 = "ApnaCollege"
print(str1[1:4])   # Output: pna
print(str1[:4])    # Output: Apna
print(str1[1:])    # Output: pnaCollege

str2 = "Apple"
print(str2[-3:-1]) # Output: pl

# 2. String Functions
str1 = "I am a coder."

print(str1.endswith("er."))       # True
print(str1.count("am"))           # 1
print(str1.capitalize())          # I am a coder.
print(str1.find("coder"))         # 7
print(str1.replace("coder", "developer"))  # I am a developer.

# 3. Practice Problems — Strings

# Problem 1: Input user’s first name & print its length

name = input("Enter your first name: ")
print("Length of your name:", len(name))

# Problem 2: Find the occurrence of ‘$’ in a String

text = input("Enter a string: ")
print("Occurrences of '$':", text.count('$'))

# 4. Conditional Statements
🔹 Syntax
if condition:
    statement1
elif condition:
    statement2
else:
    statementN

# 🔹 Example: Grade Students
marks = int(input("Enter marks: "))

if marks >= 90:
    grade = "A"
elif marks >= 80:
    grade = "B"
elif marks >= 70:
    grade = "C"
else:
    grade = "D"

print("Grade:", grade)

# 5. Practice Problems — Conditional Statements
# Problem 1: Check if a number is odd or even
num = int(input("Enter a number: "))
if num % 2 == 0:
    print("Even number")
else:
    print("Odd number")

# Problem 2: Find the greatest of 3 numbers
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
c = int(input("Enter third number: "))

if a >= b and a >= c:
    print("Greatest:", a)
elif b >= a and b >= c:
    print("Greatest:", b)
else:
    print("Greatest:", c)

# Problem 3: Check if a number is a multiple of 7
num = int(input("Enter a number: "))
if num % 7 == 0:
    print("Multiple of 7")
else:
    print("Not a multiple of 7")