# `DELETE` Commands

**Deleting all rows in a table**
```sql
DELETE FROM <table-name>;
```

**Deleting a specific row**
```sql
DELETE FROM <table-name>
WHERE <column-name> <operator> <value>;
```

**Setting the foreign key to NULL on delete (table creation)**
```sql
CREATE TABLE <table-name> (
    <column1-name> <data-type>,
    <column2-name> <data-type>,
    ...,
    FOREIGN KEY <column-name> REFERENCES <table-name>(<column-name>)
    ON DELETE SET NULL
);
```

**Setting the foreign key to NULL on delete (table creation)**
```sql
ALTER TABLE <table-name> DROP FOREIGN KEY <foreign_key_name>;

ALTER TABLE <table-name>
ADD CONSTRAINT <foreign_key_name>
FOREIGN KEY(<column-name>) REFERENCES <table-name>(<column-name>)
ON DELETE SET NULL;
```

**Deleting the foreign key row on delete**
```sql
ALTER TABLE <table-name> DROP FOREIGN KEY <foreign_key_name>;

ALTER TABLE <table-name>
ADD CONSTRAINT <foreign_key_name>
FOREIGN KEY(<column-name>) REFERENCES <table-name>(<column-name>)
ON DELETE CASCADE;
```
