04\_HowToDeleteRows
===

## 概要

- 行の削除方法をまとめる。

## `DELETE`

### 概要

- 行を削除する。

### 文法

`DELETE FROM テーブル名 WHERE 条件`

### サンプルコード

#### 実行前確認

```SQL
SELECT * FROM members;
```

- 実行結果

```
MariaDB [dekirusample]> select * from members;
+-------+------------------+----------+
| memno | name             | pref     |
+-------+------------------+----------+
|     1 | たかはしまさかず | 神奈川県 |
|     2 | 山本陽一         | 北海道   |
|     3 | 杉本彰大         | 福岡県   |
|     4 | 石橋克隆         | NULL     |
+-------+------------------+----------+
4 rows in set (0.00 sec)
```

#### 行の削除

```SQL
DELETE FROM MEMBERS WHERE memno=1;
```

- 実行結果

```
MariaDB [dekirusample]>DELETE FROM MEMBERS WHERE memno=1;
Query OK, 1 row affected (0.01 sec)
```

#### 実行後確認

```SQL
SELECT * FROM members;
```

- 実行結果

```
MariaDB [dekirusample]> SELECT * FROM members;
+-------+----------+--------+
| memno | name     | pref   |
+-------+----------+--------+
|     2 | 山本陽一 | 北海道 |
|     3 | 杉本彰大 | 福岡県 |
|     4 | 石橋克隆 | NULL   |
+-------+----------+--------+
3 rows in set (0.00 sec)
```
