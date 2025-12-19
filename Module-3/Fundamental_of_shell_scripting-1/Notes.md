# Software Engineering — Revision Notes  
## Process Management and Scheduling (Linux)

These revision notes are compiled from a live class session.  
They focus on **process management**, **background execution**, **scheduling**, **prioritization**, and **system monitoring** in Linux.

---

## 1. Background Processes

### Definition
Background processes are programs that run **without blocking the terminal**.  
They execute independently and do not require continuous user interaction.

---

### Simple Analogy
- **Foreground process** → You actively talking to someone  
- **Background process** → Your brain processing sounds around you automatically

---

### Running a Process in Background

#### Using `&`
Appending `&` at the end of a command runs it in the background.

#### Example
```bash
sleep 60 &
This starts a sleep process for 60 seconds without blocking the terminal.

Getting Process ID (PID)
After running a background process, you can retrieve its PID:

bash
Copy code
echo $!
$! → PID of the last background process

2. Scheduling with Cron Jobs
What is a Cron Job?
A cron job is a scheduled task that runs automatically at a specified time or interval.
It is commonly used for:

Backups

Log cleanup

Monitoring scripts

Automation tasks

Cron Syntax
A cron expression consists of five time fields followed by the command:

text
Copy code
*    *    *    *    *  command
|    |    |    |    |
|    |    |    |    +--- Day of week (0–6) Sunday = 0
|    |    |    +-------- Month (1–12)
|    |    +------------- Day of month (1–31)
|    +------------------ Hour (0–23)
+----------------------- Minute (0–59)
Example Cron Expressions
Run a script every minute
bash
Copy code
* * * * * /path/to/script.sh
Run a task every Sunday at midnight
bash
Copy code
0 0 * * 0 command
Managing Cron Jobs
Edit cron jobs
bash
Copy code
crontab -e
List cron jobs
bash
Copy code
crontab -l
3. Process Prioritization
Nice and Renice
Linux assigns priorities to processes using nice values.

Nice Value	Priority
-20	Highest priority
19	Lowest priority

Lower nice value → More CPU time

Start a Process with Priority
bash
Copy code
nice -n 10 your_command
This starts the command with lower priority.

Change Priority of a Running Process
bash
Copy code
renice -n 5 -p 1234
-p 1234 → PID of the process

Priority is adjusted while the process is running

Concept Analogy
Processes with lower nice values are like VIP customers —
they get CPU time first.

4. System Monitoring and Process Inspection
Viewing Process Trees — pstree
Shows parent-child relationships between processes.

bash
Copy code
pstree
Useful for:

Understanding process hierarchy

Debugging stuck or zombie processes

Interactive Monitoring — htop
A visual and interactive version of top.

bash
Copy code
htop
Features:

CPU & memory usage

Process killing

Sorting by resource usage

System Statistics Commands
VMStat — Memory & CPU
bash
Copy code
vmstat
Shows:

CPU usage

Memory

Processes

Paging activity

IOStat — Disk I/O
bash
Copy code
iostat
Used to:

Detect disk bottlenecks

Analyze storage performance

5. Summary
By mastering these commands, you can:

Run tasks in background efficiently

Automate jobs using cron

Control process priority

Monitor system health

Diagnose performance bottlenecks

💡 Practice these commands in a test environment for deeper understanding.