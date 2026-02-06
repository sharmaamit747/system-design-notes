# API Contract Design

## What is API Contract?
Agreement between backend & client.

---

## Example: Create Order API

### Request
```http
POST /api/v1/orders
```
```json
{
  "product_id": 1,
  "quantity": 2,
  "payment_method": "card"
}
```
### Response

```json
{
  "order_id": 101,
  "status": "PENDING"
}
```
### Error Handling
```json
{
  "error": "OUT_OF_STOCK"
}
```
### Best Practices

- Version APIs
- Use standard HTTP codes
- Consistent response format

“API contracts prevent breaking frontend and mobile apps.”