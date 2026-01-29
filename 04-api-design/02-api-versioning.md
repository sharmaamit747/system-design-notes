# API Versioning

## Why Version APIs?
APIs are **contracts**.

Breaking changes can:
- Break mobile apps
- Break frontend
- Break integrations

---

## Common Versioning Methods

### 1️⃣ URL Versioning
```http
/api/v1/users
/api/v2/users
```

### 2️⃣ Header Versioning
```http
Accept: application/vnd.app.v1+json
```

### Laravel Example

```php
Route::prefix('v1')->group(function () {
    Route::get('/users', [UserController::class, 'index']);
});
```

## Best Practice

- Keep old versions alive
- Deprecate slowly
- Communicate changes