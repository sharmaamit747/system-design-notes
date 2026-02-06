# Chat System Design (WhatsApp-like)

## Functional Requirements
- Send messages
- Receive messages
- Online status

---

## Non-Functional Requirements
- Real-time delivery
- Low latency
- High availability

---

## Architecture
Client  
→ WebSocket Server  
→ Message Queue  
→ DB  

---

## Data Model
messages
- id
- sender_id
- receiver_id
- message
- timestamp

---

## Message Flow
1. Client sends message
2. WebSocket server receives
3. Push to queue
4. Store in DB
5. Deliver to receiver

---

## Scaling Strategy
- Horizontal WebSocket servers
- Redis pub/sub
- Sharded DB if needed

---

## Laravel Mapping
- Laravel WebSockets
- Redis
- Queues for persistence

---

## Interview Line
> “Real-time systems separate delivery from persistence.”
