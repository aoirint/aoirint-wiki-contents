---
title: PostgreSQL
description: 
published: true
date: 2022-02-06T00:38:52.444Z
tags: 
editor: markdown
dateCreated: 2022-02-06T00:36:47.292Z
---

# ユーザ（ロール）のパスワード変更（PostgreSQL 13）

```shell
psql --user myuser postgres
```

```sql
ALTER ROLE myuser WITH PASSWORD 'new_password';
```

- <https://www.postgresql.jp/document/13/html/sql-alterrole.html>
- <https://www.postgresql.org/docs/13/sql-alterrole.html>
- <https://stackoverflow.com/questions/12720967/how-to-change-postgresql-user-password>

# データベースの名前変更（PostgreSQL 13）

```shell
psql --user myuser postgres
```

```sql
ALTER DATABASE mydatabase RENAME TO new_mydatabase;
```

- <https://www.postgresql.jp/document/13/html/sql-alterdatabase.html>
- <https://www.postgresql.org/docs/13/sql-alterdatabase.html>
- <https://www.postgresqltutorial.com/postgresql-rename-database/>

