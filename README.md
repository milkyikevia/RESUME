# 📄 RESUME（履歴書・職務経歴書テンプレート）

## 📝 概要

履歴書・職務経歴書テンプレートです。  
**`js/resume-data.js` と `js/work-data.js` を編集するだけで、履歴書・職務経歴書を作成**できます。

👇デザインはこちらから確認できます。  
[RESUME（デザイン確認）](https://milkyikevia.github.io/RESUME/)

---

## 📁 ファイル構成

```text
/
├── index.html # 一覧ページ（編集不要）
├── resume.html # 履歴書テンプレート本体（編集不要）
├── work.html # 職務経歴書テンプレート本体（編集不要）
├── css/
│   ├── common.css 
│   ├── index.css # 一覧ページ専用のスタイル（編集不要）
│   ├── resume.css # 履歴書専用のスタイル（編集不要）
│   └── work.css # 職務経歴書専用のスタイル（編集不要）
├── js/
│   ├── resume-data.js # 履歴書の内容を編集するファイル
│   └── work-data.js # 職務経歴書の内容を編集するファイル
├── photo/
│   └── photo.jpg # 証明写真
└── README.md
```

---

## 🚀 インストール

### 1. リポジトリをクローンまたはダウンロード

```bash
git clone https://github.com/milkyikevia/RESUME.git
```

### 2. データファイルを編集

履歴書は `js/resume-data.js`、職務経歴書は `js/work-data.js` を編集します。
ファイル内のコメントを参考にしながら入力してください。

### 3. ブラウザで内容を確認

* `index.html` を開くと、履歴書・職務経歴書への一覧ページが表示されます
* `resume.html` / `work.html` を直接開いて確認することもできます
* GitHub Pages で公開すれば、ブラウザだけでいつでも確認できます

---

## 🌐 GitHub Pages の設定方法

このリポジトリには `.github/workflows/deploy.yml` が含まれており、`main` ブランチへの push をきっかけに自動でビルド・デプロイされる仕組みになっています。  
初回のみ、リポジトリ側で公開設定を行ってください。

### 1. main ブランチにマージする

`deploy.yml` は `main` ブランチへの push（＝ PR のマージ）をトリガーに動作します。  
作業ブランチで変更をコミットしたら、PR を作成して `main` にマージしてください。

```bash
git add .
git commit -m "update resume data"
git push origin <作業ブランチ名>
```

push後、GitHub上でPRを作成し、`main` ブランチへマージしてください。  
マージが完了すると、その push をきっかけに GitHub Actions が起動し、公開用ファイルが自動でデプロイされます。

### 2. Actions の実行を確認する

GitHub リポジトリの **「Actions」** タブを開き、「Deploy to GitHub Pages」に緑色のチェックマーク（成功）が付いていることを確認してください。  
初回は反映までに数十秒〜数分かかることがあります。失敗している場合は、ログを開いて原因を確認してください。

### 3. Pages の公開ブランチを設定する（初回のみ）

1. リポジトリの **「Settings」** → 左メニューの **「Pages」** を開く
2. 「Build and deployment」の **Source** を **「Deploy from a branch」** に設定する
3. **Branch** を **`gh-pages`**、フォルダは **`/ (root)`** にして **Save** を押す

> 🔍 `gh-pages` ブランチが選択肢に出てこない場合、まだ一度も Actions のデプロイが成功していない可能性があります。先に手順1・2を行い、`gh-pages` ブランチが作成された状態にしてから設定してください。

### 4. 公開URLを確認する

設定が完了すると、Pages の画面上部に公開URLが表示されます。通常は次の形式です。

```text
https://<ユーザー名>.github.io/<リポジトリ名>/
```

---

## ⚠️ 編集時の注意

* 文字列は `"` または `'` で囲んでください
* 項目の区切りには `,` が必要です
* 配列（`[ ]`）に要素を追加する場合も、`,` 区切りを忘れないでください
* PDF出力は、各ページ右下の「PDF出力 / 印刷」ボタンから行えます
