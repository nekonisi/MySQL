01\_HowToInsertRow
===

## 概要

- テーブルへの行の追加の仕方についてまとめる。
- DML文の`INSERT`を使用する。

## `INSERT`

### 概要

- 新規の行の追加を行う。

### 文法1

`INSERT INTO テーブル名 VALUES (値, ...), (値, ...),... `

### 文法2

- 列名を指定して実行する。
- 指定しなかった列は`NULL`または，デフォルト値になる。

`INSERT INTO テーブル名 (列名1, 列名2, ...) VALUES (値, ...), (値, ...),... `

### サンプル1

```SQL
INSERT INTO members VALUES
(1, '高橋正和', '東京都'),
(2, '山本陽一', '北海道'),
(3, '杉本彰大', '福岡県');
```

```
MariaDB [dekirusample]> INSERT INTO members VALUES(1, '高橋正和', '東京都'),(2, '山本陽一', '北海道'),(3, '杉本彰大', '福岡県');
Query OK, 3 rows affected, 6 warnings (0.01 sec)
Records: 3  Duplicates: 0  Warnings: 6
```

### サンプル2

```SQL
INSERT INTO members
(memno, name) VALUES
(4, '石橋克隆');
```

```
MariaDB [dekirusample]> INSERT INTO members(memno, name) VALUES(4, '石橋克隆');
Query OK, 1 row affected, 1 warning (0.02 sec)
```

- 実行結果確認

```SQL
SELECT * FROM members;
```

- 文字化けしているので，後日記述する。
