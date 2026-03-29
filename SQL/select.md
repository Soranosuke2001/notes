# `SELECT` Commands

**Selecting all columns from a table**
```sql
SELECT * FROM <table-name>;
```

**Selecting specific columns from a table**
```sql
SELECT <column1-name>, <column2-name>
FROM <table-name>;
```

**Selecting specific data (filtering)**
```sql
SELECT *
FROM <table-name>
WHERE <column-name> <operator> <value>;
```

**Finding specific data with null values**
```sql
SELECT *
FROM <table-name>
WHERE <column-name> IS NULL;
```

**Subquery (query within another query)**

- The subquery doesnt have to be limited to select statements (only as an example)
    - The query below is calculating the average pay of all the employees and returning that value

```sql
SELECT first_name, last_name
FROM customers
WHERE customer_id IN
    (
        SELECT DISTINCT customer_id
        FROM transactions
        WHERE customer_id IS NOT NULL
    );
```

