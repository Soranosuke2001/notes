# `MODIFY` Commands

**Changing the data type of a column**
```sql
ALTER TABLE <table-name> 
MODIFY COLUMN <column-name> <new-data-type>;
```

**Changing the order of columns (after a specific column)**
```sql
ALTER TABLE <table-name> 
MODIFY <column-name> <data-type>
AFTER <column-name>;
```

**Changing the order of columns (first column)**
```sql
ALTER TABLE <table-name> 
MODIFY <column-name> <data-type>
FIRST;
```
