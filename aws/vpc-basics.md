# VPC Basics (AWS Networking Foundation)

Amazon VPC (Virtual Private Cloud) is a logically isolated network in AWS where you launch and manage resources like EC2 instances.

---

# 1. What is a VPC?

A VPC is your private network inside AWS.

It allows you to:
- Launch EC2 instances
- Control network access
- Define IP ranges
- Segment resources

Think of it as your own datacenter inside AWS.

---

# 2. Why VPC is Important in DevOps

In real cloud environments, DevOps engineers must understand:

- How servers communicate
- How traffic flows
- How security is enforced
- Why services are reachable or not

Most AWS connectivity issues are VPC-related.

---

# 3. Core VPC Components

## CIDR Block
Defines IP address range for your VPC.

Example:
```
10.0.0.0/16
```

---

## Subnet
A smaller section of a VPC.

Types:
- Public Subnet (internet access)
- Private Subnet (no direct internet access)

---

## Internet Gateway (IGW)
Allows communication between VPC and the internet.

Without it:
- No public internet access

---

## Route Table
Defines traffic rules for subnets.

Example:
- Send internet traffic to IGW

---

## Security Group
Acts as a firewall for EC2 instances.

Controls:
- inbound traffic
- outbound traffic

---

## Network ACL (NACL)
Additional layer of security at subnet level.

---

# 4. Public vs Private Subnets

## Public Subnet
- Has route to internet gateway
- Used for web servers

## Private Subnet
- No direct internet access
- Used for databases or backend services

---

# 5. How EC2 Uses VPC

When you launch an EC2 instance:
- It is placed inside a VPC
- It is assigned to a subnet
- It gets a private IP
- Optionally gets a public IP

---

# 6. Why You Could NOT Access a Server (Common Issue)

If EC2 is unreachable:

Possible causes:
- Security group missing port 22 or 80
- No internet gateway attached
- Wrong route table
- Instance in private subnet

---

# 7. Real-World DevOps Use Case

A typical web application architecture:

- EC2 in public subnet (web server)
- Database in private subnet
- Internet Gateway for public access
- Security groups control access between layers

---

# 8. Simple VPC Architecture

```
Internet
   |
Internet Gateway
   |
Public Subnet
   └── EC2 (Web Server)
         |
Private Subnet
   └── Database Server
```

---

# 9. Mini Lab (DO LATER IN AWS)

1. Create a VPC
2. Create public subnet
3. Launch EC2 in subnet
4. Attach internet gateway
5. Configure route table
6. Access EC2 via browser or SSH

---

# 10. VPC vs Security Group (IMPORTANT)

| Feature | VPC | Security Group |
|--------|-----|----------------|
| Scope | Network level | Instance level |
| Controls | Routing, subnets | Traffic rules |
| Layer | Infrastructure | Firewall |

---

# 11. What to Add Later

After hands-on AWS:

- VPC peering
- NAT Gateway
- Private routing strategies
- Multi-AZ architecture
- High availability design

---

# 12. Why This Matters

VPC is the **networking brain of AWS**.

If you understand VPC well, you can:
- Debug almost any AWS connectivity issue
- Design real cloud architectures
- Understand production environments
