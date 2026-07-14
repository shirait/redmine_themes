# Redmine Purple Dark Theme

紫を基調としたダークテーマ for [Redmine](https://www.redmine.org/)。

> 注：これは非公式のテーマです。Redmineプロジェクトとは一切関係がなく、承認もメンテナンスも受けていません。

## 概要

Redmine Purple Dark Theme は、標準 UI を紫系のダーク配色で上書きする CSS テーマです。長時間の作業でも目に負担が少ないよう、背景・文字・リンク・フォームなど主要 UI 要素を調整しています。

## スクリーンショット

準備中...。
<!-- TODO: スクリーンショットを追加 -->
<!-- ![Screenshot](docs/screenshot.png) -->

## 主な特徴

- 紫系のダーク配色（背景・ヘッダー・サイドバー・フォーム）
- チケット、wiki、プロジェクト一覧など主要画面の配色調整

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
git clone https://github.com/shirait/redmine_themes.git /tmp/redmine-purple-dark-theme
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

### 2. Redmine の再起動

使用しているアプリケーションサーバー（Puma、Passenger など）を再起動してください。

## 有効化

1. **管理** → **設定** → **表示** を開く
2. **テーマ** で `purple-dark` を選択
3. **保存** をクリック

## アンインストール

1. 管理画面で UI theme を別のテーマ（または空）に戻す
2. `themes/purple-dark` ディレクトリを削除
3. 必要に応じてアプリケーションサーバー（Puma、Passenger など）を再起動

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

本テーマの利用により生じたいかなる損害についても、作者は責任を負いません。
Redmine のバージョンアップ後は表示崩れが発生する場合があります。その際は Issue 報告または CSS の修正をお願いします。

