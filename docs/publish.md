---
title: 公開（GitHub Pages）
description: GitHub Pages（docs/）でこの説明サイトを公開する手順。
nav_order: 12
---

# 公開（GitHub Pages）

このリポジトリは **`docs/` フォルダを GitHub Pages の公開ソース** にする構成です（Jekyll / just-the-docs）。

> GitHubのUI表記は変更されることがあります。ここでは「どこを設定すれば公開できるか」だけを整理しています。

---

## 1. GitHub Pages の公開元を `docs/` にする

1. GitHub のリポジトリ画面で **Settings** を開きます。
2. 左メニューの **Pages** を開きます。
3. Source（公開元）で、
   - Branch: `main`（または利用している既定ブランチ）
   - Folder: `/docs`
   を選びます。

---

## 2. `_config.yml` の `baseurl` を公開URLに合わせる

`docs/_config.yml` に次が入っています。

```yml
url: "https://aramaa-vr.github.io"
baseurl: ""
```

- 自分のGitHub IDが `aramaa-vr` ではない場合は `url` を変更します。
- 公開URLが `https://<USER>.github.io/<REPO>/` の場合は `baseurl` を `"/<REPO>"` にします。
- カスタムドメインやユーザー/組織ページ（`https://<USER>.github.io/`）で公開する場合は `baseurl` を空にします。

---

## 3. 公開後に画像が出ない時

多くの場合、`baseurl` が公開URLのパスと一致していないのが原因です。  
`docs/_config.yml` を確認して、公開URLのパスと合わせてください。
