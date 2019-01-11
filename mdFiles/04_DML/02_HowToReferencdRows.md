02\_HowToReferencdRows
===

## 概要

- 行の参照方法をまとめる。

## `SELECT`

### 概要

- 行の参照を行う。

### 文法

`SELECT 列名... FROM テーブル名 WHERE 条件`

### サンプル

#### テーブル参照(列名，条件指定なし)

```SQL
SELECT * FROM MEMBERS;
```

- 実行結果

```
MariaDB [dekirusample]> SELECT * FROM MEMBERS;
+-------+----------+--------+
| memno | name     | pref   |
+-------+----------+--------+
|     1 | 高橋正和 | 東京都 |
|     2 | 山本陽一 | 北海道 |
|     3 | 杉本彰大 | 福岡県 |
|     4 | 石橋克隆 | NULL   |
+-------+----------+--------+
4 rows in set (0.00 sec)
```

#### テーブルの参照(列名指定あり)

```SQL
SELECT name, pref FROM MEMBERS;
```

- 実行結果

```
MariaDB [dekirusample]> SELECT name, pref FROM MEMBERS;
+----------+--------+
| NAME     | PREF   |
+----------+--------+
| 高橋正和 | 東京都 |
| 山本陽一 | 北海道 |
| 杉本彰大 | 福岡県 |
| 石橋克隆 | NULL   |
+----------+--------+
4 rows in set (0.00 sec)
```

#### テーブルの参照(条件指定あり)

```SQL
SELECT * FROM MEMBERS WHERE PREF = '東京都';
```

- 実行結果

```
MariaDB [dekirusample]> SELECT * FROM MEMBERS WHERE PREF = '東京都';
+-------+----------+--------+
| memno | name     | pref   |
+-------+----------+--------+
|     1 | 高橋正和 | 東京都 |
+-------+----------+--------+
1 row in set (0.01 sec)
```
