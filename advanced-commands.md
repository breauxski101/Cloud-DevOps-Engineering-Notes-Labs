# Advanced Linux Commands (DevOps Focus)

This file expands on commonly used Linux commands with deeper explanations and real-world DevOps use cases.

---

## grep

**What it does:**  
Searches for patterns inside files or output.

**Example:**
```bash
grep "ERROR" /var/log/syslog
```

**Common use case:**  
Finding errors in system or application logs.

**DevOps use:**  
Debugging failed services or deployments.

---

## find

**What it does:**  
Searches for files and directories.

**Example:**
```bash
find / -name "*.log"
```

**Common use case:**  
Locating files when path is unknown.

**DevOps use:**  
Finding logs, config files, or missing deployments.

---

## curl

**What it does:**  
Transfers data from or to a server.

**Example:**
```bash
curl http://localhost
```

**Common use case:**  
Testing APIs or websites.

**DevOps use:**  
Checking if a service is running or API is responding.

---

## ping

**What it does:**  
Checks network connectivity.

**Example:**
```bash
ping google.com
```

**Common use case:**  
Testing if a host is reachable.

**DevOps use:**  
Troubleshooting network issues.

---

## netstat / ss

**What it does:**  
Shows network connections.

**Example:**
```bash
ss -tulpn
```

**Common use case:**  
Checking open ports.

**DevOps use:**  
Debugging service connectivity issues.

---

## df

**What it does:**  
Shows disk usage.

**Example:**
```bash
df -h
```

**Common use case:**  
Checking storage space.

**DevOps use:**  
Monitoring server disk usage.

---

## du

**What it does:**  
Shows directory size.

**Example:**
```bash
du -sh *
```

**Common use case:**  
Finding large files or folders.

**DevOps use:**  
Cleaning up servers.

---

## tar

**What it does:**  
Archives files.

**Example:**
```bash
tar -cvf backup.tar folder/
```

**Common use case:**  
Creating backups.

**DevOps use:**  
Deploying applications or backups.

---
