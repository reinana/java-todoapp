Java ToDoアプリ

概要
JavaとSpring Bootを用いたToDo管理アプリです。Thymeleafを使用したシンプルなWebインターフェースを備え、タスクの登録・更新・削除・一覧表示が可能です。

使用技術
言語: Java 21
フレームワーク: Spring Boot 3.3.8
データベース: PostgreSQL
ビューエンジン: Thymeleaf
ORM: MyBatis
ビルドツール: Gradle
認証・セキュリティ: Spring Security

必要条件
Java 21 以上
PostgreSQL (データベース todo_db が作成済みであること)
Gradle
Git

環境構築
1. リポジトリのクローン
 git clone https://github.com/stein579/java-todoapp.git
 cd java-todoapp

2. データベースのセットアップ
PostgreSQLに todo_db データベースが存在しない場合は、以下のSQLを実行して作成してください。

CREATE DATABASE todo_db;

application.properties に接続情報を設定してください。

spring.datasource.url=jdbc:postgresql://localhost:5432/todo_db
spring.datasource.username=your_username
spring.datasource.password=your_password

3. 依存関係のインストール
gradlew スクリプトが既にリポジトリ内に含まれているため、そのまま以下のコマンドを実行できます。
 ./gradlew build

4. アプリの起動
 ./gradlew bootRun

使用方法
ブラウザで http://localhost:8080 にアクセス

ToDoの追加、編集、削除、一覧表示が可能
