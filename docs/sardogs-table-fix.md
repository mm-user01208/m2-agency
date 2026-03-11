# sardogs.net テーブル修正メモ

## 対象
- URL: https://sardogs.net/heathrow-airport-flight/index.html
- h3「ターミナル構成と航空会社」の表

## 修正内容
- 表の行の縦幅を縮小
- `.entry table td` のデフォルト padding: 9px 20px → 4px 20px に変更
- この表のみに適用するため、HTMLの表の直前に `<style>` ブロックを挿入

## 適用コード
```html
<style>
  table.location td,
  table.location th {
    padding: 4px 20px;
  }
</style>
```

## CSSの仕組み
- テーマCSS (page.css): `.entry table th, .entry table td { padding: 9px 20px; }`
- line-height: 2 (html root) × font-size 1.4rem = 28px
- 元の行高: 9 + 28 + 9 = 46px
- 修正後: 4 + 28 + 4 = 36px
