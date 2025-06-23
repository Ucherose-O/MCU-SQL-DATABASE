# MCU-SQL-DATABASE
# Marvel Cinematic Universe (MCU) SQL Database Project

This project was a fun and insightful introduction to relational databases using the **Marvel Cinematic Universe (MCU)** as the dataset.

I designed a database from scratch, modeled relationships between characters, actors, and movies, and wrote SQL queries to explore the Marvel universe in a structured, relational way.

---

##  What This Project Covers

###  1. Database Design
- Created an **Entity-Relationship Diagram (ERD)** to show how entities like `Movies`, `Characters`, `Actors`, and `Studios` are related.
- Defined **primary keys** and **foreign keys** to ensure data integrity.

### 2. SQL Query Practice
- Wrote SQL queries to:
  - List all movies released after 2015
  - Find which actors played in more than 3 MCU movies
  - Count the number of characters in each movie
  - Join `Movies` and `Studios` to show movie counts by studio
- Practiced `JOIN`, `GROUP BY`, `ORDER BY`, `COUNT()`, and subqueries

### 3. Skills Applied
- **Relational database modeling**
- **SQL syntax & logic**
- **Data retrieval and reporting**
- **Understanding one-to-many and many-to-many relationships**

---

## Tools Used
- SQLite (local database)
- DB Browser for SQLite
- SQL (standard syntax)
- Entity-Relationship Diagrams (ERD)

---

## What I Learned
- How to design a database from scratch
- How to use foreign keys to maintain clean relationships
- How to write useful SQL queries to answer real questions
- The power of relational data modeling using fun datasets like the MCU!

---

## Bonus
Want to try it yourself? You can clone the repo and open the `.db` file in DB Browser or use the schema to build your own version!

---

## Example SQL Snippet
```sql
-- Find all movies with more than 2 characters
SELECT m.title, COUNT(c.character_id) AS character_count
FROM movies m
JOIN movie_characters mc ON m.movie_id = mc.movie_id
JOIN characters c ON mc.character_id = c.character_id
GROUP BY m.title
HAVING character_count > 2;
