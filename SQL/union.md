# `UNION` Commands

**Combining the result of two `SELECT` statements**
```sql
SELECT * FROM <table1-name>
UNION
SELECT * FROM <table2-name>;
```

**Combining the result of two `SELECT` statements (column count differs)**
```sql
SELECT <column1-name>, <column2-name>, ... FROM <table1-name>
UNION
SELECT <column1-name>, <column2-name>, ... FROM <table2-name>;
```

**Combining the result of two `SELECT` statements (returns duplicates)**
```sql
SELECT * FROM <table1-name>
UNION ALL
SELECT * FROM <table2-name>;
```
