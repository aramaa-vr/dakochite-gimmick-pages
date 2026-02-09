---
title: 画像整理レビュー（dakochite）
description: docs/assets/img/dakochite 配下の利用実態をもとにした最適構成レビュー。
nav_exclude: true
---

# 画像整理レビュー（dakochite）

## 結論

提案されていた以下の方針は、**現状データに対して妥当**です。

- 複数ページで使うものを `common` に置く
- 個別ページ専用はページ別ディレクトリに置く
- 未使用は別フォルダに隔離する

ただし、運用を安定させるために、以下の3階層を推奨します。

```text
docs/assets/img/dakochite/
  common/
  pages/
    install/
    setup/
    play/
    quest/
    troubleshooting/
  _unused/
    2026-02-09/
```

## 検証結果（実データ）

- 画像総数: 50
- 使用中: 48
- 未使用: 2
  - `announcement.webp`
  - `vcc-avatar-project.webp`

### 複数ファイルから参照される画像（common候補）

- `hero.webp`
  - `index.md`
  - `_includes/head_custom.html`（OG/Twitter画像）

> 現状で「複数参照」は `hero.webp` のみ。

### ページ専用画像の分類

- `install.md` 専用
  - `vcc-*`, `install-unitypackage-*`, `ma-version-error.webp`, `vrcc_repo_opt_q82.webp`
- `setup.md` 専用
  - `tool-*`
- `play.md` 専用
  - `menu-*`, `grab-*`
- `quest.md` 専用
  - `questtools-*`
- `troubleshooting.md` 専用
  - `settings-*`, `issue-*`

## 「本当に最適か」の評価

### 現時点で最適な理由

1. **探索コストが最小化**される
   - どのページの画像かを `pages/<slug>/` で即判断できる。
2. **保守時の影響範囲が明確**
   - ページ更新時に同階層だけ見ればよい。
3. **未使用管理が安全**
   - いきなり削除せず `_unused/<date>/` へ退避できる。

### 補足ルール（最適化ポイント）

- `common` は「参照数2以上」だけでなく、**サイト共通責務（OG/ブランド）**を含める。
- 新規画像は原則 `pages/<slug>/` に置き、再利用が発生した時だけ `common` へ昇格。
- `_unused` は一定期間（例: 30〜90日）後に削除。

## 実施順（移行する場合）

1. ディレクトリ作成
2. 画像移動
3. `docs/*.md` と `docs/_includes/head_custom.html` の参照パス更新
4. `rg '/assets/img/dakochite/' docs -n` でリンク切れ確認

