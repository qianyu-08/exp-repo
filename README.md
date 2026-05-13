# 🧠 Smart Issue Auto Classifier テスト用README（仕様 vs バグ判定版）

このリポジトリはGitHub ActionsによるIssue自動分類ボットのテスト用です。

ボットはIssueを以下の4種類に分類します：

* 🐛 bug（バグ）
* 💡 feature（機能要望）
* 📄 spec-like（仕様に基づく挙動）
* ❓ unclear（不明）

---

# 🧪 判定テスト用ケース集

以下のIssueを作成して、ボットの判定精度を確認してください。

---

## 🐛 バグとして扱われるべきケース

### ケース1

**Title:**

```
login button does not work
```

**Body:**

```
clicking login does nothing
page freezes after submit
```

👉 期待: bug

---

### ケース2

**Title:**

```
error occurs when saving file
```

**Body:**

```
exception thrown in console
save operation fails randomly
```

👉 期待: bug

---

## 💡 機能要望として扱うケース

### ケース3

**Title:**

```
add dark mode support
```

**Body:**

```
users want better night usability
feature request: dark theme
```

👉 期待: feature

---

### ケース4

**Title:**

```
please support exporting pdf
```

**Body:**

```
it would be useful to export reports as pdf
```

👉 期待: feature

---

## 📄 仕様として扱うべきケース

### ケース5

**Title:**

```
expected behavior differs from actual result
```

**Body:**

```
according to design, system should not allow this action
but current behavior blocks valid input
```

👉 期待: spec-like

---

### ケース6

**Title:**

```
this is intended behavior
```

**Body:**

```
documentation says this is expected
system behaves correctly according to spec
```

👉 期待: spec-like

---

## ❓ 判定が難しいケース（unclear想定）

### ケース7

**Title:**

```
it doesn't work
```

**Body:**

```
something is broken
not sure why
```

👉 期待: unclear

---

### ケース8

**Title:**

```
weird behavior happens
```

**Body:**

```
sometimes it works sometimes not
cannot reproduce consistently
```

👉 期待: unclear

---

# 🧠 判定ルール（参考）

* bug: error / crash / fail / 動かない / 落ちる
* feature: add / support / want / request
* spec-like: should / expected / design / documentation
* unclear: 情報不足 or 再現不可

---

# ⚠️ 注意

このボットは自然言語を完全に理解するAIではなく、
キーワードベースの簡易分類システムです。

そのため誤判定は仕様です（バグではありません）。

---

# 🧊 まとめ

このリポジトリは「Issueを人間の代わりに理解する」のではなく、
「Issueを雑に仕分けする機械」の挙動確認用です。
