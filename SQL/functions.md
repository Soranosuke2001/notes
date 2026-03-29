# Functions

- Functions are the same as any other functions in other programming languages
    - Takes in parameters and returns some value
- There are tons of built in functions

## `COUNT` Function

- Returns the number of rows for a specific column

**Getting total row count**
```sql
SELECT COUNT(<column-name>)
FROM <table-name>;
```

**Getting total row count with a condition**
```sql
SELECT COUNT(<column-name>)
FROM <table-name>
WHERE <column-name> <operator> <value>;
```

**Getting total row count and changing the header name**
```sql
SELECT COUNT(<column-name>) AS "<alias>"
FROM <table-name>;
```


## `CONCAT` Function

- Takes 2 or more columns and concats the values together

**Combining 2 columns together into a new column**
```sql
SELECT CONCAT(<column1-name>, <column2-name>) AS <new-column-name>
FROM <table-name>;
```

**Combining 2 columns together into a new column and adding a space in between**
```sql
SELECT CONCAT(<column1-name>, " ", <column2-name>) AS <new-column-name>
FROM <table-name>;
```
