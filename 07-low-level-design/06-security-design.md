# Security in Low-Level Design

## Key Areas
- Authentication
- Authorization
- Input validation
- Data exposure

---

## Laravel Tools
- Sanctum
- Policies
- Middleware
- Encryption

---

## Example
```php
$this->authorize('view', $order);
```

“Security must be enforced at multiple layers.”