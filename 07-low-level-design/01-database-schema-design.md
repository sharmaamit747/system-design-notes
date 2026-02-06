# Database Schema Design (LLD)

## Example: Orders Table

```sql
CREATE TABLE orders (
  id BIGINT PRIMARY KEY,
  user_id BIGINT INDEX,
  status VARCHAR(20),
  total_amount DECIMAL(10,2),
  created_at TIMESTAMP
);
```
### Design Decisions

- BIGINT for scale
- Indexed foreign keys
- Enum-like status

## Order Items Table
```sql
order_items
- id
- order_id (index)
- product_id
- price
- quantity
```

“Schema design should match access patterns.”