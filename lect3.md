# 📒 Python Notes — Lists & Tuples

# 1. Lists in Python

Definition: A built-in data type that stores a set of values.

Can store elements of different data types (integer, float, string, etc.).

Mutable → we can change elements after creation.

Example:

marks = [87, 64, 33, 95, 76]
student = ["Karan", 85, "Delhi"]

student[0] = "Arjun"  # Allowed
print(len(student))   # Output: 3

# 2. List Slicing

Similar to string slicing.
Format:

list_name[start_index : end_index]  # end_index excluded


Examples:

marks = [87, 64, 33, 95, 76]
print(marks[1:4])   # [64, 33, 95]
print(marks[:4])    # [87, 64, 33, 95]
print(marks[1:])    # [64, 33, 95, 76]
print(marks[-3:-1]) # [33, 95]

# 3. List Methods
nums = [2, 1, 3]

nums.append(4)            # Adds at the end → [2, 1, 3, 4]
nums.insert(1, 5)         # Inserts 5 at index 1 → [2, 5, 1, 3, 4]
nums.sort()               # Ascending sort → [1, 2, 3, 4, 5]
nums.sort(reverse=True)   # Descending sort → [5, 4, 3, 2, 1]
nums.reverse()            # Reverse list
nums.remove(1)            # Removes first occurrence of 1
nums.pop(2)               # Removes element at index 2

# 4. Tuples in Python

Definition: Immutable sequence of values.

Cannot modify elements after creation.

Syntax:

tup = (87, 64, 33, 95, 76)
tup1 = ()        # Empty tuple
tup2 = (1,)      # Tuple with one element (comma is required)
tup3 = (1, 2, 3) # Multiple elements

# 5. Tuple Methods
tup = (2, 1, 3, 1)
print(tup.index(1))  # 1 (first occurrence index)
print(tup.count(1))  # 2 (number of times 1 occurs)

# 📝 Practice Problems — Lists & Tuples
# Problem 1: Enter names of 3 favorite movies
movies = []
for i in range(3):
    name = input(f"Enter movie {i+1}: ")
    movies.append(name)

print("Your favorite movies:", movies)

# Problem 2: Check if a list is a palindrome
lst = [1, 2, 3, 2, 1]
lst_copy = lst.copy()
lst_copy.reverse()

if lst == lst_copy:
    print("The list is a palindrome")
else:
    print("The list is not a palindrome")

# Problem 3: Count students with 'A' grade in a tuple
grades = ("C", "D", "A", "A", "B", "B", "A")
print("Number of A grades:", grades.count("A"))

# Problem 4: Sort grades from 'A' to 'D'
grades_list = list(grades)  # Convert tuple to list
grades_list.sort()
print("Sorted grades:", grades_list)