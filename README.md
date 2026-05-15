
# DummyApp

テスト用ダミープロジェクトです。  
この README は GitHub Actions の issue 自動判定テスト用に作られています。  
つまり README が人間ではなく bot に読まれる。未来。

---

# Features

- ログイン機能
- ダークモード
- オフライン非対応
- API通信あり
- ブラウザ上で動作

---

# Known Specifications

## CORSについて

このアプリは外部APIを直接呼び出します。  
そのため、一部環境では CORS エラーが発生することがあります。

これは現在の仕様です。

開発環境では以下を使用してください:

- proxy
- local backend
- mock server

---

## Offline Mode

オフラインモードはサポートされていません。

インターネット接続が必要です。

これは intended behavior です。

---

## Mobile Support

iPhone Safari は対応しています。

Android WebView は一部未対応です。

---

## Authentication

認証トークンは localStorage に保存されます。

ログアウト時に削除されます。

---

# FAQ

## Q. CORS エラーが出ます

仕様です。  
README の「CORSについて」を確認してください。

---

## Q. オフラインで動きません

オフラインモードは未対応です。

---

## Q. IEで動きません

Internet Explorer はサポート対象外です。

---

# Debug Tips

## 開発サーバー起動

```bash
npm install
npm run dev
````

---

## proxy例

```js
server: {
  proxy: {
    "/api": {
      target: "http://localhost:3000",
      changeOrigin: true
    }
  }
}
```

---

# Example Issues

以下は仕様として扱われます:

* "CORS エラーになります"
* "オフラインで動かない"
* "IE対応してない"

以下はバグ候補です:

* "ログインできない"
* "画面が真っ白"
* "保存ボタンが反応しない"

---

# License

MIT
