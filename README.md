# sample-java-api_server

## 前提条件

各ツールがインストール済であること

- VSCode
- Docker

VSCodeの以下の拡張機能をインストールすること

- Remote - Containers

## 環境構築方法

1. VSCodeで`sample-java-api_server`を開く
2. 左下にある`><`をクリックし、`Open folder in Container`をクリックし、`sample-java-api_server`を選択し、開く
3. 問題がなければ、コンテナが作成される
4. 作成後、DBがあるかどうか確認する為、以下のコマンドをコンテナ内のターミナルで入力する  
     1. DBの中に入る：`sqlite3 sqlitesample.db`
     2. テーブルがあるかどうか確認：`./tables`

※ 上記の4の2でテーブルがない場合、作成する必要がある為、下記のコマンドを入力する  

1. テーブル作成：`create table scores(id integer primary key autoincrement, score integer);`
2. データの登録：`insert into scores(score) values(100);`

## 実行方法

`/opt/spring_project/src/main/java/com/example/spring_project/SpringProjectApplication.java`へ移動し、`SpringProjectApplication.java`の35行目の上に`Run|Debug`というのがあるので、`Debug`をクリックする

## 拡張機能

開発する上で必要に応じて、以下をインストールする

- MS-CEINTL.vscode-language-pack-ja
- vscjava.vscode-java-pack: JavaExtensionPack
- pivotal.vscode-boot-dev-pack: Spring Boot Extension Pack
- gabrielbb.vscode-lombok: Lombok Annotations Support For VS Code
