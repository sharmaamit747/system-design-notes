# Normalization vs Denormalization

## Normalization
Split data into multiple tables to avoid duplication.

### Example
Users table  
Orders table

Benefits:
- Clean data
- Easy updates
- Less redundancy

---

## Denormalization
Duplicate some data for performance.

### Example
Store `user_name` in orders table.

Benefits:
- Faster reads
- Fewer joins

---

## Laravel Real Example

### Normalized
```text
users → id, name
orders → id, user_id
```

### Denormalized
```text
orders → id, user_id, user_name
```

---

## When to Use What
Use Case  |	Choice
|---------|-------|
Frequent updates  |	Normalization
Heavy reads  |	Denormalization

---

## Interview Answer

“We normalize for data integrity and selectively denormalize for performance.”