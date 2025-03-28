---
description: 'System table showing which privileges are granted to ClickHouse user
  accounts.'
keywords: ['system table', 'grants']
slug: /operations/system-tables/grants
title: 'system.grants'
---

Privileges granted to ClickHouse user accounts.

Columns:
- `user_name` ([Nullable](../../sql-reference/data-types/nullable.md)([String](../../sql-reference/data-types/string.md))) — User name.

- `role_name` ([Nullable](../../sql-reference/data-types/nullable.md)([String](../../sql-reference/data-types/string.md))) — Role assigned to user account.

- `access_type` ([Enum8](../../sql-reference/data-types/enum.md)) — Access parameters for ClickHouse user account.

- `database` ([Nullable](../../sql-reference/data-types/nullable.md)([String](../../sql-reference/data-types/string.md))) — Name of a database.

- `table` ([Nullable](../../sql-reference/data-types/nullable.md)([String](../../sql-reference/data-types/string.md))) — Name of a table.

- `column` ([Nullable](../../sql-reference/data-types/nullable.md)([String](../../sql-reference/data-types/string.md))) — Name of a column to which access is granted.

- `is_partial_revoke` ([UInt8](/sql-reference/data-types/int-uint#integer-ranges)) — Logical value. It shows whether some privileges have been revoked. Possible values:
- `0` — The row describes a grant.
- `1` — The row describes a partial revoke.

- `grant_option` ([UInt8](/sql-reference/data-types/int-uint#integer-ranges)) — Permission is granted `WITH GRANT OPTION`, see [GRANT](../../sql-reference/statements/grant.md#granting-privilege-syntax).
