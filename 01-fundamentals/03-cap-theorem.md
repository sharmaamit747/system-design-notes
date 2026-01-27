# CAP Theorem (Very Important)

## CAP Means
- Consistency
- Availability
- Partition Tolerance

In distributed systems, you can only guarantee **2 out of 3**.

---

## Easy Explanation
Imagine 2 servers in different cities.

If network breaks:
- Do you show old data? (Availability)
- Or stop response until sync? (Consistency)

You must choose.

---

## CAP Combinations
- CP → MySQL
- AP → Redis
- CA → Not realistic in distributed systems

---

## Laravel Real Example
- Orders table → CP (must be correct)
- Notifications count → AP (can be eventually consistent)

---

## Interview Line
> “For critical data, we prefer consistency. For user experience, availability is acceptable.”

---

## Tech Lead Decision
- Payments → Consistency
- Likes / Views → Availability
