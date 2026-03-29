# Triggers

- When an event (insert, update, delete), do something before or after it

**Show all triggers**
```sql
SHOW TRIGGERS;
```

**Create a new trigger (before insert)**

- NEW keyword will let sql know if it needs to reference the old data or the new data

```sql
CREATE TRIGGER <trigger-name>
BEFORE INSERT ON <table-name>
FOR EACH ROW
SET NEW.<column-name> = (NEW.<column-name> ...);
```

**Create a new trigger (after delete)**

- NEW keyword will let sql know if it needs to reference the old data or the new data

```sql
CREATE TRIGGER <trigger-name>
AFTER DELETE ON <table-name>
FOR EACH ROW
SET NEW.<column-name> = (OLD.<column-name> ...);
```

**Delete a trigger**
```sql
DROP TRIGGER <trigger_name>;
```
