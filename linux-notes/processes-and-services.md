# Processes and Services in Linux (DevOps Focus)

This file explains how processes and services work in Linux from a system administration and cloud engineering perspective.

---

# 1. What is a Process?

A process is a running instance of a program.

Examples:
- A running web server (nginx)
- A shell session
- A script you execute

Each process has:
- A Process ID (PID)
- Memory usage
- CPU usage
- Parent process

---

# 2. What is a Service?

A service is a background process managed by the system.

Examples:
- nginx (web server)
- sshd (SSH service)
- cron (scheduled tasks)

In modern Linux systems, services are managed by systemd.

---

# 3. Why This Matters in DevOps

In cloud environments (like AWS EC2):

- You constantly check if services are running
- You restart failed services
- You investigate high CPU usage
- You debug broken deployments

Most production issues involve services, not code.

---

# 4. Viewing Processes

## List all processes

```bash
ps aux
```

## Real-time process monitoring

```bash
top
```

or better:

```bash
htop
```

---

# 5. Killing Processes

## Kill by Process ID

```bash
kill <PID>
```

Example:

```bash
kill 1234
```

## Force kill

```bash
kill -9 <PID>
```

---

# 6. Managing Services (systemd)

## Check service status

```bash
systemctl status nginx
```

## Start a service

```bash
systemctl start nginx
```

## Stop a service

```bash
systemctl stop nginx
```

## Restart a service

```bash
systemctl restart nginx
```

## Enable service at boot

```bash
systemctl enable nginx
```

---

# 7. Logs (VERY IMPORTANT in DevOps)

## View system logs for a service

```bash
journalctl -u nginx
```

## Follow logs in real time

```bash
journalctl -u nginx -f
```

---

# 8. Real-World DevOps Use Case

Imagine your website is down on an AWS EC2 instance.

You would:

1. Check if service is running:
```bash
systemctl status nginx
```

2. If not running, start it:
```bash
systemctl start nginx
```

3. Check logs:
```bash
journalctl -u nginx
```

4. Check CPU/memory usage:
```bash
top
```

This is basic production troubleshooting.

---

# 9. Mini Lab (DO LATER ON EC2 OR VM)

1. Install nginx:
```bash
sudo apt install nginx -y
```

2. Check if running:
```bash
systemctl status nginx
```

3. Stop service:
```bash
sudo systemctl stop nginx
```

4. Start service:
```bash
sudo systemctl start nginx
```

5. View logs:
```bash
journalctl -u nginx
```

---

# 10. What to Add Later (After AWS Practice)

After working with EC2:

- How processes behave on cloud servers
- Real debugging of broken services
- High CPU troubleshooting in production
- Difference between system processes vs container processes
