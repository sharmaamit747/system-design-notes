# Events & Listeners

## Problem
Tight coupling between actions.

---

## Solution
Event-driven architecture.

```php
event(new OrderPlaced($order));
```

### Listeners:
- Send email
- Update analytics
- Notify admin

---

## Benefits
- Clean code
- Easy extension
- Async ready

“Events decouple actions from side effects.”