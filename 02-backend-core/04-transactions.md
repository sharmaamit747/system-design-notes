# Transactions & Isolation Levels

## What is a Transaction?
A transaction is a **group of queries that succeed or fail together**.

---

## Example (Money Transfer)
```php
DB::transaction(function () {
    DB::table('accounts')->decrement('balance', 100);
    DB::table('accounts')->increment('balance', 100);
});
```
If one fails → rollback

## Why Transactions Matter

- Prevent partial updates
- Ensure data consistency
- Critical for payments


---

## Isolation Levels (Simple)

Level  |  Issue Prevented
|------|-----------------|
Read Uncommitted  |	Nothing
Read Committed  |	Dirty reads
Repeatable Read  |	Non-repeatable reads
Serializable  |	All issues

---

## Laravel Default

MySQL → Repeatable Read

## Interview Line

“We use transactions for critical operations like payments to ensure atomicity.”

## Tech Lead Rule
Always use transactions for:
- Payments
- Inventory
- Wallets