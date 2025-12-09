### 🐧 Linux Basics and Scripting – Revision Notes

This revision note covers the key topics from the Linux class, focusing on Linux filesystem concepts, essential commands, and shell scripting fundamentals. Practical examples and analogies are included for easier understanding.

📌 1. Overview

Linux provides a powerful environment for managing files, directories, and automation using shell scripts.
This guide walks through:

Linux filesystem structure

Navigation and file-management commands

Shell scripting basics

Practical command examples

📂 2. Linux Filesystem Basics
## 📁 2.1 Directories and Files

Linux treats everything as a file in a structured hierarchy.

Files are like books in a library.

Directories are like shelves, used to organize groups of files.

Current Directory Commands

pwd — prints the directory you are currently in

ls — lists files and folders inside the current directory

<span style="color:blue">These help you understand: Where am I? What is here?</span>

📌 3. Basic Commands
## 📂 3.1 Creating Directories
mkdir Geography


Creates a directory named Geography.

## 📂 3.2 Changing Directories
cd Geography


Moves inside the folder.

cd ..


Moves one level up.

## 📄 3.3 Creating Files
touch file.txt


Creates an empty file.

## 🗑️ 3.4 Removing Files and Directories
rm file.txt


Remove a file.

rm -rf foldername


Remove a directory recursively.

<span style="color:red; font-weight:bold">❗ WARNING: rm -rf is irreversible. Use with caution!</span>

🏠 4. Understanding Root and Home Directories
📌 Root Directory /

The top-most folder in the Linux filesystem

All files and directories originate from here

📌 Home Directory ~

The user’s personal work area

Stores files, preferences, configurations

Example path: /home/username

🖥️ 5. Shell Scripting Basics

Shell scripts allow automation of tasks using command sequences.

## ⚙️ 5.1 Writing a Simple Shell Script
The Shebang (#!)

Placed on the first line:

#!/bin/bash


Tells Linux which interpreter should execute the script.

## ✏️ 5.2 Creating a Script File

Use vi or vim:

vi script.sh


Add commands inside and save.

## ▶️ 5.3 Making a Script Executable
chmod +x script.sh


Run the script:

./script.sh

📘 6. Example Shell Script
#!/bin/bash
mkdir B
cd B
mkdir Civics
mkdir Physics
cd Civics
touch book3.txt
cd ..
cd Physics
touch book4.txt


<span style="color:purple">This script creates folders and text files inside them automatically.</span>

🔧 7. Common Script Commands
Exiting Vim

:wq — save and exit

:q! — exit without saving

Permissions
chmod 700 script.sh


Gives execute permission only to the owner.

<span style="color:green">Useful for protecting scripts from other users.</span>

🧠 8. CPU, Memory & Disk — Analogy
🔥 CPU (Central Processing Unit)

Acts like multiple burners on a stove — more burners = more multitasking.

🍳 RAM (Random Access Memory)

Works like counter space while cooking — holds items temporarily for quick access.

✅ Conclusion

This revision guide provides a complete, structured overview of Linux basics and scripting concepts.
By practicing commands and writing simple scripts, you can build confidence in navigating and automating tasks in Linux.