# Dockerized Application Lab (DevOps Foundations)

This project demonstrates how to containerize a simple application using Docker.

---

# 🎯 Objective

- Understand Docker basics
- Create a Docker container
- Run an application inside a container
- Learn how DevOps standardizes environments

---

# 🧱 Technologies Used

- Docker
- Linux
- Simple Python application (or static app)

---

# 🧠 Concept Overview

Docker allows you to package an application with everything it needs to run:

- Code
- Dependencies
- Environment

This ensures it runs the same everywhere.

---

# 📦 Step 1: Create Simple App

Create a file called `app.py`:

```python
print("Hello from Dockerized App 🚀")
```

---

# 🐳 Step 2: Create Dockerfile

Create a file called `Dockerfile`:

```dockerfile
FROM python:3.9-slim

WORKDIR /app

COPY app.py .

CMD ["python", "app.py"]
```

---

# 🔨 Step 3: Build Docker Image

```bash
docker build -t my-docker-app .
```

---

# ▶️ Step 4: Run Container

```bash
docker run my-docker-app
```

Expected output:

```
Hello from Dockerized App 🚀
```

---

# 🧠 What You Learned

- What containers are
- How Docker images work
- How applications are packaged
- Why DevOps uses containers

---

# 📌 Real-World DevOps Use Case

In production:

- Developers build apps
- Docker packages them
- CI/CD pipelines deploy containers
- Kubernetes manages scaling

---

# 🔍 Why Docker is Important

Without Docker:
- “It works on my machine” problem

With Docker:
- Same environment everywhere
- Predictable deployments
- Easy scaling

---

# 🚨 Common Issues

## Docker command not found
- Docker not installed

## Build fails
- Wrong Dockerfile syntax
- Missing files in context

## Container exits immediately
- No running process in container

---

# 🚀 Future Upgrades

This project will later evolve into:

- Multi-container apps (frontend + backend)
- Docker Compose setups
- CI/CD pipeline integration
- Kubernetes deployment

---

# 🧭 Status

✔ First container created  
✔ Docker image built  
✔ Application containerized  
✔ DevOps fundamentals started  
