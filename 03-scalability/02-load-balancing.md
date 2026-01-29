# Load Balancing

## What is Load Balancer?
A load balancer distributes traffic across **multiple servers**.

---

## Why It’s Needed
Without load balancer:
- One server gets overloaded
- Downtime if server fails

---

## Common Load Balancers
- Nginx
- AWS ALB / ELB
- HAProxy

---

## Request Flow
User → Load Balancer → Laravel Servers

---

## Load Balancing Algorithms
- Round Robin
- Least Connections
- IP Hash

---

## Laravel Session Problem
With multiple servers:
❌ File-based sessions break

---

## Solution
Store sessions in:
- Redis
- Database

```env
SESSION_DRIVER=redis
