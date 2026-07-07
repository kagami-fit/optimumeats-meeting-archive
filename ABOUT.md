# OptimumEats Meeting Archive

## 一言で言うと

OptimumEatsの店舗運営マニュアル化プロジェクト用に作成した、閲覧専用の議事録アーカイブサイトです。議事録の要点、決定事項、アクション、図解を日付ごとに見返せます。

## 何ができるのか

- 議事録を日付別に一覧表示
- 要約、議題、決定事項、課題、次回アクションを確認
- 担当者、期限、状態つきのアクション項目を確認
- Image-gen2で作成した図解PNGを議事録に紐づけて表示
- サイドバーの開閉状態をブラウザに保存
- GitHub Pages用の静的サイトとして公開可能

## 構成

- `public/index.html` — 議事録アーカイブの画面本体
- `public/styles.css` — OptimumEats公式サイトの白・黒・ブラウン・オリーブ系に寄せたデザイン
- `public/app.js` — 日付別アーカイブ、詳細表示、図解ライトボックス
- `public/records.json` — 公開する議事録データ
- `public/records/` — 議事録ごとの図解PNG保存先
- `public/brand/logo.svg` — 公式サイトから取得したOptimumEatsロゴ
- `server/index.js` — ローカル確認用の読み取り専用Expressサーバー
- `.github/workflows/pages.yml` — GitHub Pages公開用ワークフロー

## 使い方

```bash
cd /Users/hayatokagami/Documents/OptimumEats/minutes-archive-site
npm install
npm run dev
```

起動後、ブラウザで以下を開きます。

```text
http://localhost:3000
```

チェックだけ行う場合は以下です。

```bash
npm run check
```

## 状態

- ルートプロジェクト — 開発中。OptimumEats用の初期サイトを作成済み
- `public/` — 稼働中。議事録4件、公式ロゴ、図解画像、レスポンシブ画面を実装済み
- `server/` — 稼働中。ローカル確認用サーバーとして実装済み
- `public/records/2026-07-05-operations-manual-kickoff/` — 稼働中。キックオフMTGの図解PNGを保存済み
- `public/records/2026-07-06-ai-tools-website-renovation-progress/` — 稼働中。AI/Web改善MTGの図解PNGを保存済み
- `public/records/2026-07-06-operations-flow-checklist-reservation/` — 稼働中。業務フロー・予約管理MTGの図解PNGを保存済み
- `public/records/2026-07-06-inventory-checklist-design/` — 稼働中。在庫チェック表MTGの図解PNGを保存済み
- GitHub Pages公開 — 稼働中。`gh-pages` ブランチから公開
