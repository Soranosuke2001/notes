# `JOINS` Commands

- You should imagine a ven-diagram of 2 tables
    - One on the left and another on the right
- The overlapping values will be the columns that are the same (foreign keys referencing primary keys)


## `INNER JOINS` Commands

- Only returns rows that meet the criteria
    - Any rows that do not have a connection to the other table will be ignored

**Getting all columns from both tables where foreign key and primary key are the same**
```sql
SELECT * FROM <table1-name> 
INNER JOIN <table2-name>
ON <table1-name>.<foreign-key-column-name> = <table2-name>.<primary-key-column-name>;
```

**Getting specific columns from both tables where foreign key and primary key are the same**
```sql
SELECT <column1-name>, <column2-name>, ... FROM <table1-name> 
INNER JOIN <table2-name>
ON <table1-name>.<foreign-key-column-name> = <table2-name>.<primary-key-column-name>;
```

**Joining a table on itself with alias (self join)**
```sql
SELECT <table1-alias>.<column1-name>, ..., <table2-alias>.<column1-name>,...
FROM <table1-name> AS <table1-alias>
INNER JOIN <table2-name> AS <table2-alias>
ON <table1-alias>.<column1-name> <operator> <table2-alias>.<column2-name>;
```


## `LEFT JOIN` Commands

- Returns all rows from the left side but only returns rows with a connection to the left table from the right side
    - Any rows in the right table that do not have a connection will be ignored

**Getting all columns from left table and only rows that are connected from right table**
```sql
SELECT * FROM <table1-name>
LEFT JOIN <table2-name>
ON <table1-name>.<foreign-key-column-name> = <table2-name>.<primary-key-column-name>;
```


## `RIGHT JOIN` Commands

- Returns all rows from the right side but only returns rows with a connection to the right table from the left side
    - Any rows in the left table that do not have a connection will be ignored

**Getting all columns from right table and only rows that are connected from left table**
```sql
SELECT * FROM <table1-name>
RIGHT JOIN <table2-name>
ON <table1-name>.<foreign-key-column-name> = <table2-name>.<primary-key-column-name>;
```


