# Managing SQL performance

[Oracle docs](https://docs.oracle.com/cd/B19306_01/server.102/b14211/ex_plan.htm#i3305)

## Indexes:

Indexes speed up look ups (aka SELECTs) but slow modification actions.

By default, the CREATE INDEX statement creates a __btree__ index. [Indexes reference 1](https://www.sqlshack.com/what-is-the-difference-between-clustered-and-non-clustered-indexes-in-sql-server/). [Indexes reference 2](https://www.oracletutorial.com/oracle-index/oracle-create-index/)

### Adding Index to table:
```sql
CREATE INDEX index_name 
ON table_name(column1[,column2,...])
```

> index name should follow the `<table_name>_<column_name>_I` convention.

### Removing Index from table:
```sql
DROP INDEX index_name;
```

## Oracle Explain Plan
