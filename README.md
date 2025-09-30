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

### UNIQUE and NOT NULL | Travel Tracker Part 1

### INSERT and add Data | Travel Tracker Part 2

### Tavel Tracker Part 3

### One to One Relationship and Inner Joins

### One to Many Relationships

### The Family Travel Tracker

### How to UNDATE and DELETE Data and Tables

### Permalist Project
