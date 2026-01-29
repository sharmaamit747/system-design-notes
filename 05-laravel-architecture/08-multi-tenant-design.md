# Multi-Tenant Architecture

## What is Multi-Tenancy?
One application → multiple customers.

---

## Types
1️⃣ Database per tenant  
2️⃣ Schema per tenant  
3️⃣ Single DB with tenant_id

---

## Laravel Example
```php
Order::where('tenant_id', auth()->user()->tenant_id);
```

---

## Use Case

SaaS apps, CRM, ERP.

“Tenant isolation is key for data security.”