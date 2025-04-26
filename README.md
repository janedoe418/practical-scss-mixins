## Practical SCSS Mixins

A practical SCSS mixin library focused on responsive design and real-world development needs.  
_(If you're working in the hell, this is for you.)_

## About

このライブラリは、日々の開発現場で本当に使える**SCSS mixin**を集めたものです。  
スマホファースト設計、一部古いブラウザ向けのフォールバックも考慮しています。  
PCとSPのデザインデータが先に作られている（Tailwindなどのフレームワークを使わない）現場向きです。  

No more "hello world" mixins — just practical tools.  
Each SCSS file also includes English comments for easier understanding and customization.

---

## Structure

```
scss/
  00_global/
    _variables.scss
    _index.scss
    mixin/
      _hover.scss
      _lineclamp.scss
      _math.scss
      _mq.scss
      _transition.scss
      _extras.scss
      _index.scss
```

- `variables` : カラーパレットや共通変数
- `mixin/` : 各種mixin
- `_index.scss` : 各mixinをまとめて`@forward`しているので、`00_global`単位で読み込み可能

---

## How to Use

```scss
// 例：プロジェクト側で
@use "path/to/00_global" as glob;

.foo {
  @include glob.hover {
    color: red;
  }
}
```

> 必要なmixinだけインポートして使うスタイル推奨。

---

## Notes

- このリポジトリはmixinの提供のみが目的です。
- スタイル全体のビルド用ファイル（style.scssなど）は含まれません。
- テスト用コードは含まず、**自分のプロジェクトに取り込んで使ってください**。

---

## License

MIT License  
自由に改変してください。ただし責任は自己負担で。