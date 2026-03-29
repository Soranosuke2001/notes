# `ORDER BY` Commands

`ORDER BY` will return the result in a sorted order for the specified column
    - Ascending order is returned by defualt
    - Specify more than 1 column to order by (priority goes from left to right)

**Getting all records sorted by a specific column**
```sql
SELECT * FROM <table-name>
ORDER BY <column-name>;
```

**Getting all records sorted by a specific column (descending order)**
```sql
SELECT * FROM <table-name>
ORDER BY <column-name> DESC;
```

**Getting all records sorted by a specific column (multiple columns)**
```sql
SELECT * FROM <table-name>
ORDER BY <column1-name>, <column2-name> ...;
```
