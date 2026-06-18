# S3 Static Website Hosting Lab (AWS Cloud Project)

This project demonstrates how to host a static website using Amazon S3.

---

# 🎯 Objective

- Create an S3 bucket
- Upload a static website
- Enable static website hosting
- Make the site publicly accessible
- Understand object storage vs compute

---

# 🧱 Technologies Used

- Amazon S3
- HTML
- AWS Console

---

# 🧠 Concept Overview

Amazon S3 is an object storage service used to store files.

It can also be used to host static websites (HTML, CSS, JS).

---

# 🏗️ Architecture

```
User Browser
     |
     v
S3 Bucket (Static Website Hosting)
     |
     v
HTML / CSS / JS Files
```

---

# 🚀 Step 1: Create S3 Bucket

In AWS Console:

- Go to S3
- Click "Create bucket"
- Name must be unique (e.g. my-devops-site-123)
- Select region

---

# ⚙️ Step 2: Disable Block Public Access (for learning)

Uncheck:
- Block all public access

Confirm warning.

---

# 📤 Step 3: Upload Website Files

Create a simple `index.html` file:

```html
<!DOCTYPE html>
<html>
<head>
    <title>My DevOps Site</title>
</head>
<body>
    <h1>Hello from AWS S3 🚀</h1>
</body>
</html>
```

Upload it to your bucket.

---

# 🌐 Step 4: Enable Static Website Hosting

Go to:
- Properties → Static website hosting

Enable it:
- Index document: `index.html`

---

# 🔗 Step 5: Access Website

You will get a URL like:

```
http://bucket-name.s3-website-region.amazonaws.com
```

Open it in browser.

---

# 🔍 Troubleshooting

## Access Denied
- Bucket is still private
- Fix: adjust bucket policy

## Website not loading
- Missing index.html
- Static hosting not enabled

---

# 🧠 What You Learned

- Difference between storage and compute
- How S3 serves static content
- Basics of public vs private access
- Cloud object storage fundamentals

---

# 📌 Real-World DevOps Use Case

S3 is used for:

- Hosting frontend websites
- Storing backups
- Serving static assets (images, JS, CSS)
- CI/CD build artifacts

---

# 🔥 How this connects to real architecture

Real systems often look like:

```
S3 (Frontend)
   ↓
CloudFront (CDN)
   ↓
API (EC2 or backend service)
```

---

# 📸 (Optional but HIGHLY recommended)

Add screenshots:
- S3 bucket
- Static hosting settings
- Website in browser

---

# 🚀 Future Improvements

Later you will upgrade this project with:

- Custom domain (Route 53)
- HTTPS (SSL certificate)
- CloudFront CDN
- CI/CD deployment from GitHub

---

# 🧭 Status

✔ First AWS storage project completed  
✔ Static website deployed  
✔ Cloud fundamentals reinforced  
