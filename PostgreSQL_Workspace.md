# PostgreSQL Workspace

## Website References

| SNO | Topic | Website | Tags |
| :-: | :---- | :------ | :--- |
|  -  | -     | -       | -    |

---

## Postgres SQL Query References

```PostgreSQL
-- list databases
SELECT datname FROM pg_database;
```

```PostgreSQL
-- list tables
SELECT table_name 
FROM information_schema.tables 
WHERE table_schema = 'public';
```

```PostgreSQL
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

```PostgreSQL
-- create a user role with Admin priviliges (shorthand)
CREATE ROLE AdminUser
WITH LOGIN
SUPERUSER
PASSWORD 'Admin@123';
```

```PostgreSQL
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

```PostgreSQL
-- temp variables usage
-- NOTE: Always cast the custom values to avoid errors.

SET custom.emp_id  = 1011;
SET custom.role_id = 2;

SELECT * FROM public.amazon_employees AS e
WHERE e.role_id = current_setting('custom.role_id')::Integer
    AND e.id = current_setting('custom.emp_id')::Integer;
```
