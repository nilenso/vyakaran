# Migrations

## MIGRATION

### The database flavours:

* RDBMS
* document
* object

### The shape of a migration

\[tbd\]

### Timelines

* schema is always mutable \(datamic an exception\)

### Complicated migrations

#### Small example \(datatype, MySQL version fix, and default data\):

## +BEGIN\_SRC

-- fix the MODIFIED column so it defaults to a sensible value

* -- \(this column is deprecated but still fails when the defaults are used in inserts\)
* ALTER TABLE merchants MODIFY COLUMN MODIFIED timestamp NOT NULL DEFAULT CURRENT\_TIMESTAMP;
* -- \(this column is deprecated but still fails when the old string defaults are used in inserts\)
* ALTER TABLE merchants MODIFY COLUMN MODIFIED timestamp NULL;

  UPDATE merchants SET MODIFIED = CREATED where MODIFIED = '0000-00-00 00:00:00';

  **+END\_SRC**

#### Big example:

\[tbd\]

#### Non-schema modification

## +BEGIN\_SRC

INSERT INTO roles \(id, name, created\_at, updated\_at\) VALUES \(1, 'ADMIN', now\(\), now\(\)\) ON DUPLICATE KEY UPDATE id=1;

-- a sample of schema data formatting changes ALTER TABLE merchants CONVERT TO CHARACTER SET utf8 COLLATE utf8\_general\_ci;

## +END\_SRC

