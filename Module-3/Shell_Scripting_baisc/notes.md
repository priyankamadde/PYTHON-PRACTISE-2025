# Advanced Linux Command Line Usage – Revision Notes

These notes summarize key concepts from the advanced Linux command-line class. They cover text editors, stream editing, archiving, compression, file management, and user management.

---

## 1. Text Editors

### 1.1 Vim Editor

Vim is a powerful, modal text editor widely used in Linux systems.

#### Modes in Vim
- **Insert Mode**  
  Allows you to type and edit text like a normal editor.  
  **Command:**  
  ```bash
  i
Command Mode
Used to execute commands for saving, quitting, editing, etc.

Common Vim Commands
Save and exit:

vim
Copy code
:wq
Quit without saving:

vim
Copy code
:q!
Undo last action:

vim
Copy code
u
Copy (yank) current line:

vim
Copy code
yy
Paste copied content:

vim
Copy code
p
Delete current line:

vim
Copy code
dd
Navigation Keys
h → Move left

j → Move down

k → Move up

l → Move right

1.2 Nano Editor
Nano is a simple and user-friendly text editor, often pre-installed on Linux systems.

Basic Nano Commands
Save file:

bash
Copy code
Ctrl + O
Exit editor:

bash
Copy code
Ctrl + X
2. Stream Editor (sed)
sed is used for non-interactive editing of files.

Common sed Operations
Replace Text
Replace all occurrences of a word in a file:

bash
Copy code
sed -i 's/old/new/g' filename
Delete Lines Matching a Pattern
bash
Copy code
sed '/pattern/d' filename
Print a Specific Line
Print the 3rd line of a file:

bash
Copy code
sed -n '3p' filename
3. Archiving and Compression
3.1 Archiving with tar
tar combines multiple files into a single archive without compressing them.

Create a Tar Archive
bash
Copy code
tar -cvf archive.tar folder/
c → create

v → verbose

f → file name

Extract a Tar Archive
bash
Copy code
tar -xvf archive.tar
x → extract

Analogy: tar works like packing tape—it bundles files together without reducing size.

3.2 Compression with gzip
gzip reduces file size for efficient storage.

Compress a File
bash
Copy code
gzip file.txt
Decompress a File
bash
Copy code
gunzip file.txt.gz
Archive and Compress Together
bash
Copy code
tar -czvf archive.tar.gz folder/
Combines tar and gzip

4. File Management
4.1 Truncate
Used to reduce or empty a file from the end.

Example
Empty a file without deleting it:

bash
Copy code
truncate -s 0 filename
4.2 Word Count (wc)
Used to count lines, words, and characters in a file.

Examples
Count lines:

bash
Copy code
wc -l filename
Count words:

bash
Copy code
wc -w filename
Count characters:

bash
Copy code
wc -c filename
5. User Management
Basic User Commands
Display current user:

bash
Copy code
whoami
Show logged-in users and their activities:

bash
Copy code
w
6. Understanding Inodes
Concept
An inode is a data structure that stores metadata about a file, such as:

File permissions

Ownership

File type

Inodes do not store file names or actual data.

7. Upcoming Topic
Process Management
This topic will be covered in the next class and focuses on handling and managing running processes in a Linux environment.

Summary
These commands and concepts form the foundation of advanced Linux command-line usage and are essential for efficient system administration and development workflows.