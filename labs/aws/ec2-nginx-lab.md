# EC2 Nginx Deployment Lab (AWS + Linux + Networking)

This project demonstrates how to deploy and expose a web server on an AWS EC2 instance.

---

# 🎯 Objective

- Launch an EC2 instance
- Connect via SSH
- Install Nginx web server
- Configure security groups
- Access server via browser
- Understand basic cloud networking flow

---

# 🧱 Technologies Used

- AWS EC2
- Ubuntu Linux
- SSH
- Nginx
- Security Groups

---

# 🏗️ Architecture

```
User Browser
     |
     v
AWS Security Group (Port 80)
     |
     v
EC2 Instance (Ubuntu)
     |
     v
Nginx Web Server
```

---

# 🚀 Step 1: Launch EC2 Instance

In AWS Console:

- Choose AMI: Ubuntu Server
- Instance type: t2.micro
- Create/select key pair
- Configure security group:

### Inbound rules:
- SSH (22) → My IP
- HTTP (80) → Anywhere (0.0.0.0/0)

---

# 🔑 Step 2: Connect via SSH

```bash
chmod 400 key.pem
ssh -i key.pem ubuntu@<public-ip>
```

---

# 📦 Step 3: Install Nginx

```bash
sudo apt update
sudo apt install nginx -y
```

---

# ▶️ Step 4: Start Nginx

```bash
sudo systemctl start nginx
sudo systemctl enable nginx
```

Check status:

```bash
systemctl status nginx
```

---

# 🌐 Step 5: Access Website

Open browser:

```
http://<public-ip>
```

You should see:
> Welcome to Nginx

---

# 🔍 Step 6: Troubleshooting

## Website not loading
- Check security group (port 80 open)
- Ensure Nginx is running:
```bash
systemctl status nginx
```

## SSH not working
- Wrong key permissions
- Port 22 not open
- Wrong IP

---

# 🧠 What You Learned

- How cloud servers (EC2) work
- How SSH connects to Linux machines
- How web servers run on Linux
- How security groups control traffic
- Basic production troubleshooting

---

# 📌 Real-World DevOps Connection

This is exactly how production systems work:

- EC2 = application server
- Nginx = web server / reverse proxy
- Security groups = firewall rules
- SSH = remote administration

---

# 📸 (Optional but powerful)

Add screenshots to repo:
- EC2 running instance
- SSH terminal
- Nginx page in browser

---

# 🚀 Next Improvements (Future upgrades)

Later you will extend this project with:

- Custom HTML website
- Domain name (Route 53)
- HTTPS (SSL)
- Load balancer
- Auto Scaling Group
- Terraform deployment

---

# 🧭 Status

✔ First cloud deployment completed  
✔ Linux + AWS integration  
✔ Networking fundamentals applied  
