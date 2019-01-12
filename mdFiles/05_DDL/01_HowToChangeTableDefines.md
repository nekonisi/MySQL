01\_HowToChangeTableDefines
===

## 概要

- テーブル定義の変更方法をまとめる。

## `ALTER`

### 概要

- テーブル定義を変更する。

### 文法

`ALTER TABLE テーブル名 ALTER指定`

### ALTER指定について

|指定                                           |解説                                                                  |
|`ADD [COLUMN] 列名 データ型 [FIRST;AFTER 列名]`|列を追加する。デフォルトでテーブルの最後に追加する。<br>`[FIRST]`を指定するとテーブルの最初に，`[AFTER]`を指定すると，`列名`で指定した列の後に追加する。|
|`CHANGE [COLUMN] 列名 新列名 新データ型`       |列の定義を変更する。列名またはデータ型，あるいはその両方を変更できる。|
|`MODIFY [COLUMN] 列名 新データ型`              |列のデータ型を変更する。                                              |
|`DROP [COLUMN] 列名`                           |列を削除する。                                                        |

### サンプルコード

#### テーブル定義を変更

```SQL
ALTER TABLE members CHANGE pref district VARCHAR(4);
```

- 実行結果

```
MariaDB [dekirusample]> ALTER TABLE members CHANGE pref district VARCHAR(4);
Query OK, 0 rows affected (0.07 sec)
Records: 0  Duplicates: 0  Warnings: 0
```

#### 変更内容を確認

```SQL
SHOW COLUMNS FROM members;
```

- 実行結果

```
MariaDB [dekirusample]> SHOW COLUMNS FROM members;
+----------+-------------+------+-----+---------+-------+
| Field    | Type        | Null | Key | Default | Extra |
+----------+-------------+------+-----+---------+-------+
| memno    | int(11)     | YES  |     | NULL    |       |
| name     | varchar(16) | YES  |     | NULL    |       |
| district | varchar(4)  | YES  |     | NULL    |       |
+----------+-------------+------+-----+---------+-------+
3 rows in set (0.05 sec)
```

- `pref`を`district`に変更
  - `pref` : 県
  - `district` : 地区
