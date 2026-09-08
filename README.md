# 特別支援学級 所見作成支援システム Web版

**Version 6.3.0**

特別支援学級における所見作成を、既存の記録を中心に「見取る → 記録する → 振り返る → 次へつなぐ」ための単一HTML型Webアプリです。

## 基本方針
- 入力画面を増やさず、既存の記録を複数の仕事へつなげる
- 一人の子どもを中心に、所見・履歴・成長シート・面談準備・次の支援・年度レビューをつなげる
- システムが子どもの評価や支援方針を自動決定しない
- 最終確認・判断は先生が行う

## 主な機能
- 所見作成・保存・履歴管理
- 前回からの変化の確認
- 成長シート
- 面談準備
- 記録まとめ
- 次の支援
- 年度レビュー
- 児童ポートフォリオ
- クラス全体の進捗・見通し
- Excel出力
- JSONバックアップ／復元
- 印刷
- デモデータ
- 3分ガイド
- システム診断・公開前点検
- Gemini API連携（任意）

## ファイル構成
- `index.html` — Vercel等の静的ホスティング用エントリーポイント
- `app.html` — 配布用単一HTML本体
- `MANUAL.md` — 操作マニュアル
- `VECTOR_MANUAL.md` — Vector掲載時の説明・導入手順
- `vercel.json` — Vercel静的配信用設定
- `LICENSE` — MIT License
- `.gitignore` — Git管理対象外設定
- `.github/workflows/validate.yml` — GitHub Actionsによる自動点検

## GitHubへの公開
1. このフォルダをGitリポジトリとして登録します。
2. GitHubで空の公開リポジトリを作成します。
3. `git add .` → `git commit` → `git push` で公開します。

## Vercelへの公開
GitHubリポジトリをVercelへImportし、Framework Presetは静的HTMLとして扱います。Build Commandは不要、Output Directoryはリポジトリ直下です。`index.html`を入口として公開できます。

## Vectorへの配布
`app.html`は単一HTMLとしてオフラインでも利用できます。Vector掲載時は、`app.html`を配布本体とし、`VECTOR_MANUAL.md`の説明文・注意事項を商品説明として利用できます。

## 重要な注意
Gemini APIを利用する場合、現在のWeb版はブラウザからAPIへ直接接続する方式です。APIキーをブラウザ側へ置く構成は、公開サービスとして秘密情報を完全には保護できません。公開運用でAPIキーを安全に管理する場合は、サーバー側プロキシ等への移行を推奨します。

個人情報・要配慮情報を入力する際は、学校の情報管理規程、利用するAIサービスの規約、所属自治体・学校の方針を確認してください。

## 公開前チェック
- [ ] 実ブラウザで主要操作を確認
- [ ] 新規入力→保存→履歴を確認
- [ ] JSONバックアップ→復元を確認
- [ ] Excel出力を実際に開いて確認
- [ ] 個人情報を含むデータのAI送信範囲を確認
- [ ] APIキーの管理方法を確認
- [ ] 最終的な所見・評価・支援判断を先生が確認


### 公開時の補助ファイル
- `SECURITY.md` — Gemini APIキー・個人情報の取り扱いに関する注意
- `CHANGELOG.md` — 主なバージョン更新履歴
- `.github/workflows/validate.yml` — GitHub Actionsによる構文・ID・バージョンの自動点検
---
GitHub連携によるVercel自動デプロイ確認済み
## ライセンス
MIT License。学校等での利用・改変を想定しています。
