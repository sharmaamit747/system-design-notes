# Queue-Based Architecture

## Why Queues?
Queues move **slow tasks** out of the request cycle.

---

## Without Queue
User → API → Email → Response ❌ (slow)

---

## With Queue
User → API → Queue → Worker → Email ✅

---

## Laravel Queue Example
```php
SendEmailJob::dispatch($user);
```

## Queue Benefits

- Faster API response
- Better user experience
- Retry on failure
- Scales independently

## Common Use Cases

- Emails
- Notifications
- Reports
- Image processing

## Golden Line
“Queues help achieve asynchronous processing and better scalability.”