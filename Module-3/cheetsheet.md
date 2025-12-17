🐧 Linux Cheat Sheet – Markdown Version
🟦 1. Linux – Common Commands
📁 Navigation
Command	Meaning
pwd	Show current directory
ls	List files
ls -a	Show hidden files
ls -l	Long listing
cd dir	Change directory
cd ..	Go up one level
📂 File & Directory Operations
Command	Meaning
touch - file	Create an empty file
mkdir dir	Create directory
rm file - 	Delete file
rm -r dir	Delete folder
cp src dest	Copy file
mv src dest	- Move/Rename file
cat file	View file
nano file	Edit file
🔍 Search
Command	Meaning
grep "text" file	Search text in file
find /path -name file	Search file by name
📝 Permissions
Command	Meaning
chmod 777 file	Full permissions
chmod 755 file	Owner full, others read/execute
chown user file	Change file owner
🟩 2. Linux – File & Process Management
📊 File Content & Info
Command	Meaning
wc file	Count lines/words/characters
wc -l file	Line count
wc -w file	Word count
head file	First 10 lines
tail file	Last 10 lines
file file	Determine file type
🧵 Process Management
Command	Meaning
ps	Show running processes
ps aux	List all processes
top	Live process monitor
htop	Better top (if installed)
kill PID	Kill process
kill -9 PID	Force kill
pgrep name	Find PID by name
⚙️ System Monitoring
Command	Meaning
df -h	Disk usage
du -sh folder	Folder size
free -h	Memory usage
uptime	System load
who	Logged-in users
🟧 3. Linux Essentials (Must-Know Basics)
📌 File Types
Type	Symbol
Directory	d
File	-
Link	l
Executable	x
📌 Inode

What an inode stores:

file size

owner

permissions

timestamps

physical data block location

❌ Does NOT store the filename

📌 Permissions
Symbol	Meaning
r	Read
w	Write
x	Execute
🗂 Users & Groups
Command	Meaning
whoami	Current user
id	User + group info
groups username	Group list
sudo command	Run as root
🔗 Links
Command	Meaning
ln file link	Hard link
ln -s file link	Soft (symbolic) link