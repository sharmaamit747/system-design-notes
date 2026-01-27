# Latency vs Throughput

## Latency
Time taken to process **one request**.

Example:
API response in 120ms.

---

## Throughput
Number of requests processed **per second**.

Example:
1000 requests/sec.

---

## Easy Analogy
- Latency = Time for one car to cross bridge
- Throughput = Cars per minute

---

## Optimization Strategy
| Goal | Solution |
|---|---|
| Reduce latency | Cache |
| Increase throughput | Horizontal scaling |

---

## Laravel Example
- Cache user profile → low latency
- Queue emails → high throughput

---

## Interview Answer
> “We optimize latency using caching and throughput using horizontal scaling.”
