# Rate Limiting

## What is Rate Limiting?
Limits number of requests per user/IP.

Prevents:
- Abuse
- DDoS
- Server overload

---

## Laravel Rate Limiting
```php
Route::middleware('throttle:60,1')->group(function () {
    Route::get('/profile', fn () => auth()->user());
});
```

## Real Use Cases

- Login API
- OTP API
- Public APIs

## Rate Limit Strategies

- Per IP
- Per user
- Per token

## Golden Line

“Rate limiting protects APIs from abuse and ensures fairness.”