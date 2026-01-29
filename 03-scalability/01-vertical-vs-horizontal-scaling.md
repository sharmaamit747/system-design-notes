# Vertical vs Horizontal Scaling

## What is Scaling?
Scaling means handling **more users, more traffic, more data** without breaking the system.

---

## Vertical Scaling (Scale Up)

### Meaning
Add more power to **one server**:
- More RAM
- Faster CPU

### Example
Upgrade EC2 from 4GB → 16GB RAM

### Pros
- Simple
- No code change

### Cons
- Has a limit
- Single point of failure
- Expensive

---

## Horizontal Scaling (Scale Out)

### Meaning
Add **more servers**.

### Example
1 Laravel server → 5 Laravel servers

### Pros
- Highly scalable
- Fault tolerant

### Cons
- Needs load balancer
- Session management required

---

## Laravel Perspective

### Vertical Scaling
- Increase PHP memory
- Increase MySQL resources

### Horizontal Scaling
- Multiple Laravel instances
- Redis for session & cache
- Load balancer in front

---

## Interview Answer
> “We start with vertical scaling for simplicity and move to horizontal scaling when traffic grows.”

---

## Tech Lead Rule
Vertical scales **limits**, horizontal scales **infinity**.
