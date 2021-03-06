01\_MySQLについて
===

## 概要

- MySQLの歴史とか豆知識とか現状についてまとめる。

## 発足

- 1995年にMonty WideniusによってMySQL 1.0がリリースされた。
- 後にMySQL ABの共同創立者となるDavid Axmarkの勧めにより，OSSとなった。
- 2000年にMySQL ABが創立される。
- 2008年にMySQL ABがサンマイクロシステムズに買収される。
- 2009年にサンマイクロシステムズがOracleに買収される。
- なので，MySQLはOracleの製品となっている。

## 豆知識

- MySQLのロゴであるイルカの名前は，"Sakila"
![ロゴ](https://www.mysql.com/common/logos/logo-mysql-170x115.png)
- WindowsでMySQLサーバを起動した場合，サービス名は`SQL56`となる。

## MySQLの種類

- コミュニティ版(MySQL Community Server)と商用版(MySQL Enterprise Edition)がある。
- 商用版は有料だが，サポートを受けることができる。

## 主なリレーショナルデータベースとその特性

|種類                |企業     |特性                                      |
|:------------------:|:-------:|:----------------------------------------:|
|Oracle Database     |Oracle   |企業での基幹システムで利用されることが多い|
|MySQL               |Oracle   |高速で使いやすさに定評がある。OSSシェア1位|
|Microsoft SQL Server|Microsoft|Windows環境でシェアが高く，使いやすい     |
|PostgreSQL          |-        |MySQLと並び世界で利用されている           |
|DB2                 |IBM      |Unix環境でのシェアが高く，堅牢性に定評あり|

## 標準としてのSQLと独自拡張のSQL

### 標準SQLについて

- SQLは，ANSI, ISO, JISが規格化しているものである。
- MySQLについても，この標準SQLへの対応がバージョンごとに対応している。
- 対応については各ベンダーや開発コミュニティによって，差がある。

### 独自のSQL拡張について

- MySQLの開発者は，標準SQLへの準拠を行いつつ開発を進めているが，*速度や信頼性を犠牲にすることなく*
  ユーザにとって使いやすくなるのであれば，独自のSQLに対する拡張機能やSQL以外の機能のサポートを行っている。
- 例えば，自動連番を行う[`AUTO_INCREMENT`][1]はMySQL独自の拡張機能である。  

これらの拡張機能を使用した場合，*ほかのリレーショナルデータベースにコードを移植できなくなる*ので注意する。

[1]: ../07_テーブルのカスタマイズ/02_主キーの自動連番.md
