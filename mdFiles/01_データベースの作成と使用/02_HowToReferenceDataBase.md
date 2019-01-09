02\_HowToReferenceDataBase
===

## 概要

- データベースの参照方法についてまとめる。

## `SHOW DATABASES`

### 概要

- データベースの一覧を表示する。
- デフォルトで下記のデータベースが存在する。
  - `information_schema`
  - `mysql             `
  - `test              `

### 文法

`SHOW DATABASES`

### サンプル

```
MariaDB [(none)]> SHOW DATABASES;
+--------------------+
| Database           |
+--------------------+
| book_diary_db      |
| dekirusample       |
| information_schema |
| mysql              |
| performance_schema |
| phpmyadmin         |
| test               |
| testdb             |
+--------------------+
8 rows in set (0.13 sec)
```
