# LIFF LINEログインフォーム

LINE LIFF（LINE Front-end Framework）を使用して、GoogleフォームにLINEユーザーIDを自動入力するアプリケーションです。

## 機能

- LINEログイン機能
- ユーザーIDの自動取得
- Googleフォームへの自動リダイレクト
- ユーザーIDの自動入力

## セットアップ

### 1. LIFF IDの設定

`form.html`の以下の行で、あなたのLIFF IDを設定してください：

```javascript
const liffId = "2007697448-JE8Kx3Mq"; // あなたのLIFF IDに変更
```

### 2. Googleフォームの設定

Googleフォームで以下の設定を行ってください：

1. Googleフォームを作成
2. LINEユーザーIDを受け取る項目を追加
3. その項目のentry IDを確認
4. `form.html`の以下の行でentry IDを設定：

```javascript
const userIdEntryId = "entry.1234567890"; // 実際のentry IDに変更
```

### 3. GoogleフォームのURL設定

`form.html`の以下の行で、GoogleフォームのURLを設定してください：

```javascript
const googleFormBaseUrl = "https://docs.google.com/forms/d/e/YOUR_FORM_ID/viewform";
```

## 使用方法

1. ファイルをWebサーバーにアップロード
2. LINE DevelopersコンソールでLIFFアプリのエンドポイントURLを設定
3. LINEアプリ内でLIFFアプリを起動
4. 自動的にGoogleフォームにリダイレクトされ、ユーザーIDが入力されます

## 注意事項

- LIFFアプリはHTTPS環境でのみ動作します
- Googleフォームのentry IDは正確に設定してください
- テスト環境での動作確認を推奨します

## トラブルシューティング

### よくある問題

1. **LIFF SDKの読み込みエラー**
   - ネットワーク接続を確認
   - HTTPS環境で実行されているか確認

2. **Googleフォームへのリダイレクトエラー**
   - entry IDが正しく設定されているか確認
   - GoogleフォームのURLが正しいか確認

3. **ログインエラー**
   - LIFF IDが正しく設定されているか確認
   - LINE Developersコンソールの設定を確認

## ライセンス

このプロジェクトはMITライセンスの下で公開されています。 