🐧 Linux Revision Notes

Welcome to the revision notes for our Linux class. This document covers essential Linux concepts, commands, navigation, file handling, and the differences between hardlinks and softlinks. Use this as a quick and complete guide for revision.

🗂️ 1. Basic Linux Navigation Commands
### 📌 1.1 PWD (Present Working Directory)

Purpose:
Displays the current directory you're working in.
Usage:

pwd


It returns the absolute path of your present directory.
Highlight: <span style="color:blue">Useful for checking "Where am I right now?"</span>

### 📌 1.2 CD (Change Directory)

Purpose:
Allows you to navigate between directories.

Usage Patterns:

cd <directory-path>   # Move into a given directory
cd ..                 # Move to parent directory
cd ../..              # Go up two levels


Analogy:
Using cd is like entering a destination into your GPS — you can use both relative and absolute paths.

📁 2. File and Directory Handling
### 📌 2.1 LS (List Directory Contents)

Purpose:
Lists files and directories.

Advanced Usage:

ls <file-name>   # Check if a file exists
ls *.txt         # List all .txt files
ls a*.txt        # List files starting with 'a'


Wildcards:

* → matches multiple characters

? → matches a single character

### 📌 2.2 MKDIR & RMDIR

MKDIR — Creates a new directory

mkdir newFolder


RMDIR — Removes an empty directory

rmdir oldFolder

### 📌 2.3 RM & RMRF

Purpose: Delete files or directories.

Usage:

rm <file>         # Remove a file
rm -rf <dir>      # Force delete directory + contents


Warning:
<span style="color:red; font-weight:bold">❗ rm -rf is extremely dangerous and cannot be undone.</span>

### 📌 2.4 TOUCH

Creates an empty file.

touch file.txt

📦 3. File Copy & Move Commands
### 📌 3.1 CP (Copy)

Purpose: Create a duplicate of a file.

cp source.txt destination.txt


Note:
<span style="color:green">Source file remains unchanged.</span>

### 📌 3.2 MV (Move)

Purpose: Move or rename files.

mv oldname.txt newname.txt


Note:
<span style="color:purple">Works like renaming — original file path no longer exists.</span>

🔗 4. Links: Hardlinks & Softlinks
### 📌 4.1 Hardlink

Characteristics:

Multiple file names point to the same inode

Deleting one link does not remove data as long as another link exists

Must be on the same filesystem

Analogy:
<span style="color:orange">Like one city having two different names — remove one, city still exists.</span>

### 📌 4.2 Softlink (Symbolic Link)

Characteristics:

Acts like a shortcut

Can link across filesystems

If the original file is deleted, the symlink breaks (dangling link)

🧰 5. Additional Commands
### 📌 5.1 CAT

Displays the content of a file:

cat file.txt

### 📌 5.2 ECHO

Prints a string:

echo "Hello World"

### 📌 5.3 CLEAR

Clears the terminal screen:

clear

### 📌 5.4 HISTORY

Displays previously executed commands:

history


<span style="color:blue">Helpful for debugging, re-running commands, or auditing.</span>

✅ Conclusion

By mastering these Linux commands and concepts, you can efficiently navigate and manage Linux systems.
Always handle powerful commands like rm -rf with extreme caution, and use wildcard patterns to speed up file operations.