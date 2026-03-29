# Stored Procedures

- These are basically functions that you can save instead of having to write sql code again
    - Saves the sql code to a procedure to be executed once again
- Pros
    - Reduces network traffic
    - Increases performance
    - Secure (admin is able to set privileges)
- Cons
    - Increases memory usage for every connection

**Creating a new procedure (no arguments)**

- New delimiter is required to set since the sql query inside the procedure uses the default delimiter

```sql
DELIMITER <new-delimiter>
CREATE PROCEDURE <procedure-name>()
BEGIN
    <sql-query>;
END <new-delimiter>
DELIMITER ;
```

**Creating a new procedure (with paramter)**
```sql
CREATE PROCEDURE <procedure-name>(IN <paramter-name> <parameter-data-type>)
BEGIN
    <sql-query>;
END
```

**Calling a stored procedure**
```sql
CALL <procedure-name>();
```

**Deleting a stored procedure**
```sql
DROP PROCEDURE <procedure-name>;
```
