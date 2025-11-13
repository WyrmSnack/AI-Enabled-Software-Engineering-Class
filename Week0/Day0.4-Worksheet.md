# Day 0.4 Worksheet: Databases & SQL

**Estimated Time**: 1–2 hours  
**Focus**: Understanding relational databases, tables, and SQL queries

---

## Learning Objectives

By the end of this session, you will be able to:
- Understand relational databases (tables ↔ rows ↔ columns)
- Learn how SQL retrieves data
- Practice SELECT, WHERE, and JOIN queries
- Complete SQLBolt Lessons 1–6

---

## Pre-Activity: What is a Database?

**Think about data storage**:

Imagine you need to store information about students in a class:
- Name
- Email
- Grade
- Enrollment date

**How would you organize this in a spreadsheet?**
- Draw or describe your structure:

_______________________________________________________________________
_______________________________________________________________________

**A database table is similar to a spreadsheet**:
- **Table** = The whole spreadsheet
- **Row** = One student's information
- **Column** = One type of information (name, email, etc.)

---

## Activity 1: Understanding Relational Databases

**Key Concepts**:

| Term | Definition | Real-World Analogy |
|------|------------|-------------------|
| Database | | A filing cabinet |
| Table | | A folder in the cabinet |
| Row (Record) | | A single document |
| Column (Field) | | A specific piece of information |
| Primary Key | | A unique identifier (like a student ID) |
| Foreign Key | | A reference to another table |

**Example Table: `students`**

| student_id | name | email | grade |
|------------|------|-------|-------|
| 1 | Alice | alice@example.com | A |
| 2 | Bob | bob@example.com | B |
| 3 | Charlie | charlie@example.com | A |

**Questions**:
1. How many rows are in this table? _______
2. How many columns? _______
3. What is the primary key? _______

---

## Activity 2: SQLBolt Tutorial — Lessons 1–6

**Resource**: [SQLBolt](https://sqlbolt.com/)

**Instructions**: Complete Lessons 1–6. Take notes as you go.

### Lesson 1: SELECT queries

**Key concept**: `SELECT` retrieves data from a table

**Example**:
```sql
SELECT column1, column2 
FROM table_name;
```

**Practice**: Write a query to select all columns from a table called `movies`:
```sql

```

**Notes**:
_______________________________________________________________________

### Lesson 2: Queries with constraints (WHERE)

**Key concept**: `WHERE` filters rows based on conditions

**Example**:
```sql
SELECT * FROM movies 
WHERE year > 2000;
```

**Practice**: Write a query to find movies with a rating above 8:
```sql

```

**Notes**:
_______________________________________________________________________

### Lesson 3: Queries with constraints (Pt. 2)

**Key operators**: `AND`, `OR`, `IN`, `LIKE`, `IS NULL`

**Practice**: Write a query to find movies released in 2000 OR 2010:
```sql

```

**Notes**:
_______________________________________________________________________

### Lesson 4: Filtering and sorting

**Key concepts**: `DISTINCT`, `ORDER BY`, `LIMIT`

**Example**:
```sql
SELECT DISTINCT director 
FROM movies 
ORDER BY director ASC 
LIMIT 10;
```

**Practice**: Write a query to get the top 5 highest-rated movies:
```sql

```

**Notes**:
_______________________________________________________________________

### Lesson 5: Simple SELECT queries

**Review**: Combine what you've learned

**Practice exercise**: Write a query that:
- Selects movies from the 2000s
- Orders them by rating (highest first)
- Limits to 10 results

```sql

```

**Notes**:
_______________________________________________________________________

### Lesson 6: Multi-table queries with JOINs

**Key concept**: `JOIN` combines data from multiple tables

**Example**:
```sql
SELECT movies.title, boxoffice.domestic_sales
FROM movies
JOIN boxoffice ON movies.id = boxoffice.movie_id;
```

**Visual representation**:
```
Table: movies          Table: boxoffice
id | title            movie_id | domestic_sales
1  | Toy Story        1        | 191796233
2  | Monsters Inc     2        | 162798565
```

**Practice**: Write a query to join `movies` and `boxoffice` tables:
```sql

```

**Notes**:
_______________________________________________________________________

---

## Activity 3: SQL Concepts Practice

**Fill in the blanks**:

1. To get all data from a table, use: `SELECT _____ FROM table_name;`
2. To filter rows, use the _____ clause
3. To combine tables, use a _____
4. To sort results, use _____ BY
5. To limit results, use _____

**Answers**:
1. _______
2. _______
3. _______
4. _______
5. _______

---

## Activity 4: Real-World Scenario

**Scenario**: You work for a bookstore and need to query the database.

**Tables**:
- `books` (id, title, author, price, category)
- `customers` (id, name, email)
- `orders` (id, customer_id, book_id, order_date)

**Write SQL queries for**:

1. **Find all books in the "Fiction" category**:
```sql

```

2. **Find books priced under $20, ordered by price**:
```sql

```

3. **Find all orders for a specific customer (customer_id = 5)**:
```sql

```

4. **Find customers who ordered a specific book (book_id = 10)**:
```sql

```

---

## Activity 5: Understanding JOINs

**Types of JOINs**:

| JOIN Type | What It Does | When to Use |
|-----------|--------------|-------------|
| INNER JOIN | Returns only matching rows | When you need data that exists in both tables |
| LEFT JOIN | Returns all rows from left table + matching from right | When you want all records from one table |
| RIGHT JOIN | Returns all rows from right table + matching from left | Less common, similar to LEFT JOIN |

**Visual Example**:

**Table A** (students)     **Table B** (enrollments)
| id | name |        | student_id | course |
|----|------|        |------------|--------|
| 1  | Alice|        | 1          | Math   |
| 2  | Bob  |        | 1          | Science|
| 3  | Charlie|      | 3          | Math   |

**INNER JOIN** (only students with enrollments):
```sql
SELECT students.name, enrollments.course
FROM students
INNER JOIN enrollments ON students.id = enrollments.student_id;
```

**Result**: Alice (Math), Alice (Science), Charlie (Math)

**LEFT JOIN** (all students, even without enrollments):
```sql
SELECT students.name, enrollments.course
FROM students
LEFT JOIN enrollments ON students.id = enrollments.student_id;
```

**Result**: Alice (Math), Alice (Science), Bob (NULL), Charlie (Math)

---

## Activity 6: Optional — SQLite Browser

**If you want to practice locally**:

1. Download [DB Browser for SQLite](https://sqlitebrowser.org/)
2. Create a new database
3. Create a table:
```sql
CREATE TABLE students (
    id INTEGER PRIMARY KEY,
    name TEXT,
    email TEXT,
    grade TEXT
);
```

4. Insert some data:
```sql
INSERT INTO students (name, email, grade) 
VALUES ('Alice', 'alice@example.com', 'A');
```

5. Query your data:
```sql
SELECT * FROM students;
```

**Did you try SQLite Browser?** [ ] Yes [ ] No

---

## Deliverable Checklist

- [ ] Completed SQLBolt Lesson 1 (SELECT queries)
- [ ] Completed SQLBolt Lesson 2 (WHERE constraints)
- [ ] Completed SQLBolt Lesson 3 (More constraints)
- [ ] Completed SQLBolt Lesson 4 (Filtering and sorting)
- [ ] Completed SQLBolt Lesson 5 (Simple SELECT review)
- [ ] Completed SQLBolt Lesson 6 (JOINs)
- [ ] Took screenshot of completed SQLBolt lesson (showing "Lesson complete!")
- [ ] (Optional) Installed and tried SQLite Browser
- [ ] Saved screenshot as `Day0.4-SQLBolt-Screenshot.png` in Week0 folder

---

## Reflection Questions

1. **How does SQL differ from programming languages like Python?**
   _______________________________________________________________________
   _______________________________________________________________________

2. **What was the most challenging SQL concept?**
   _______________________________________________________________________

3. **When would you use a JOIN in a real application?**
   _______________________________________________________________________

4. **What questions do you still have about databases?**
   _______________________________________________________________________

---

## SQL Cheat Sheet

**Basic SELECT**:
```sql
SELECT column1, column2 FROM table_name;
SELECT * FROM table_name;  -- Get all columns
```

**Filtering**:
```sql
SELECT * FROM table_name WHERE condition;
SELECT * FROM table_name WHERE column > 10;
SELECT * FROM table_name WHERE column IN ('value1', 'value2');
```

**Sorting and Limiting**:
```sql
SELECT * FROM table_name ORDER BY column ASC;
SELECT * FROM table_name ORDER BY column DESC;
SELECT * FROM table_name LIMIT 10;
```

**JOINs**:
```sql
SELECT t1.column, t2.column
FROM table1 t1
JOIN table2 t2 ON t1.id = t2.foreign_id;
```

---

## Additional Resources (Optional)

- [SQLBolt — Complete Tutorial](https://sqlbolt.com/)
- [W3Schools SQL Tutorial](https://www.w3schools.com/sql/)
- [SQLite Tutorial](https://www.sqlitetutorial.net/)

---

## Troubleshooting

**Common Issues**:

- **Syntax errors**: Check for missing commas, quotes, or semicolons
- **"Table doesn't exist"**: Make sure you're using the correct table name
- **JOIN not working**: Verify the column names match between tables

**Error you encountered?** Note it here:
_______________________________________________________________________
_______________________________________________________________________

---

## Next Steps

Tomorrow (Day 0.5), you'll learn about web foundations and APIs. Make sure you have:
- Python installed (from Day 0.3)
- The `requests` library installed: `pip install requests` or `pip3 install requests`

