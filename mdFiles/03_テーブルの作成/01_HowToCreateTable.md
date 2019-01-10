01\_HowToCreateTable.md
===

## 概要

- テーブルの作成方法についてまとめる。

## `CREATE TABLE`

### 概要

- テーブルの作成を行う。
- MySQLの拡張機能として，同じ名前のテーブルが存在したときにエラーではなく警告にすることができる。
  - エラーにならなくなるだけなので，テーブルが作成されるわけではないので注意!

### 文法

`CREATE TABLE テーブル名(列名 データ型, ...)`

### データ型について

- MySQLで使用可能なデータ型は下記の通り

#### 数値

|データ型       |扱うもの      |
|:-------------:|:------------:|
|`INT(INTEGER)` |整数          |
|`DOUBLE`       |浮動小数点数  |
|`BOOL(BOOLEAN)`|真偽値        |

#### 文字列等

|データ型       |扱うもの      |
|:-------------:|:------------:|
|`VARCHAR`      |可変文字列    |
|`CHAR`         |固定文字列    |
|`TEXT`         |長い文字列    |
|`BLOB`         |バイナリデータ|

#### 時刻

|データ型       |扱うもの    |
|:-------------:|:----------:|
|`DATETIME`     |日時        |
|`DATE`         |日付        |
|`TIME`         |時刻        |

### サンプル

```SQL
CREATE TABLE members (
		memno INT,
		name VARCHAR(16),
		pref VARCHAR(4)
		);
```

- CREATE文の実行

```
MariaDB [dekirusample]> CREATE TABLE members (
    -> memno INT,
    -> name VARCHAR(16),
    -> pref VARCHAR(4)
    -> );
Query OK, 0 rows affected (0.08 sec)
```

- `SHOW TABLES`で確認

```
MariaDB [dekirusample]> show tables;
+------------------------+
| Tables_in_dekirusample |
+------------------------+
| members                |
+------------------------+
1 row in set (0.01 sec)
```
