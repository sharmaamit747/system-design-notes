# Functional vs Non-Functional Requirements

## Functional Requirements
These define **WHAT the system does**.

Examples:
- User can register
- User can place an order
- Admin can approve content

---

## Non-Functional Requirements
These define **HOW the system behaves**.

Examples:
- Response time < 200ms
- System supports 1M users
- Data must be secure

---

## Why Non-Functional Matters More
Most systems fail because of:
❌ slow performance  
❌ downtime  
❌ poor scalability  

Not because features are missing.

---

## Example: Video Upload System

Functional:
- User uploads video
- User watches video

Non-Functional:
- Upload completes within 5 seconds
- Video streams smoothly at 100k concurrent users
- Videos stored securely

---

## Interview Tip
Always say:
> “Let’s clarify both functional and non-functional requirements.”

This shows **senior-level thinking**.

---

## Laravel Mapping
| Requirement | Laravel Solution |
|------|------|
| Fast response | Cache |
| Heavy tasks | Queues |
| Secure APIs | Sanctum / Middleware |
| High traffic | Load balancer + Redis |
