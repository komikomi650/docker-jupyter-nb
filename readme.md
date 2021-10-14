## jupyter labをdocker-composeにて作成する方法 ##
前提として、 [Docker Desktop](https://www.docker.com/products/docker-desktop) がインストールされていることを想定して解説します。
Windows使用者の方はWSLが有効化する必要があります。

** クローン作成 **

1. 本bitbucketよりクローン作成ボタンにてcloneコマンドを取得する

参考コマンド

```
   git clone https://github.com/komikomi650/docker-jupyter-nb.git
```

~~

2. cloneしたディレクトリ内に移動し、workディレクトリを作成
```
   mkdir work
```
   ※jupyter notebookで作成したファイルを保存するために必要

~~

*** ディレクトリ作成部分は以降の`docker-compose up`で自動的に作成されます。 ***
*** ただし権限の問題でファイル作成ができなくなる可能性があるので、留意が必要 ***

** jupyter notebookのbuild **
ここからはWindowsの場合はpowershellで実行する必要があるかもしれません。

1. クローン作成したディレクトリに"docker-compose.yml"があることを確認

2. 下記コマンドにてビルドを行う
```
　　docker-compose build
```
** jupyter notebookの起動 **

1. 下記コマンドで起動する
```
　　docker-compose up 
```
** jupyter notebookにログイン **

1. 使用しているブラウザを立ち上げて下記URLを入力
```
   http://127.0.0.1:8888
```
以上でjupyter notebook起動までの説明を終わります。





