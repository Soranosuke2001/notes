# Wildcards

This is used for string data types to match a specific subset

## `LIKE` Command

`LIKE` is used to search any patterns in the data

**Getting all rows where the string starts with the character `s`**
```sql
SELECT * FROM <table-name>
WHERE <column-name> LIKE "s%";
```

## `%` Wildcard

`%` represents any number of random characters

**Getting all rows where the string starts with the character `s`**
```sql
SELECT * FROM <table-name>
WHERE <column-name> LIKE "s%";
```

**Getting all rows where the string ends with the character `r`**
```sql
SELECT * FROM <table-name>
WHERE <column-name> LIKE "%r";
```

## `_` Wildcard

`_` represents a single random character

**Getting all rows where the string starts with a random character but ends with r**
```sql
SELECT * FROM <table-name>
WHERE <column-name> LIKE "_r";
```
