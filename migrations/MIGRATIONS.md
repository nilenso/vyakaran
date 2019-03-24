# MIGRATION

## The database flavours:
   - RDBMS
   - document
   - object

## The shape of a migration

[tbd]

## Timelines

- schema is always mutable (datamic an exception)

## Complicated migrations

### Small example (datatype, MySQL version fix, and default data):

#+BEGIN_SRC
  -- fix the MODIFIED column so it defaults to a sensible value
- -- (this column is deprecated but still fails when the defaults are used in inserts)
- ALTER TABLE merchants MODIFY COLUMN MODIFIED timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP;
+ -- (this column is deprecated but still fails when the old string defaults are used in inserts)
+ ALTER TABLE merchants MODIFY COLUMN MODIFIED timestamp NULL;
  UPDATE merchants SET MODIFIED = CREATED where MODIFIED = '0000-00-00 00:00:00';
#+END_SRC

### Big example:

[tbd]

### Non-schema modification

#+BEGIN_SRC
INSERT INTO roles (id, name, created_at, updated_at)
VALUES (1, 'ADMIN', now(), now()) ON DUPLICATE KEY UPDATE id=1;


-- a sample of schema data formatting changes
ALTER TABLE merchants CONVERT TO CHARACTER SET utf8 COLLATE utf8_general_ci;
#+END_SRC
