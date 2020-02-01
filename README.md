[日本語のREADMEは英語の下にあります]

# shp2mysql

shp2mysql is a fork of shp2pgsql(PostGIS).

shp2mysql is a command-line tool that converts a shape file into SQL for import shape file into MySQL. shp2mysql supports MySQL 8.0 and later.

## Download

You can download shp2mysql from the release page.
https://github.com/hajime-miyauchi/shp2mysql/releases

## Install

### Windows

There is an executable file(shp2mysql.exe) on the release page. It is provided as a compressed file and the name is shp2mysql-win-64.zip.

### Linux/Mac

You can compile it from source as follows.

```
$ ./configure
$ make
$ sudo make install
```

## How to use shp2mysql.

Execute with the input shape file name as an argument and saves the output as follows.

```
$ shp2mysql input.shp > output.sql
```

Execute the generated SQL in MySQL.

```
$ mysql -u root -p <<database_name>> < output.sql
```

You can also specify the character sets and/or SRID of the input shape file.

```
$ shp2mysql -W CP932 -s 4326 input.shp > output.sql
```



# README日本語版

# shp2mysql

shp2mysql is a fork of shp2pgsql(PostGIS).

shp2mysqlはシェープファイルを、MySQL8へのインポート用SQLに変換するコマンドラインツールです。
MySQL8.0以降を対象としています。

## ダウンロード

リリースページからダウンロードします。

https://github.com/hajime-miyauchi/shp2mysql/releases

## インストール

### Windows

リリースページに実行ファイル(shp2mysql.exe)があります。

### Linux/Mac

ソースからコンパイルします。

```
$ ./configure
$ make
$ sudo make install
```

## 使い方

入力するシェープファイル名を引数として実行し、出力結果を保存します。

```
$ shp2mysql input.shp > output.sql
```

生成されたSQLをMySQLで実行します。

```
$ mysql -u root -p データベース名 < output.sql
```

入力の文字コードやSRIDを指定することもできます。

```
$ shp2mysql -W CP932 -s 4326 input.shp > output.sql
```

