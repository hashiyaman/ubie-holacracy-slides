# これはなに？

[こちらのnote記事](https://note.com/hashiyaman/n/nc83ac8198318)を、[Marp](https://marp.app/)を使用してプレゼンテーション資料を作成したものです。

# PDF生成方法

## ローカルでの生成
```bash
# 依存関係のインストール
npm install

# PDF生成
npm run build

# 開発時の自動更新（オプション）
npm run watch
```

## GitHub Actionsによる自動生成
mainブランチにプッシュすると、以下のタイミングで自動的にPDFが生成されます：
- `slide.md`が更新されたとき
- `images/`ディレクトリ内のファイルが更新されたとき

生成されたPDFは：
GitHub Actionsの"Artifacts"からダウンロード可能です。
各ワークフロー実行後、Artifactsセクションから最新のPDFをダウンロードできます。

## コマンドオプション説明
- `--pdf-notes`: プレゼンテーションモードでの出力
- `--allow-local-files`: ローカルの画像ファイルを使用可能に
