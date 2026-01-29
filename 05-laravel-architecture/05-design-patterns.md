# Design Patterns in Laravel

## Singleton
Laravel Service Container

```php
app()->singleton(PaymentService::class);
```

### Used for:
- Config
- Cache
- Logger

---

## Factory

Model factories

```php
User::factory()->create();
```

### Used for:
- Testing
- Seeding

---

## Repository

Data abstraction layer.

--- 

## Observer

Model events
```php
User::created(fn () => SendWelcomeEmail::dispatch());
```

---

## Strategy

Multiple payment gateways.

---

## Facade

Static-like access to services.
```php
Cache::get('key');
```

---

Laravel is pattern-driven, not magic.