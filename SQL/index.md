# `INDEXES` Commands

- Indexes are BTrees
- Used to find values very quickly from a specific column
    - Normally searches sequentially through a column
- Update takes a lot longer, but select takes less time

**Showing the current list of indexes**
```sql
SHOW INDEXES FROM <table-name>;
```

**Create an index**
```sql
CREATE INDEX <index-name>
ON <table-name>(<column-name>);
```

**Creating a muti column index**

- Order of column matters where the priority of checking goes from left to right of the columns defined
    - Sequence order is displayed when selecting the list of indexes from a specific table
- When searching for a value without the <column1-name>, the index will not be used

```sql
CREATE INDEX <index-name>
ON <table-name>(<column1-name>, <column2-name>);
```

**Deleting an index**
```sql
ALTER TABLE <table-name>
DROP INDEX <index-name>;
```
