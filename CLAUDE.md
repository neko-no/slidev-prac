# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## プロジェクト概要

これはSlidevプレゼンテーションプロジェクトです。Slidevは開発者向けのスライド作成・プレゼンテーションツールで、Markdownを使用してプレゼンテーションを作成できます。

## 開発コマンド

### パッケージマネージャー

このプロジェクトは`pnpm`をパッケージマネージャーとして使用しています。

### 共通コマンド

- `pnpm install` - 依存関係をインストール
- `pnpm dev` または `npm run dev` - 開発サーバーを起動（自動リロード付き、<http://localhost:3030>で開きます）
- `pnpm build` または `npm run build` - プロダクション用にプレゼンテーションをビルド
- `pnpm export` または `npm run export` - スライドを静的ファイルにエクスポート

### 作業ディレクトリ

メインのSlidevプロジェクトは`slidev/`サブディレクトリにあります。すべての開発コマンドはこのディレクトリ内で実行する必要があります。

## プロジェクト構造

```text
slidev/
├── slides.md           # メインプレゼンテーション内容
├── components/         # スライド用Vueコンポーネント
│   └── Counter.vue    # サンプルコンポーネント
├── pages/             # 追加スライドページ
├── snippets/          # プレゼンテーション用コードスニペット
└── package.json       # プロジェクト依存関係とスクリプト
```

## 主要ファイル

- `slides.md` - フロントマター設定付きでMarkdownでスライド内容を記述するメインプレゼンテーションファイル
- `components/` - スライド内で使用できるカスタムVueコンポーネント
- `snippets/` - スライドに埋め込み可能な外部コードスニペット

## Slidev設定

プレゼンテーションは以下で設定されています：

- テーマ: `seriph`（slides.mdのフロントマターで変更可能）
- 拡張Markdownコンポーネント用のMDC構文が有効
- 描画の永続化は無効
- スライドトランジションが有効

## 開発ノート

- スライドはYAMLフロントマター付きのMarkdownで記述
- Vueコンポーネントをスライドに直接埋め込み可能
- コードハイライト、アニメーション、LaTeX、図表をサポート
- 開発モードでライブ編集が利用可能
- 開発時はプレゼンテーションが<http://localhost:3030>で実行
