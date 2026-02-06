# Notification System Design

## Functional Requirements
- Send email
- Send SMS
- Send push notification

---

## Non-Functional Requirements
- Reliable delivery
- Retry on failure
- Scalable

---

## Architecture
Event → Queue → Workers → Providers

---

## Flow
OrderPlaced Event  
→ Notification Job  
→ Queue  
→ Worker  
→ Email/SMS Provider

---

## Database
notifications
- id
- user_id
- type
- status
- retries

---

## Retry Strategy
- Exponential backoff
- Dead letter queue

---

## Laravel Mapping
- Events & listeners
- Jobs
- Horizon
- Mail / SMS drivers

---

## Interview Line
> “Notifications must never block user requests.”
