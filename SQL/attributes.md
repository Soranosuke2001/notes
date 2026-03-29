# Column Attributes

These are slightly different from constraints


## `AUTO INCREMENT` Attribute

`AUTO INCREMENT` attribute can only be set to keys
    - It will take the previous value set and increment it by 1

**Setting a auto increment attribute on table creation**
```sql
CREATE TABLE <table-name> (
    <column-name> <data-type> PRIMARY KEY AUTO_INCREMENT
);
```


