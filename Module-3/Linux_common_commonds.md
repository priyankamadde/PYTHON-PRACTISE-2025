🔐 Comprehensive Notes on File and Directory Permissions in Linux

Understanding permissions is essential for managing system security and controlling access in Linux.
This guide covers file permissions, ownership, ACLs, redirection, and useful commands.

📌 1. Understanding Linux Permissions

Linux permissions determine who can perform what actions on files and directories.

📂 2. Basics of File Permissions

Permissions are divided into three types:

Read (r) — View file or list directory

Write (w) — Modify file or add/remove items in a directory

Execute (x) — Run scripts/programs or enter a directory

Each file/directory has permissions for:

User (u) → the owner

Group (g) → assigned group

Others (o) → everyone else

🔢 3. Numerical (Octal) Permission Representation

Each permission has a number:

Permission	Value
Read (r)	4
Write (w)	2
Execute (x)	1

Add them to form a numeric mode.

Example: 755

7 = 4+2+1 → read, write, execute (user)

5 = 4+1 → read, execute (group)

5 = 4+1 → read, execute (others)

<span style="color:blue">✔ Shortcut: Higher number = more access</span>

👤 4. Changing Ownership & Permissions
## 📌 chown — Change Ownership

Format:

chown user:group filename


Example:

chown root:basketball_group basketball

## 📌 chmod — Change Permissions

Format:

chmod 755 filename


Example with meaning:

chmod 760 basketball


7 → user (root) has full access

6 → group has read + write

0 → others have no access

<span style="color:red">❗Important: Misusing permission values can expose files or lock out access.</span>

🏫 5. School Analogy for Permissions

Imagine:

Files = sports equipment → basketball, football, tennis

Groups = sports teams → basketball_group, football_group

Root (admin) = teacher

Steps:

Create files

Create groups

Assign files to groups

Restrict access using chmod

Example:

chown root:basketball_group basketball
chmod 760 basketball


<span style="color:green">✔ Basketball team can use their ball, others cannot.</span>

🧩 6. ACL (Access Control Lists)

ACLs allow assigning permissions to individual users, not just user-group-others.

Commands:

Set ACL
setfacl -m u:john:rw file.txt

View ACL
getfacl file.txt


<span style="color:purple">✔ ACLs provide fine-grained, flexible permission control.</span>

🔄 7. Redirection & Pipe Operators
## 🔁 Redirection

> → overwrite

>> → append

Example:

echo "Hello" > file.txt
echo "More data" >> file.txt

## 🔗 Pipe ( | )

Sends output of one command to another:

ls -l | grep ".txt"


<span style="color:orange">✔ Pipes are essential for chaining commands.</span>

👥 8. Additional Commands
## ➕ Adding a User to a Group
usermod -aG groupname username

## ✨ Wildcards

* → matches many characters

? → matches one character

Example:

ls *.txt

🏁 9. Summary

Linux permissions help control:

who reads files

who modifies files

who executes programs

Core tools:

chmod → change permissions

chown → change ownership

ACLs → extended, fine access control

<span style="color:blue; font-weight:bold">Understanding permissions = secure system + proper access management.</span>