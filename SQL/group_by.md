# `GROUP BY` Commands

**Grouping by a specific column**
```sql
SELECT *
FROM <table-name>
GROUP BY <column-name>;
```

**Grouping by a specific column with a where clause**

- Using the WHERE clause with GROUP BY doesnt work, instead use HAVING

```sql
SELECT *
FROM <table-name>
GROUP BY <column-name
HAVING <column-name> <operator> <value>;
```

**Adding another row to show the grand total (ROLLUP)**
```sql
SELECT SUM(<column1-name>), <column2-name>, ...
FROM <table-name>
GROUP BY <column2-name> WITH ROLLUP;
```
