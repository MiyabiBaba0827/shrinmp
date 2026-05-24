# プロジェクト

このリポジトリは `Nodejs` ディレクトリを中心とした Node.js アプリケーションを含みます。

## 構成

- `Nodejs/` : Node.js アプリケーション本体
- `.devcontainer/` : VS Code Dev Container 設定

## Docker の利用方法

ルートディレクトリで以下を実行します。

### Docker イメージのビルド

```sh
docker build -f .devcontainer/nodejs/Dockerfile -t nodejs .
```

### Docker コンテナの起動

```sh
docker run --rm -p 3000:3000 -p 3443:3443 nodejs
```

### docker-compose を使う場合

```sh
docker compose -f .devcontainer/docker-compose.yml up --build
```

### コンテナを停止する

```sh
docker compose -f .devcontainer/docker-compose.yml down
```

## Dev Container の利用

VS Code からリポジトリを開き、`Remote-Containers: Reopen in Container` を実行します。

この設定ではホストの Docker ソケット `/var/run/docker.sock` をコンテナにマウントするため、コンテナ内から Docker コマンドが利用できます。

## Nodejs アプリの詳細

`Nodejs/README.md` にアプリケーション固有の開発手順と構成を記載しています。
