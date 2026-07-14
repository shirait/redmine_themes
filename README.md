# Redmine Purple Dark Theme

紫を基調としたダークテーマ for [Redmine](https://www.redmine.org/)。

> **Note:** This is an unofficial theme. It is not affiliated with, endorsed by, or maintained by the Redmine project.

## 概要

Redmine Purple Dark Theme は、標準 UI を紫系のダーク配色で上書きする CSS テーマです。長時間の作業でも目に負担が少ないよう、背景・文字・リンク・フォームなど主要 UI 要素を調整しています。

## スクリーンショット

<!-- TODO: スクリーンショットを追加 -->
<!-- ![Screenshot](docs/screenshot.png) -->

## 主な特徴

- 紫系のダーク配色（背景・ヘッダー・サイドバー・フォーム）
- 一覧テーブル（`table.list`）のダークスタイル
- Wiki 未作成ページリンクの赤色表示（`a.wiki-page.new`）
- Wiki 表のヘッダ行スタイル（tablesort 対応）
- Wiki プレビュー、チケット、プロジェクト一覧など主要画面の配色調整

## 動作確認環境

| 項目 | バージョン |
|------|-----------|
| Redmine | 7.0.x |

他バージョンでも動作する可能性がありますが、未検証です。

## インストール

### 1. テーマを配置

Redmine の `themes` ディレクトリに、このリポジトリの `purple-dark` フォルダを配置します。

```bash
cd /path/to/redmine
git clone https://github.com/YOUR_USERNAME/redmine-purple-dark-theme.git /tmp/redmine-purple-dark-theme
cp -r /tmp/redmine-purple-dark-theme/purple-dark themes/
```

リポジトリ構成によっては、`stylesheets/application.css` を含むフォルダ自体を `themes/purple-dark` として配置してください。

```
redmine/
└── themes/
    └── purple-dark/
        └── stylesheets/
            └── application.css
```

### 2. アセットの再生成（本番環境）

本番環境ではアセットのプリコンパイルが必要な場合があります。

```bash
cd /path/to/redmine
bundle exec rake assets:precompile RAILS_ENV=production
```

### 3. Redmine の再起動

使用しているアプリケーションサーバー（Puma、Passenger など）を再起動してください。

## 有効化

1. **管理** → **設定** → **表示** を開く
2. **UI theme** で `purple-dark` を選択
3. **保存**

## アンインストール

1. 管理画面で UI theme を別のテーマ（または空）に戻す
2. `themes/purple-dark` ディレクトリを削除
3. 必要に応じて `assets:precompile` を実行し、Redmine を再起動

## カスタマイズ

配色は `stylesheets/application.css` 内の CSS 変数・カラーコードを編集することで変更できます。

例: Wiki 表ヘッダ行の背景色

```css
div.wiki table thead th {
  background-color: #d9e8a8 !important;
}
```

## ライセンス

[MIT License](LICENSE)

## 免責事項

本テーマは作者の善意で提供されるものです。利用により生じたいかなる損害についても、作者は責任を負いません。Redmine のバージョンアップ後は表示崩れが発生する場合があります。その際は Issue 報告または CSS の修正をお願いします。

