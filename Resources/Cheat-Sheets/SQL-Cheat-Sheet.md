# SQL Cheat Sheet

Quick reference for SQL queries.

## SELECT
```sql
SELECT * FROM users;
SELECT name, email FROM users;
SELECT DISTINCT status FROM orders;
```

## WHERE
```sql
SELECT * FROM users WHERE age > 18;
SELECT * FROM users WHERE name LIKE 'J%';
SELECT * FROM users WHERE age BETWEEN 18 AND 65;
```

## JOIN
```sql
SELECT u.name, o.product
FROM users u
INNER JOIN orders o ON u.id = o.user_id;

SELECT u.name, o.product
FROM users u
LEFT JOIN orders o ON u.id = o.user_id;
```

## GROUP BY
```sql
SELECT status, COUNT(*) 
FROM orders 
GROUP BY status;

SELECT user_id, SUM(amount) 
FROM orders 
GROUP BY user_id;
```

## ORDER BY
```sql
SELECT * FROM users ORDER BY name ASC;
SELECT * FROM users ORDER BY created_at DESC;
```

## LIMIT
```sql
SELECT * FROM users LIMIT 10;
SELECT * FROM users LIMIT 10 OFFSET 20;
```

## Aggregate Functions
```sql
SELECT COUNT(*) FROM users;
SELECT AVG(age) FROM users;
SELECT MAX(price) FROM products;
SELECT MIN(price) FROM products;
SELECT SUM(amount) FROM orders;
```

## INSERT
```sql
INSERT INTO users (name, email) VALUES ('John', 'john@example.com');
```

## UPDATE
```sql
UPDATE users SET email = 'new@example.com' WHERE id = 1;
```

## DELETE
```sql
DELETE FROM users WHERE id = 1;
```

