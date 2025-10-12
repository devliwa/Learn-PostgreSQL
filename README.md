# Learn-PostgreSQL

### use pgAdmin to CREATE a Table
```sql
CREATE TABLE capitals (
id SERIAL PRIMARY KEY,
country VARCHAR(45),
capital VARCHAR(45)
);
```

### READ data from a Postgres database
```js
import pg from "pg";

const db = new pg.Client({
  user: "pstgres",
  host: "localhost",
  database: "world",
  password: "123456",
  port: 5432,
});
db.connect();

db.query("SELECT * FROM capitals", (err, res) => {
   if (err) {
    console.error("Error executing query", err.stack);
   }
   else {
   quiz = res.row;
   }

   db.end();
 });
```


### Query data using SELECT, WHERE, and LIKE
```sql
CREATE TABLE world_food (
id SERIAL PRIMARY KEY,
country VARCHAR(45),
rice_production FLOAT,
wheat_production FLOAT
);
```
Select All
```sql
SELECT * FROM <TABLE>;

SELECT * FROM world_food;
```
Select Column
```sql
SELECT <COLUMN> FROM <TABLE>;

SELECT * FROM world_food;

SELECT country FROM world_food;
```
Select Multi-Column
```sql
SELECT <COLUMN>, <COLUMN> FROM <TABLE>;

SELECT country, wheat_production FROM world_food;
```
Where Equals(>, <, >=, <=)
```sql
SELECT <COLUMN> FROM <TABLE> WHERE <CONDITION>;

SELECT rice_production FROM world_food WHERE country = 'United States';

SELECT country FROM world_food WHERE wheat_production > 20;
```

### UNIQUE and NOT NULL | Travel Tracker Part 1

### INSERT and add Data | Travel Tracker Part 2

### Tavel Tracker Part 3

### One to One Relationship and Inner Joins

### One to Many Relationships

### The Family Travel Tracker

### How to UNDATE and DELETE Data and Tables

### Permalist Project
