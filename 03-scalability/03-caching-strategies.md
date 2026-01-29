# Caching Strategies (High Impact Topic)

## What is Caching?
Caching stores **frequently accessed data** in fast storage (RAM).

---

## Why Cache?
- Reduce database load
- Faster response
- Lower cost

---

## Cache Layers
1️⃣ Browser  
2️⃣ CDN  
3️⃣ Application (Redis)  
4️⃣ Database

---

## Laravel Cache Example
```php
$user = Cache::remember('user_1', 60, function () {
    return User::find(1);
});
```

## Cache Invalidation (Important)

Cache is useless if data is stale.

### Strategies:
- TTL (time based)
- Manual invalidation
- Event-based invalidation

## What to Cache?

✅ User profile
✅ Settings
❌ Payments
❌ Inventory stock

## Golden Line
“Caching improves read performance but requires proper invalidation.”