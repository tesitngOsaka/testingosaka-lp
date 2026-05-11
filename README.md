# testingOsaka 公式サイト

testingOsakaは、大阪や関西で働くソフトウェアエンジニアやプロダクト開発の当事者が、テストやQAについて語り、集うコミュニティ（略称：テオ）です。
このリポジトリは、testingOsakaの公式サイトのソースコードを管理しています。

## 🛠 開発環境のセットアップ

サイトの保守・更新を行うためには、以下のツールが必要です。
- Node.js (v18以降推奨)
- npm

### 1. リポジトリのクローンと依存関係のインストール

```bash
git clone <https://github.com/tesitngOsaka/testingosaka-lp.git>
cd testingosaka-lp
npm install
```
*(※リポジトリのURLは実際のホスティング先に合わせて読み替えてください)*

### 2. ローカルサーバーの起動

```bash
npm run dev
```
起動後、ブラウザで `http://localhost:4321` にアクセスすると、ローカル環境でサイトを確認できます。

## 📝 サイトの更新方法

このサイトは Astro と Tailwind CSS を使用して構築されています。
当サイトでは、記事コンテンツを「ブログ」と「ドキュメント」の2種類に分けて管理しています。
- **ブログ**: イベントの告知や活動報告など、時間に紐づいたフロー情報を扱います。
- **ドキュメント**: ガイドラインやナレッジなど、継続的に参照されるストック情報を扱います。

### ブログ記事の追加・編集
ブログ記事は `src/content/blog/` ディレクトリ内でMarkdown（`.md` または `.mdx`）ファイルとして管理されています。
新しい記事を追加する場合は、同ディレクトリに新しいMarkdownファイルを作成し、Frontmatter（記事上部のメタデータ）を設定して執筆してください。

### ドキュメントの追加・編集
ドキュメントは `src/content/docs/` ディレクトリ内でMarkdownファイルとして管理されています。
新しいドキュメントを追加する場合は、同ディレクトリに新しいMarkdownファイルを作成し、Frontmatter（記事上部のメタデータ）を設定して執筆してください。
ファイル名がそのままページのURL（例: `why-testingosaka.md` -> `/docs/why-testingosaka`）になり、ドキュメント一覧にも自動的に追加されます。

### ページ内容（テキスト）の変更
- トップページ全体: `src/pages/index.astro`
- コンポーネントごとの内容: `src/components/` 内の各ファイル（`hero.astro`, `features.astro`, `cta.astro` など）
- その他のページ: `src/pages/about.astro` や `src/pages/contact.astro` など

### 共通パーツの変更
ナビゲーションバーやフッターなどの全ページ共通のパーツは、`src/components/` フォルダ内にあります。
- ナビゲーション: `src/components/navbar/navbar.astro`
- フッター: `src/components/footer.astro`


## 帰属表示・クレジット

本サイトは無料テンプレート Astroship (by Web3Templates) をベースに作成しています。ライセンスに則り、フッターのクレジット表記は保持してください。
