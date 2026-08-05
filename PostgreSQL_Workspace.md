# PostgreSQL Workspace

## Website References

| SNO | Topic | Website |
| :---: | :--- | :--- |

---

## Postgres SQL Query References

```sql
-- list databases
SELECT datname FROM pg_database;
```

```sql
-- list tables
SELECT table_name 
FROM information_schema.tables 
WHERE table_schema = 'public';
```

```sql
-- list all columns 
SELECT 
    column_name, 
    data_type, 
    character_maximum_length, 
    is_nullable
FROM 
    information_schema.columns
WHERE 
    table_name = 'departments'
ORDER BY 
    ordinal_position;
```

```sql
-- create a user role with Admin priviliges (shorthand)
CREATE ROLE AdminUser
WITH LOGIN
SUPERUSER
PASSWORD 'Admin@123';
```

```sql
-- check if an index exist, returns bool
SELECT EXISTS (
    SELECT 1 
    FROM pg_class c
    JOIN pg_namespace n ON n.oid = c.relnamespace
    WHERE c.relname = 'index name'
      AND n.nspname = 'public' -- Change to your schema name if different
      AND c.relkind = 'i'
) AS Index_Exists;
```

