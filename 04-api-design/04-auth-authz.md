# Authentication vs Authorization

## Authentication (AuthN)
Who are you?

Example:
- Login
- Token validation

---

## Authorization (AuthZ)
What can you do?

Example:
- Admin access
- Permission checks

---

## Laravel Tools
- Sanctum (API tokens)
- Policies
- Gates
- Middleware

---

## Sanctum Example
```php
$user->createToken('api-token')->plainTextToken;
```

## Authorization Example
```php
$this->authorize('update', $post);
```

## Golden Answer
“Authentication verifies identity, authorization verifies permissions.”