# Class Design in Laravel (LLD)

## Tech Lead Rule
Controllers should never contain business logic.

---

## Example: Order Placement

### Classes Involved
- OrderController
- OrderService
- OrderRepository
- PaymentService
- InventoryService
- OrderPlacedEvent

---

## Responsibility Split

### Controller
```php
class OrderController {
    public function store(StoreOrderRequest $request) {
        return $this->service->placeOrder($request->validated());
    }
}
```
### Service (Core Logic)
```php
class OrderService {
    public function placeOrder(array $data) {
        DB::transaction(function () use ($data) {
            $order = $this->repo->create($data);
            $this->payment->charge($order);
            event(new OrderPlaced($order));
        });
    }
}
```
### Repository (DB Access)
```php
class OrderRepository {
    public function create(array $data) {
        return Order::create($data);
    }
}
```
“LLD focuses on clear responsibilities and loose coupling.”