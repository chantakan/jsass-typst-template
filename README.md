# JSASS 年会講演会の原稿

**[JSASS](https://smartconf.jp/content/57nenkai/paper) 年会講演会の原稿を [Typst](https://typst.app/) で書くための非公式テンプレート**

公式 Word テンプレートのレイアウトを再現しています。フォント同梱済み、clone してすぐ使えます。

## 使い方

```bash
git clone https://github.com/<your-username>/jsass-typst-template.git
cd jsass-typst-template
typst compile --font-path fonts jsass-57nenkai.typ
```

VS Code で使う場合は [Tinymist](https://marketplace.visualstudio.com/items?itemName=myriad-dreamin.tinymist) をインストールしてください。`.vscode/settings.json` 同梱済みなのでプレビューがそのまま動きます。

## 書き方

ファイル冒頭のユーザ設定を書き換えて、本文を書くだけです。

```typst
#let paper-id  = "1A01"
#let title-ja  = "あなたの論文タイトル"
#let title-en  = "Your Paper Title"

#let authors-ja = (
  (name: "山田太郎", presenter: true),
  (name: "鈴木花子", presenter: false),
)
#let affiliation-ja = "○○大学"
```

見出しは `=` / `==` / `===` で自動番号が付きます。

```typst
= はじめに           // → １．はじめに
= 手法               // → ２．手法
== 提案手法           // → ２－１　提案手法
=== アルゴリズム      // → ２－１－１　アルゴリズム
```

参考文献は `refs.bib` に追加して `@key` で引用すると `[1]` 形式で表示されます。

## ライセンス

テンプレート本体: MIT License

同梱フォント（`fonts/` 内にライセンス全文あり）:
- [Noto Serif CJK JP](https://github.com/notofonts/noto-cjk) — SIL Open Font License 1.1
- [TeX Gyre Termes](https://www.gust.org.pl/projects/e-foundry/tex-gyre) — GUST Font License
