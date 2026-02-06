# Error Handling in LLD

## Types of Errors
- Validation errors
- Business rule violations
- System failures

---

## Laravel Approach
- FormRequest validation
- Custom exceptions
- Global exception handler

---

## Example
```php
throw new InsufficientBalanceException();
```

“Errors are part of design, not afterthoughts.”