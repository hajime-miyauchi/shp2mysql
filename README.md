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

