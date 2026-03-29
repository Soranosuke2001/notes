# Logical Operators

## `AND` Operation

**Getting rows with multiple conditions (all conditions must be true)**
```sql
SELECT * FROM <table-name>
WHERE <column-name> <operator> <value> AND <column-name> <operator> <value>;
```

## `OR` Operation

**Getting rows with multiple conditions (any of the conditions are true)**
```sql
SELECT * FROM <table-name>
WHERE <column-name> <operator> <value> OR <column-name> <operator> <value>;
```

## `NOT` Operation

**Getting rows that do not match the condition**
```sql
SELECT * FROM <table-name>
WHERE NOT <column-name> <operator> <value> OR <column-name> <operator> <value>;
```

## `BETWEEN` Operation

**Getting rows that are within a range of values**
```sql
SELECT * FROM <table-name>
WHERE <column-name> BETWEEN <value1> AND <value2>;
```

## `IN` Operation

**Getting rows that have the value in a specific set of values**
```sql
SELECT * FROM <table-name>
WHERE <column-name> IN (<valu1>, <value2>, ...);
```
