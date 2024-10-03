

# 1. **Basic Connection and Navigation**
- **Connect to a database:**
  ```bash
  psql -d database_name
  ```
- **List databases:**
  ```bash
  \l
  ```
  or
  ```bash
  \list
  ```
- **List tables:**
  ```bash
  \dt
  ```
- **List schemas:**
  ```bash
  \dn
  ```
- **Show table definition:**
  ```bash
  \d table_name
  ```
- **Show all available commands:**
  ```bash
  \?
  ```

# 2. **Database Modeling and Manipulation**
- **Create database:**
  ```sql
  CREATE DATABASE database_name;
  ```
- **Create table:**
  ```sql
  CREATE TABLE table_name (
    column1 type1 [constraints],
    column2 type2 [constraints],
    ...
  );
  ```
- **Add a column to an existing table:**
  ```sql
  ALTER TABLE table_name ADD COLUMN column_name type;
  ```
- **Remove a column:**
  ```sql
  ALTER TABLE table_name DROP COLUMN column_name;
  ```
- **Create an index:**
  ```sql
  CREATE INDEX index_name ON table_name (column);
  ```
- **Remove an index:**
  ```sql
  DROP INDEX index_name;
  ```

# 3. **Queries and CRUD Operations**
- **Insert data:**
  ```sql
  INSERT INTO table_name (column1, column2) VALUES (value1, value2);
  ```
- **Query data:**
  ```sql
  SELECT * FROM table_name;
  ```
- **Update data:**
  ```sql
  UPDATE table_name SET column1 = value WHERE condition;
  ```
- **Delete data:**
  ```sql
  DELETE FROM table_name WHERE condition;
  ```

# 4. **Transaction Commands**
- **Begin a transaction:**
  ```sql
  BEGIN;
  ```
- **Commit a transaction:**
  ```sql
  COMMIT;
  ```
- **Rollback a transaction:**
  ```sql
  ROLLBACK;
  ```

# 5. **User and Permission Administration**
- **Create a user:**
  ```sql
  CREATE USER username WITH PASSWORD 'password';
  ```
- **Grant permissions to a user:**
  ```sql
  GRANT ALL PRIVILEGES ON TABLE table_name TO username;
  ```
- **Revoke permissions:**
  ```sql
  REVOKE ALL PRIVILEGES ON TABLE table_name FROM username;
  ```

# 6. **Navigation and Object Information**
- **List functions:**
  ```bash
  \df
  ```
- **Show function definition:**
  ```bash
  \sf function_name
  ```
- **Show environment variables:**
  ```bash
  \set
  ```

# 7. **Utilities**
- **Exit psql:**
  ```bash
  \q
  ```
- **Execute SQL commands from a file:**
  ```bash
  \i file_path.sql
  ```

# 8. Backup
To perform a complete backup of a database in SQL format, including both the schema (table structure, indexes, schemas, etc.) and all the data, you can use the **pg_dump** command.

Here is the basic command for that:

```bash
pg_dump -U username -d database_name -F p -f backup.sql
```

## Explanation of parameters:
- **-U username**: Specifies the user to be used for the backup.
- **-d database_name**: Specifies the database to be copied.
- **-F p**: Indicates that the output file format will be plain text (p = plain), which is a readable SQL format.
- **-f backup.sql**: Specifies the name of the output file where the backup will be saved (in this example, `backup.sql`).

### Additional options:
- **--clean**: Includes instructions to remove (DROP) existing objects before recreating them. This can be useful when restoring a backup to ensure no duplicate objects.
  ```bash
  pg_dump -U username -d database_name -F p --clean -f backup.sql
  ```
- **--create**: Includes the `CREATE DATABASE` command in the backup, so that it recreates the database automatically during the restore process.
  ```bash
  pg_dump -U username -d database_name -F p --create -f backup.sql
  ```

### Complete example with all data and structure:
```bash
pg_dump -U username -d database_name -F p --clean --create -f full_backup.sql
```

This command will generate a complete SQL file with all the instructions needed to recreate the database, including the schema, tables, and data.

### Restore the backup:
To restore the generated backup, you can use **psql**:
```bash
psql -U username -d database_name -f full_backup.sql
```

If the database does not exist and you used the `--create` option, you can run it directly:
```bash
psql -U username -f full_backup.sql
```

This will restore both the schema and data to the database.