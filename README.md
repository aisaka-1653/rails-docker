# 環境構築

## 1. ローカルにリポジトリをコピーする

- ターミナルでリポジトリをコピーしたいディレクトリに移動します。
```bash
$ cd ~/desktop
```
- git cloneでリモートリポジトリをローカルにコピーします。
```bash
$ git clone https://github.com/aisaka-1653/rails-docker.git
```

## 2. docker-composeを実行する

- コピーされたディレクトリに移動します。
```bash
$ cd ~/desktop/rails-docker
```
- **初回起動時のみ**以下のコマンドを実行してdatabaseを作成します。
```bash
$ docker-compose run --rm web rails db:create
```


- docker-composeを実行します。
```bash
$ docker-compose up
```
- detachモードで実行する事もできます。
```bash
$ docker-compose up -d
```

- `Listening on http://0.0.0.0:3000`がlogに表示されます。
- [http://localhost:3000](http://localhost:3000)にアクセスして、Tasksと書かれたページが表示されていれば完了です。

## version
- Ruby 3.22
- Node.js 18.13
- Rails 7.0.6
- PostgreSQL 12.17