# マルタ村相談室（シンプル版）

完結しない村の哲学を体現した相談チャットボット

## 🚀 超簡単デプロイ手順

### 必要なもの
1. GitHubアカウント
2. Anthropic APIキー（https://console.anthropic.com で無料取得）
3. Vercelアカウント（GitHubで無料登録）

---

## ステップ1：GitHubにアップロード

### 方法A：Web UIから（推奨・超簡単）

1. **GitHub（https://github.com）にログイン**

2. **新しいリポジトリを作成**
   - 右上の「+」→「New repository」
   - Repository name: `malta-consultation`
   - Public/Private: どちらでもOK
   - 「Create repository」をクリック

3. **ファイルをアップロード**
   - 「uploading an existing file」のリンクをクリック
   - ダウンロードしたフォルダの中身を**全部**ドラッグ&ドロップ
   - 重要：フォルダごとではなく、**中身のファイル**をアップロード
   - 「Commit changes」をクリック

---

## ステップ2：Vercelでデプロイ

1. **Vercel（https://vercel.com）にアクセス**
   - 「Sign Up」→「Continue with GitHub」

2. **プロジェクトをインポート**
   - 「Add New...」→「Project」
   - `malta-consultation`リポジトリを選択
   - 「Import」をクリック

3. **環境変数を設定**
   - 「Environment Variables」セクションで：
   - Name: `ANTHROPIC_API_KEY`
   - Value: あなたのAnthropic APIキー
   - 「Add」をクリック

4. **デプロイ**
   - 「Deploy」をクリック
   - 1〜2分待つ
   - 完成！🎉

---

## 完成！

URLが生成されます（例：https://malta-consultation-xxxx.vercel.app）

このURLを友人に送れば、すぐに使えます！

---

## 💡 このバージョンの特徴

- **超シンプル**：外部ライブラリは最小限
- **確実に動く**：依存関係のエラーが起きにくい
- **軽量**：ビルドが速い
- **メンテしやすい**：コードがわかりやすい

---

## トラブルシューティング

### ビルドエラーが出る場合

1. GitHubで全てのファイルがアップロードされているか確認
2. Vercelで環境変数`ANTHROPIC_API_KEY`が設定されているか確認
3. Vercelの「Deployments」→「Building」でエラーログを確認

### 404エラーが出る場合

ビルドが失敗している可能性があります。Vercelの「Deployments」でステータスを確認してください。

### APIエラーが出る場合

- Anthropic APIキーが正しく設定されているか確認
- APIキーにクレジットが残っているか確認（https://console.anthropic.com）

---

## 🔧 カスタマイズ

### システムプロンプトを変更

`pages/api/chat.js` の `SYSTEM_PROMPT` を編集

### デザインを変更

`pages/index.js` の `styles` オブジェクトを編集

---

## サポート

わからないことがあれば：
- Vercel: https://vercel.com/docs
- Anthropic: https://docs.anthropic.com
- Next.js: https://nextjs.org/docs

---

頑張ってください！🌱
