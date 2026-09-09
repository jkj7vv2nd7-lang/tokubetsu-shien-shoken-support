# 公開手順（GitHub / Vercel / Vector）

## 1. GitHub

GitHubで新しい空のリポジトリを作成します。既存ファイルをアップロードする場合は、README・.gitignore・LicenseをGitHub側で追加せず、このパッケージのファイルをそのまま登録します。

### GitHub Desktopを使う場合
1. このフォルダをGitHub Desktopに追加。
2. リポジトリ名を確認。
3. Commitを作成。
4. Publish repositoryを実行。
5. 公開する場合はPrivate設定を外して公開。

### Gitコマンドを使う場合
```bash
git init
git branch -M main
git add .
git commit -m "Release v9.0.0"
git remote add origin https://github.com/YOUR-ACCOUNT/YOUR-REPOSITORY.git
git push -u origin main
```

## 2. Vercel

GitHubリポジトリをVercelのNew ProjectからImportします。Root Directoryはプロジェクト直下、Framework Presetは静的サイトとして扱い、特別なBuild Commandは設定不要です。`index.html`が入口になります。

GitHub連携後は、mainへのpushを本番更新に利用できます。

## 3. Vector

`app.html`を配布用本体として利用します。単一HTMLなので、ダウンロードしたファイルをChrome/Edge等で開いて使用できます。

掲載説明には`VECTOR_MANUAL.md`を利用してください。

## 4. 公開前に必ず行うこと

- 実ブラウザで3分ガイドを確認
- 児童追加・カテゴリー選択・入力・保存を確認
- 履歴・変化ビューを確認
- バックアップ→復元を確認
- Excel出力を実際に開く
- 印刷を確認
- システム診断を実行
- AIを使う場合の送信内容とAPIキー管理を確認
- 学校の情報管理規程を確認

## 5. APIキーについて

現在のGemini連携はブラウザから直接APIへ接続する構成です。公開WebサービスとしてAPIキーを秘密にする構成ではありません。公開運用でAI連携を安全に提供する場合は、後段でサーバー側プロキシ方式へ移行してください。
