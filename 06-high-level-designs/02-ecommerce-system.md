# E-Commerce System Design

## Functional Requirements
- Browse products
- Add to cart
- Place order
- Make payment
- Track orders

---

## Non-Functional Requirements
- High availability
- Data consistency
- Secure payments
- Fast response

---

## Core Services
- User Service
- Product Service
- Cart Service
- Order Service
- Payment Service
- Notification Service

---

## High-Level Architecture
Client  
→ API Gateway  
→ Services  
→ DB / Cache / Queue  

---

## Database Design (Simplified)
users  
products  
orders  
order_items  
payments  

---

## Critical Design Decisions
### Cart
- Redis (fast, temporary)

### Orders
- MySQL (transactions)

### Payments
- External gateway
- Idempotency keys

---

## Queue Usage
- Order confirmation email
- Invoice generation
- Inventory update

---

## Laravel Mapping
- Services → Domain logic
- Jobs → Payment confirmation
- Events → OrderPlaced
- Policies → Order access

---

## Interview Line
> “Orders and payments require strong consistency, carts don’t.”
