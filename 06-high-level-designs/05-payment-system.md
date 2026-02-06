# Payment System Design

## Functional Requirements
- Initiate payment
- Verify payment
- Update order status

---

## Non-Functional Requirements
- Strong consistency
- Security
- Idempotency

---

## Architecture
Client  
→ Backend  
→ Payment Gateway  
→ Webhook  
→ Backend  

---

## Payment Flow
1. Create payment intent
2. Redirect to gateway
3. Gateway calls webhook
4. Verify signature
5. Update DB

---

## Database Tables
payments
- id
- order_id
- gateway_id
- status
- amount

---

## Critical Concepts
- Transactions
- Idempotency keys
- Webhook verification

---

## Laravel Mapping
- Webhook controller
- DB transactions
- Queues for post-payment tasks

---

## Interview Line
> “Payment systems must handle retries without double charging.”
