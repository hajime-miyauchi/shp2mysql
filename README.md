# shp2mysql

shp2mysql is a fork of shp2pgsql(PostGIS).

shp2mysqlはシェープファイルを、MySQL8へのインポート用SQLに変換するコマンドラインツールです。

## 使い方

```
$ shp2mysql input.shp > output.sql
```

## インストール

ソースからコンパイルします。

```
$ ./autogen.sh
$ ./configure
$ make
$ sudo make install
```

もしくはリリースに一部プラットフォームの実行ファイルがあります。

https://github.com/hajime-miyauchi/shp2mysql/releases
