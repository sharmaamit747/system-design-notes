# MVC Architecture in Laravel

## What is MVC?
MVC = Model + View + Controller

Laravel follows MVC but adds **Service, Events, Jobs, Policies** on top.

---

## Role Breakdown

### Model
- Represents data
- Talks to database
- Contains relationships

```php
class Order extends Model {
    public function user() {
        return $this->belongsTo(User::class);
    }
}
```
### Controller
- Handles HTTP request
- Delegates work (should be thin)

#### ❌ Bad Controller

```php
public function store(Request $r) {
    // validation
    // business logic
    // db logic
}
```

#### ✅ Good Controller

```php
public function store(StoreOrderRequest $request) {
    $this->orderService->create($request->validated());
}
```

### View

- Presentation only
- Blade / API JSON