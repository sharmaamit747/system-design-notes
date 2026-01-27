# Database Indexing (Performance Booster)

## What is Indexing?
Indexing is like a **book index**.

Without index → scan every row  
With index → jump directly to data

---

## Example Without Index
```sql
SELECT * FROM users WHERE email = 'test@example.com';
Database checks every row.

Example With Index
CREATE INDEX idx_users_email ON users(email);
Database jumps directly → fast query 🚀

Types of Indexes
1️⃣ Single Column Index
INDEX (email)
2️⃣ Composite Index
INDEX (user_id, status)
Order matters ❗

Laravel Example
Schema::table('orders', function (Blueprint $table) {
    $table->index(['user_id', 'status']);
});
Common Mistake (Interview Favorite)
❌ Too many indexes
❌ Index on low-cardinality columns (gender, status)

Tech Lead Rule
Index columns used in WHERE, JOIN, ORDER BY

Interview Line
“Indexes speed up reads but slow down writes, so we index carefully.”