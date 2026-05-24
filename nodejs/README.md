# Node.js プロジェクト

このディレクトリは Node.js を用いたアプリケーションのソースコードおよび関連ファイルを管理しています。

## ディレクトリ構成

- `src/` : アプリケーションの TypeScript ソースコード
- `http-test/requests.rest` : HTTP リクエストのテスト用ファイル
- `package.json` : プロジェクトの依存関係とスクリプト
- `tsconfig.json` : TypeScript 設定ファイル

## Docker / devcontainer

Docker のビルドや起動、VS Code の Dev Container は、リポジトリルートの `README.md` と `.devcontainer/` を参照してください。

## セットアップ

1. 依存パッケージのインストール

```sh
npm install
```

2. 開発サーバーの起動

```sh
npm run dev
```

## その他

- 本ディレクトリの詳細な使い方や設定はルート `README.md` を参照してください。
