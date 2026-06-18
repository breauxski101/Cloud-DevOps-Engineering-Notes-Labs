# Kubernetes Basics + First Deployment Lab

This project introduces Kubernetes and demonstrates deploying a containerized application.

---

# 🎯 Objective

- Understand Kubernetes concepts
- Run a local cluster (Minikube or Kind)
- Deploy an application using Kubernetes
- Expose the application using a Service

---

# 🧠 What is Kubernetes?

Kubernetes is a container orchestration system used to:

- Run containers at scale
- Manage deployments
- Handle scaling and recovery
- Automate container operations

---

# 🧱 Technologies Used

- Kubernetes
- Docker
- kubectl
- Minikube or Kind

---

# ⚙️ Step 1: Start Local Cluster

Using Minikube:

```bash
minikube start
```

Check status:

```bash
kubectl cluster-info
```

---

# 📦 Step 2: Create Deployment

Create file:

```
deployment.yaml
```

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: devops-app
spec:
  replicas: 2
  selector:
    matchLabels:
      app: devops-app
  template:
    metadata:
      labels:
        app: devops-app
    spec:
      containers:
      - name: devops-app
        image: nginx
        ports:
        - containerPort: 80
```

---

# 🚀 Step 3: Apply Deployment

```bash
kubectl apply -f deployment.yaml
```

Check pods:

```bash
kubectl get pods
```

---

# 🌐 Step 4: Expose Deployment

Create service:

```
service.yaml
```

```yaml
apiVersion: v1
kind: Service
metadata:
  name: devops-service
spec:
  type: NodePort
  selector:
    app: devops-app
  ports:
    - port: 80
      targetPort: 80
      nodePort: 30007
```

Apply service:

```bash
kubectl apply -f service.yaml
```

---

# 🔍 Step 5: Access Application

For Minikube:

```bash
minikube service devops-service
```

---

# 🧠 What You Learned

- What Kubernetes is
- How containers are managed at scale
- How deployments work
- How services expose applications
- How orchestration replaces manual container handling

---

# 📌 Real-World DevOps Use Case

In production:

- Applications run in Kubernetes clusters
- Pods scale automatically
- Services handle traffic routing
- Failures are automatically recovered

---

# 🔄 Why Kubernetes Matters

Without Kubernetes:
- Manual container management
- No scaling automation

With Kubernetes:
- Self-healing systems
- Auto scaling
- High availability

---

# 🚨 Common Issues

## Pods not running
- Image pull issues
- YAML indentation errors

## Service not accessible
- Wrong port mapping
- NodePort not configured

## kubectl not working
- Cluster not started

---

# 🧭 Status

✔ Kubernetes cluster started  
✔ Deployment created  
✔ Service exposed  
✔ First container orchestration completed  
