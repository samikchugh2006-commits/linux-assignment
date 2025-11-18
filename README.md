# CSFCP Assignment – Unit 2  
## Linux Shell Commands & Shell Scripting

---

## 📌 *Project Overview*
This project demonstrates basic Linux command usage and shell scripting as part of the CSFCP Unit 2 assignment.  
The work includes:

- Setting up a Linux environment (WSL Ubuntu on Windows 10)
- Executing common Linux commands
- Creating and running three shell scripts:
  - A directory backup script
  - A system monitoring script
  - A file download automation script

All scripts were tested in the Ubuntu terminal and sample outputs/screenshots are included separately.

---

## 📁 *Instructions for Running the Scripts*

### **1️⃣ How to Run backup.sh**
This script creates a compressed (.tar.gz) backup of a directory.

```bash
cd scripts
chmod +x backup.sh
./backup.sh <directory_path>

Example:

./backup.sh ~/linux_assignment

The backup file will be saved inside the backups/ folder.


---

2️⃣ How to Run monitor.sh

This script logs CPU and memory usage every few seconds into monitor_logs.csv.

chmod +x monitor.sh
nohup ./monitor.sh 2 > /dev/null 2>&1 &

To stop the script:

ps aux | grep monitor.sh
kill <PID>


---

3️⃣ How to Run download.sh

This script downloads a file from a given URL into the downloads/ folder.

chmod +x download.sh
./download.sh <url>

Example:

./download.sh https://example.com/sample.txt


---

📄 Brief Description of Each Script

🔹 backup.sh

Accepts a directory as input.

Creates a timestamped .tar.gz archive of that directory.

Stores the backup under the backups/ folder.


🔹 monitor.sh

Continuously records CPU load and memory usage at fixed intervals.

Saves entries into a CSV log file (monitor_logs.csv) for later analysis.


🔹 download.sh

Downloads any file from a provided URL using wget or curl.

Saves downloaded files inside the downloads/ folder.



---
