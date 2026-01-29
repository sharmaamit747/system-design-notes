# Service & Repository Pattern

## Problem
Controllers become fat and untestable.

---

## Repository
Handles data access.

```php
class OrderRepository {
    public function create(array $data) {
        return Order::create($data);
    }
}
```
---

## Service
Handles business logic.

```php
class OrderService {
    public function __construct(
        private OrderRepository $repo
    ) {}

    public function placeOrder($data) {
        // validation
        // calculations
        return $this->repo->create($data);
    }
}
```

---

## Controller

```php
class OrderController {
    public function store(Request $r) {
        $this->service->placeOrder($r->all());
    }
}
```

---

## Benefits
- Clean controllers
- Testable logic
- Easy refactor

“Service handles business logic, repository handles data.”