# Column Constraints

You can add constraints on columns (this is something else from setting the data type)


## `UNIQUE` Constraint

`UNIQUE` will ensure that all values in the column do not overlap (unique) from one another

**Setting the unique constraint on table creation**
```sql
CREATE TABLE <table-name> (
    <column1-name> <data-type> UNIQUE
);
```

**Updating a column to set the unique constraint**
```sql
ALTER TABLE <table-name>
ADD CONSTRAINT
UNIQUE(<column-name>);
```


## `NOT NULL` Constraint

`NOT NULL` will ensure that the calumn value cannot be NULL

**Setting the not null constraint on table creation**
```sql
CREATE TABLE <table-name> (
    <column-name> <data-type> NOT NULL
);
```

**Updating a column to set the unique constraint**
```sql
ALTER TABLE <table-name>
MODIFY <column-name> <data-type> NOT NULL;
```


## `CHECK` Constraint

`CHECK` constraint will ensure that the value entered for a specific column meets a certain condition

**Setting a check constraint on table creation**
```sql
CREATE TABLE <table-name> (
    <column1-name> <data-type>,
    CONSTRAINT <check-name> CHECK (<column-name> <operator> <value>)
);
```

**Updating a column to set the check constraint**
```sql
ALTER TABLE <table-name>
ADD CONSTRAINT <check-name> CHECK(<column-name> <operator> <value>);
```

**Removing a check constraint**
```sql
ALTER TABLE <table-name>
DROP CHECK <check-name>
```


## `DEFAULT` Constraint

If the value is not entered for a column we can set a default value

**Setting a default constraint on table creation**
```sql
CREATE TABLE <table-name> (
    <column-name> <data-type> DEFAULT <value>
);
```

**Updating a column to set the default constraint**
```sql
ALTER TABLE <table-name>
ALTER <column-name> SET DEFAULT <value>;
```


## `PRIMARY KEY` Constraint

`PRIMARY KEY` constraint will ensure that the value for the column is not null and unique
    - For each table, there can only be a single primary key constraint

**Setting a primary key constraint on table creation**
```sql
CREATE TABLE <table-name> (
    <column-name> <data-type> PRIMARY KEY
);
```

**Updating a column to set the primary key constraint**
```sql
ALTER TABLE <table-name>
ADD CONSTRAINT
PRIMARY KEY(<column-name>);
```


## `FOREIGN KEY` Constraint

`FOREIGN KEY` constraint allows us to connect one table to another using the other tables primary key
    - The primary key must be created before creating the foreign key

**Setting a foreign key constraint on table creation**
```sql
CREATE TABLE <table-name> (
    <column-name> <data-type>,
    FOREIGN KEY <column-name> REFERENCES <table-name>(<column-name>)
);
```

**Updating a column to set the foreign key constraint**
```sql
ALTER TABLE <table-name>
ADD CONSTRAINT <foreign_key_name>
FOREIGN KEY (<column_name>) REFERENCES <table-name>(<column-name>);
```

**Deleting the foreign key constraint**
```sql
ALTER TABLE <table-name>
DROP FOREIGN KEY <foreign-key-name>;
```








