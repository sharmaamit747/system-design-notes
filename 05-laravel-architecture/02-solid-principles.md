# SOLID Principles in Laravel

SOLID makes your app:
- Scalable
- Testable
- Maintainable

---

## S – Single Responsibility
One class → One reason to change

❌ UserController handles payments
✅ PaymentService handles payments

---

## O – Open/Closed
Open for extension, closed for modification

Example:
```php
interface PaymentGateway {
    public function pay();
}
```
Add Razorpay, Stripe without touching old code.

## L – Liskov Substitution
Child class should replace parent without breaking logic.

Laravel example:
- Custom guards
- Custom cache drivers

## I – Interface Segregation

Small interfaces > fat interfaces

❌ One giant interface
✅ Multiple small contracts

## D – Dependency Inversion

Depend on abstractions, not concrete classes

```php
public function __construct(PaymentGateway $gateway) {}
```

## Golden line

“SOLID helps us avoid tightly coupled systems.”