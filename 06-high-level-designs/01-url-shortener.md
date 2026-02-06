# URL Shortener System (Like Bitly)

## Functional Requirements
- Generate short URL
- Redirect to original URL
- Track clicks

## Non-Functional Requirements
- Low latency redirects (<50ms)
- Highly available
- Scalable to millions of URLs

---

## Scale Estimation
- 10M URLs
- 100M redirects/day
- Read-heavy system

---

## High-Level Architecture
Client → API → Cache → DB

Redirect flow:
Short URL → Cache → DB → Redirect

---

## Database Design
urls
- id
- short_code (indexed, unique)
- long_url
- created_at

---

## Short Code Generation
- Base62 encoding
- Auto-increment ID

---

## Caching Strategy
- Cache short_code → long_url in Redis
- TTL optional

---

## Bottlenecks & Solutions
| Problem | Solution |
|------|------|
| DB load | Redis cache |
| Collision | Unique index |
| High traffic | Horizontal scaling |

---

## Laravel Mapping
- Controller → RedirectController
- Cache → Redis
- DB → MySQL/Postgres
- Middleware → Rate limit

---

## Interview Line
> “URL shortener is read-heavy, so caching is critical.”
