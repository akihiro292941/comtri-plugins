# crm-writer（ネタ帳の書く係）

コントリの CRM のネタ帳で「書く」を押したネタを、お使いの PC の Claude Code が下書きまで書いて片づけるプラグインです。

## しくみ

```
ネタ帳で「書く」 → CRM の順番待ち
PC の Claude に「ネタ帳の書くを片づけて」
  → CRM からネタを1件受け取る（会社の言葉・物語・使わない言葉・発信ルールも一緒に）
  → 下書きを書く → 発信ルールで調べて直す
  → ブログは CRM が WordPress に「下書き」で入れる／SNS は CRM のカードの中に置く
  → ネタ帳のネタが「下書き」になる
公開は、ご自身で下書きを読んで WordPress で押します（AI は公開しません）
```

- PC に置くのは、CRM のアドレスと鍵（APIトークン）だけです。WordPress のパスワードは PC に置きません。
- 会社ごとの中身（らしさカルテ・発信ルール・出口）は CRM が持っています。このプラグインには書く流れだけが入っています。
- 頼んだときだけ動きます。PC をつけっぱなしにする必要はありません。

## 入れ方

1. Claude Code を入れて、ご自身の Claude のアカウントでログインします。
2. Claude Code で次の2つを入力します。
   ```
   /plugin marketplace add akihiro292941/comtri-plugins
   /plugin install crm-writer@comtri
   ```
3. 入れるときに聞かれる3つを入れます（あとから `/plugin` → crm-writer → Configure で直せます）。
   - CRM のアドレス（例 `https://crm.example.jp`）
   - CRM の鍵（CRM の「設定 > API」で発行した `crm_` で始まるもの。入力は伏せて保存されます）
   - この PC で書く出口（例 `代表ブログ,SNS`）
4. 週に1回くらい、Claude に「ネタ帳の書くを片づけて」と頼みます。

困ったときは、コントリの担当者にご連絡ください。
