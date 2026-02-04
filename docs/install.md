---
title: 導入（VCC / パッケージ）
description: VCC（VRChat Creator Companion）での導入手順と、ZIP/UnityPackage導入の注意点。
nav_order: 2
---

# 導入（VCC / パッケージ）

このページは **インストール手順** をまとめたものです。  
（説明書 ver 1.1.2 と `package.json` の要件を元に記載しています。）

---

## 事前準備（ここだけ確認）

- Unity: **2022.3.22f1**（説明書と `package.json` で記載）
- VCC（VRChat Creator Companion）で作ったアバタープロジェクト（説明書表記: 「2022.3.22f1 avator project」）
- 依存パッケージ  
  - VRChat SDK（com.vrchat.avatars / com.vrchat.base）: >=3.8.2  
  - Modular Avatar: >=1.12.5 以上

![VCCのUnityバージョン]({{ site.baseurl }}/assets/img/dakochite/vcc-unity-version.webp)

---

## 方法1: VCCでインストール（推奨）

1. **Add to VCC**  
   - 公式のリポジトリ追加ページから登録します。  
     - Add to VCC: [https://aramaa-vr.github.io/vpm-repos/redirect.html](https://aramaa-vr.github.io/vpm-repos/redirect.html)

![VCCにリポジトリ追加]({{ site.baseurl }}/assets/img/dakochite/vcc-add-repo.webp)
![VCCリポジトリ追加（確認）]({{ site.baseurl }}/assets/img/dakochite/vcc-add-repo-confirm.webp)
![Confirm]({{ site.baseurl }}/assets/img/dakochite/vcc-confirm.webp)

2. **プロジェクトに追加**  
   - VCCで、だこちてギミックを入れたいプロジェクトの **Manage Project** を開きます。

![Manage Project]({{ site.baseurl }}/assets/img/dakochite/vcc-manage-project.webp)

3. **検索してインストール**  
   - 「dakochite-gimmick - みんなでつかめるだこちてギミック」で検索 → 「＋」で追加します。

![検索して追加]({{ site.baseurl }}/assets/img/dakochite/vcc-search-package.webp)

4. **アップデート（以降）**  
   - 説明書では「インストール以降はVCCのマネージャーでボタンを押すだけでアップデートできる」と記載されています。

![VCCでアップデート]({{ site.baseurl }}/assets/img/dakochite/vcc-update.webp)

---

## 方法2: パッケージ（ZIP等）でインストール

説明書では、パッケージをインポートする手順も記載されています。

![パッケージを開く]({{ site.baseurl }}/assets/img/dakochite/install-unitypackage.webp)
![インポート確認]({{ site.baseurl }}/assets/img/dakochite/install-unitypackage-import.webp)
![インポート完了]({{ site.baseurl }}/assets/img/dakochite/install-unitypackage-done.webp)

> 注意: 説明書では「インストール以降はVCCのマネージャーでボタンを押すだけでアップデートできる」とも書かれています。  
> ただし **パッケージ導入の更新手順** はプロジェクト構成に依存するため、迷ったら「VCC導入」をおすすめします。

---

## Modular Avatar が足りない場合のエラー

説明書には「Modular Avatar - 1.12.5以上が入っていないとエラーが発生」と記載があります。

![Modular Avatar バージョン不足の例]({{ site.baseurl }}/assets/img/dakochite/ma-version-error.webp)

---

## 参考

- `Assets/Aramaa/DakochiteGimmick/package.json`（Unity/依存関係/ドキュメントURL）
- 説明書（HTML）: 「5, アバターにギミックを入れる方法」→「0, 事前準備」「1, VCCでインストールする場合」「1, パッケージでインストールする場合」
