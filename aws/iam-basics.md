# IAM Basics (Identity and Access Management)

IAM is the AWS service used to manage access to AWS resources securely.

---

# 1. What is IAM?

IAM controls:
- Who can access AWS
- What they can access
- What actions they can perform

---

# 2. Why IAM is Important in DevOps

In real cloud environments:
- You NEVER give full admin access to everyone
- You follow least privilege principle
- You assign roles to services instead of users

---

# 3. Core IAM Components

## Users
An individual person or application.

Example:
- dev-user
- admin-user

---

## Groups
Collection of users with shared permissions.

Example:
- Developers group
- Admin group

---

## Roles (VERY IMPORTANT)
Temporary permissions assigned to AWS services.

Example:
- EC2 role accessing S3

---

## Policies
JSON documents that define permissions.

Example:
- Allow S3 read access
- Deny EC2 termination

---

# 4. IAM Policy Example

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": "s3:ListBucket",
      "Resource": "*"
    }
  ]
}
```

---

# 5. Real-World DevOps Use Case

Instead of giving an EC2 server your AWS credentials:

You assign an IAM Role:

- EC2 instance can access S3
- No hardcoded passwords
- More secure and scalable

---

# 6. IAM Best Practices

- Use least privilege access
- Never use root account for daily tasks
- Use roles instead of access keys when possible
- Rotate credentials regularly

---

# 7. Mini Lab (DO LATER IN AWS)

1. Create IAM user
2. Assign S3 read-only policy
3. Login with IAM user
4. Try accessing S3 bucket
5. Confirm permissions work

---

# 8. What to Add Later

After EC2 practice:

- IAM roles for EC2
- Cross-account access
- Service-linked roles
- Security auditing with IAM
