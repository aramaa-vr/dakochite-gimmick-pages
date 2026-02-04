---
title: 導入（VCC / パッケージ）
description: VCC（VRChat Creator Companion）での導入手順と、ZIP/UnityPackage導入の注意点。
nav_order: 2
---

# 導入（VCC / パッケージ）

このページは **インストール手順** をまとめたものです。  

---

## 事前準備（ここだけ確認）

- Unity: **2022.3.22f1**  
- VCCで作ったアバタープロジェクト「2022.3.22f1 avator project」  
- 依存パッケージ  
  - VRChat SDK: 3.10.1 以上  
  - Modular Avatar: 1.12.5 以上  

![VCCのUnityバージョン]({{ "/assets/img/dakochite/vcc-unity-version.webp" | relative_url }})

---

## 方法1: VCCでインストール（推奨）

1. **Add to VCC**  
   - 公式のリポジトリ追加ページから登録します。  
     - Add to VCC: [https://aramaa-vr.github.io/vpm-repos/redirect.html](https://aramaa-vr.github.io/vpm-repos/redirect.html)

![VCCにリポジトリ追加]({{ "/assets/img/dakochite/vcc-add-repo.webp" | relative_url }})
![VCCリポジトリ追加（確認）]({{ "/assets/img/dakochite/vcc-add-repo-confirm.webp" | relative_url }})
![Confirm]({{ "/assets/img/dakochite/vcc-confirm.webp" | relative_url }})

2. **プロジェクトに追加**  
   - VCCで、だこちてギミックを入れたいプロジェクトの **Manage Project** を開きます。

![Manage Project]({{ "/assets/img/dakochite/vcc-manage-project.webp" | relative_url }})

3. **検索してインストール**  
   - 「dakochite-gimmick - みんなでつかめるだこちてギミック」で検索 → 「＋」で追加します。

![検索して追加]({{ "/assets/img/dakochite/vcc-search-package.webp" | relative_url }})

4. **アップデート（以降）**  
   - インストール以降はVCCのマネージャーでボタンを押すだけでアップデートできます。

![VCCでアップデート]({{ "/assets/img/dakochite/vcc-update.webp" | relative_url }})

---

## 方法2: Boothのパッケージ（ZIP等）でインストール

[Booth](https://aramaa.booth.pm/items/7016968)のパッケージをインポートする手順

![パッケージを開く]({{ "/assets/img/dakochite/install-unitypackage.webp" | relative_url }})
![インポート確認]({{ "/assets/img/dakochite/install-unitypackage-import.webp" | relative_url }})
![インポート完了]({{ "/assets/img/dakochite/install-unitypackage-done.webp" | relative_url }})

> 注意: インストール以降はVCCのマネージャーでボタンを押すだけでアップデートできます。  
> ただし **パッケージ導入の更新手順** はプロジェクト構成に依存するため、迷ったら「VCC導入」をおすすめします。

---

## Modular Avatar が足りない場合のエラー

説明書には「Modular Avatar - 1.12.5以上が入っていないとエラーが発生」と記載があります。

![Modular Avatar バージョン不足の例]({{ "/assets/img/dakochite/ma-version-error.webp" | relative_url }})
