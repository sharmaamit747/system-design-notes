# What is System Design?

## Simple Definition
System Design is about **planning how a software system will work** before writing code.

It answers questions like:
- How will data flow?
- How will the system scale?
- What happens when traffic increases?
- How do components talk to each other?

👉 As a **Senior Laravel Developer**, system design means:
You don’t just write APIs — you design **solutions**.

---

## Real-Life Analogy
Building a house:
- Code = bricks
- Framework = tools
- System Design = blueprint

Without a blueprint, the house may fall.

---

## Why System Design is Important
- Avoids performance issues
- Reduces future rewrites
- Handles millions of users
- Saves infrastructure cost

---

## Interview One-Liner
> “System design is about defining architecture, components, and data flow while considering scalability, reliability, and performance.”

---

## Laravel Mapping
| Concept | Laravel Example |
|------|------|
| API Layer | Controllers |
| Business Logic | Services |
| Async Processing | Queues / Jobs |
| Performance | Cache / Redis |
| Security | Middleware / Policies |

---

## Example
Bad Design:
Controller → DB → Response

Good Design:
Controller → Service → Repository → DB  
Controller → Job → Queue → Worker

---

## Tech Lead Mindset
- Think long-term
- Assume traffic will grow
- Minimize coupling
- Maximize readability
