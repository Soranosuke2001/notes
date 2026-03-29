# `LIMIT` Commands

**Limiting the number of records fetched from a table**
```sql
SELECT * FROM <table-name>
LIMIT <max-row-count>;
```

**Setting an offset to the number of records fetched from a table**
```sql
SELECT * FROM <table-name>
LIMIT <offset>, <max-row-count>;
```
