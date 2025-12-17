# Scaler Live Class – Revision Notes
Topics Covered

Grep and Cut Commands

Pipe Concept

AWK Command

Log Analysis in DevOps

Concept of Log Rotation

Command Line Tools: diff and cmp

# 1. Introduction to Grep and Cut
🔍 Grep Command

Grep is a powerful tool used to search for patterns inside files.
It works like Ctrl + F on Windows but at the command-line level.

Syntax
grep "pattern" filename

Example
<span style="color:#2b82ff; font-weight:bold;"> To search for the status code 200 in a log file: </span>
grep "200" access.log

# ✂️ Cut Command

Cut extracts specific sections of each line based on delimiters.

Syntax
cut -d "delimiter" -f field_number file_name

Example
<span style="color:#ff7b00; font-weight:bold;"> To extract the 2nd column (space-separated): </span>
cut -d " " -f2 access.log

# 2. Understanding Pipe (|) Commands

Pipes allow chaining commands so that the output of one becomes the input of the next.

Example
<span style="color:#9b59b6; font-weight:bold;"> Find a timestamp for a specific IP using grep + cut: </span>
grep "192.168.1.1" access.log | cut -d " " -f 2

# 3. AWK Command for Text Processing

AWK is a mini programming language for advanced text processing, filtering, and formatting.

Basic Syntax
awk 'pattern {action}' filename

📌 Example: Print IP and Status Code

<span style="color:#1abc9c; font-weight:bold;">
Print the 3rd & 6th columns from a log file:</span>

awk '{print $3, $6}' access.log

📌 Example: Count Occurrences of Status Codes

<span style="color:#e91e63; font-weight:bold;">Counting how many times each status code appears:</span>

awk '{count[$6]++} END {for (code in count) print code, count[code]}' access.log

# 4. Log Analysis in DevOps

Log analysis is essential for:

Monitoring

Debugging

Security

Understanding system behavior

# 🌀 Log Rotation

Logs can grow huge over time — log rotation helps manage them by:

Archiving older logs

Compressing logs

Creating numbered backups:

access.log
access.log.1
access.log.2

# 5. Comparing Files with diff and cmp
📘 diff Command

Shows line-by-line differences between two files.

Example
diff file1.log file2.log

📗 cmp Command

Compares files byte-by-byte.

Example
cmp file1.log file2.log

### 📌 Summary

You now understand:

Grep for searching

Cut for extracting

Pipes for chaining commands

AWK for advanced text processing

Log rotation importance

diff & cmp for comparing files

Practice these commands regularly to gain confidence in real DevOps scenarios.


### DUMMY DATA FOR THIS LECTURE => dummy data

cat > access.log << 'EOF'
2025-01-01 10:00:12  192.168.1.10   GET   /login           200 OK            Mozilla/5.0
2025-01-01 10:00:15  192.168.1.11   GET   /home            200 OK            Mozilla/5.0
2025-01-01 10:00:18  192.168.1.10   POST  /buy             500 ERROR         curl/7.74.0
2025-01-01 10:00:20  10.0.0.5       GET   /home            200 OK            Chrome/119.0
2025-01-01 10:00:22  192.168.1.10   GET   /cart            404 NOT_FOUND     Mozilla/5.0
2025-01-01 10:00:25  10.0.0.5       POST  /checkout        500 ERROR         Python-urllib/3.9
2025-01-01 10:00:28  172.16.0.3     GET   /login           200 OK            Safari/17.1
2025-01-01 10:00:30  192.168.1.11   GET   /cart            200 OK            Mozilla/5.0
2025-01-01 10:00:35  203.0.113.45   POST  /admin/login     403 FORBIDDEN     sqlmap/1.6.10
2025-01-01 10:00:38  198.51.100.99  GET   /search?q=shoes  200 OK            Mozilla/5.0
2025-01-01 10:00:40  192.168.1.10   GET   /product/123     200 OK            Mozilla/5.0
2025-01-01 10:00:42  203.0.113.45   GET   /admin           401 UNAUTHORIZED  sqlmap/1.6.10
2025-01-01 10:00:45  172.16.0.3     POST  /cart/add        201 CREATED       Safari/17.1
2025-01-01 10:00:48  10.0.0.5       GET   /offers          200 OK            Chrome/119.0
2025-01-01 10:00:51  192.168.1.11   GET   /buy             503 SERVICE_DOWN  Mozilla/5.0
2025-01-01 10:00:55  198.51.100.99  GET   /search?q=bags   200 OK            Mozilla/5.0
2025-01-01 10:00:58  203.0.113.45   POST  /admin/delete    403 FORBIDDEN     sqlmap/1.6.10
2025-01-01 10:01:00  198.51.100.99  GET   /search?q=shirts 200 OK            Mozilla/5.0
2025-01-01 10:01:02  192.168.1.10   GET   /wishlist        200 OK            Mozilla/5.0
2025-01-01 10:01:05  10.0.0.5       GET   /home            200 OK            Chrome/119.0