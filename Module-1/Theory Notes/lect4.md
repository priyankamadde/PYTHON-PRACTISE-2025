# 📒 Python Notes — Dictionaries & Sets

# 1. Dictionaries in Python

Store data in key:value pairs.

Unordered, mutable, and keys must be unique.

Syntax:

myDict = {
    "name": "Karan",
    "cgpa": 8.7,
    "marks": [90, 85, 88]
}

# Access values
print(myDict["name"])   # Karan

# Add/Update values
myDict["city"] = "Delhi"

# 2. Nested Dictionaries

Dictionary inside another dictionary.

student = {
    "name": "Karan",
    "score": {
        "math": 95,
        "science": 90
    }
}
print(student["score"]["math"])  # 95

# 3. Dictionary Methods
myDict = {"name": "Karan", "age": 20}

print(myDict.keys())             # dict_keys(['name', 'age'])
print(myDict.items())            # dict_items([('name', 'Karan'), ('age', 20)])
print(myDict.values())           # dict_values(['Karan', 20])
print(myDict.get("age"))         # 20

myDict.update({"city": "Delhi"}) # Add/Update
print(myDict)

# 4. Sets in Python

Unordered collection of unique, immutable elements.

Syntax:

null_set = set()      # Empty set
nums = {1, 2, 3, 4}
set2 = {1, 2, 2, 2}   # Output: {1, 2} (duplicates removed)

# 5. Set Methods
set1 = {1, 2, 3}

set1.add(4)                       # {1, 2, 3, 4}
set1.remove(2)                    # Removes 2
set1.clear()                      # Empty set {}
set1.pop()                        # Removes random element

# Union & Intersection
a = {1, 2, 3}
b = {3, 4, 5}
print(a.union(b))                 # {1, 2, 3, 4, 5}
print(a.intersection(b))          # {3}

# 📝 Practice Problems — Dictionaries & Sets

# Problem 1: Store word meanings

dictionary = {
    "table": ["a piece of furniture", "list of facts & figures"],
    "cat": "a small animal"
}
print(dictionary)

# Problem 2: Count classrooms needed

subjects = ["python", "java", "C++", "python", "javascript",
            "java", "python", "java", "C++", "C"]

unique_subjects = set(subjects)
print("Classrooms needed:", len(unique_subjects))

# Problem 3: Store marks of 3 subjects

marks_dict = {}
for i in range(3):
    subject = input("Enter subject name: ")
    marks = int(input(f"Enter marks for {subject}: "))
    marks_dict[subject] = marks

print(marks_dict)

# Problem 4: Store 9 and 9.0 separately in a set

⚠ In Python, 9 and 9.0 are treated as the same because they compare equal (int vs float).
✅ Solution → Store them as different data types, e.g., one as int and one as str:

my_set = {9, "9.0"}  # String makes it different
print(my_set)        # {9, '9.0'}