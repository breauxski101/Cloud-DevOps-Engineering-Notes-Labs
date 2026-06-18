# Basic Linux Commands

This file contains commonly used Linux commands with explanations and real-world use cases for Cloud and DevOps engineering.

---

## pwd

**What it does:**  
Prints the current working directory.

**Example:**
```bash
pwd
```

**Use case:**  
Used when navigating a Linux system to confirm your current location in the filesystem.

---

## ls

**What it does:**  
Lists files and directories.

**Example:**
```bash
ls
ls -l
ls -a
```

**Use case:**  
Used to view files in a directory and check file details or hidden files.

---

## cd

**What it does:**  
Changes the current directory.

**Example:**
```bash
cd Documents
cd ..
cd /
```

**Use case:**  
Used to navigate between directories in the Linux filesystem.

---

## mkdir

**What it does:**  
Creates a new directory.

**Example:**
```bash
mkdir projects
mkdir devops-labs
```

**Use case:**  
Used to organize files into folders for projects and applications.

---

## rm

**What it does:**  
Removes files or directories.

**Example:**
```bash
rm file.txt
rm -r foldername
```

**Use case:**  
Used to delete files or clean up directories.

⚠️ Be careful: deletion is permanent.

---

## touch

**What it does:**  
Creates an empty file.

**Example:**
```bash
touch file.txt
```

**Use case:**  
Used to quickly create files for scripts, logs, or configuration.

---

## cat

**What it does:**  
Displays file content.

**Example:**
```bash
cat file.txt
```

**Use case:**  
Used to quickly view small files or config files.

---

## less

**What it does:**  
Displays file content one page at a time.

**Example:**
```bash
less file.txt
```

**Use case:**  
Used to view large log files or system files.

---

## grep

**What it does:**  
Searches for text inside files.

**Example:**
```bash
grep "error" app.log
```

**Use case:**  
Used in DevOps to find errors in logs or filter output.

---

## find

**What it does:**  
Searches for files and directories.

**Example:**
```bash
find /home -name "file.txt"
```

**Use case:**  
Used to locate files when you don’t know their location.

---

## chmod

**What it does:**  
Changes file permissions.

**Example:**
```bash
chmod 755 script.sh
```

**Use case:**  
Used to control who can read, write, or execute a file.

---

## chown

**What it does:**  
Changes file ownership.

**Example:**
```bash
chown user:user file.txt
```

**Use case:**  
Used in server management to assign file ownership.

---

## ps

**What it does:**  
Shows running processes.

**Example:**
```bash
ps aux
```

**Use case:**  
Used to monitor what is running on the system.

---

## top

**What it does:**  
Shows real-time system processes.

**Example:**
```bash
top
```

**Use case:**  
Used to monitor CPU and memory usage.

---

## kill

**What it does:**  
Stops a running process.

**Example:**
```bash
kill 1234
```

**Use case:**  
Used to stop unresponsive processes.

---

## systemctl

**What it does:**  
Manages system services.

**Example:**
```bash
systemctl status nginx
systemctl start nginx
systemctl stop nginx
```

**Use case:**  
Used to manage services like web servers or databases.

---
