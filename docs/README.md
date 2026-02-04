# dakochite-gimmick Docs

このフォルダは「みんなでつかめるだこちてギミック」のドキュメントサイト (GitHub Pages) 用の Jekyll ソースです。
テーマは just-the-docs を使用しています。

## ローカルで表示を確認する

### 1) Ruby/Jekyll が使える場合

```bash
bundle install
bundle exec jekyll serve --livereload
```

### 2) Docker / CI などで静的ビルドだけしたい場合

```bash
./build-docs.sh
```

上記コマンドは、`../.docs-site` に静的サイトを出力します。
必要に応じて `python -m http.server` などでプレビューしてください。
