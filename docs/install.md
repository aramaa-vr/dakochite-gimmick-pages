---
title: 導入（VCC / パッケージ）
description: VCC（VRChat Creator Companion）での導入手順と、ZIP/UnityPackage導入の注意点。
nav_order: 2
---

# 導入（VCC / パッケージ）

最短で導入したい方は、**方法1: VCCで導入（推奨）**を選んでください。  
このページは、迷いやすいポイント（追加済み表示・依存不足エラー）まで含めて順番に説明します。

---

## 最初にここだけ確認（1分）

- Unity: **2022.3.22f1**
- VCCで作成したアバタープロジェクト（`2022.3.22f1 avatar project`）
- 依存パッケージ
  - VRChat SDK: **3.10.1 以上**
  - Modular Avatar: **1.12.5 以上**

![VCCのUnityバージョン]({{ "/assets/img/dakochite/vcc-unity-version.webp" | relative_url }})

---

## 方法1: VCCで導入（推奨）

### 4ステップで完了

1. Add to VCC でリポジトリ追加
2. VCCで対象プロジェクトを開く
3. `dakochite-gimmick` を検索して追加
4. 以降はVCCでアップデート

---

### 1) Add to VCC でリポジトリ追加

以下のページを開いて、**Add to VCC** を押します。  
[https://aramaa-vr.github.io/vpm-repos/redirect.html](https://aramaa-vr.github.io/vpm-repos/redirect.html)

![VCCにリポジトリ追加]({{ "/assets/img/dakochite/vcc-add-repo.webp" | relative_url }})

#### 「すでに追加済み」と出る場合

`You have already added this repository. You can't add it again.` と表示されたら正常です。  
**追加は完了しているので、そのまま手順2へ進んでください。**

![Added]({{ "/assets/img/dakochite/vcc-settings-repo-added-q75.webp" | relative_url }})
![Confirm]({{ "/assets/img/dakochite/vcc-confirm.webp" | relative_url }})
![VCCリポジトリ追加（確認）]({{ "/assets/img/dakochite/vcc-add-repo-confirm.webp" | relative_url }})

---

### 2) 対象プロジェクトを開く

- `Settings → Packages → Installed Repositories` を開き、**aramaa にチェックがある**ことを確認
- 導入したいプロジェクトの **Manage Project** を押す

![Added]({{ "/assets/img/dakochite/vrcc_repo_opt_q82.webp" | relative_url }})
![Manage Project]({{ "/assets/img/dakochite/vcc-manage-project.webp" | relative_url }})

---

### 3) `dakochite-gimmick` を検索して追加

`dakochite-gimmick - みんなでつかめるだこちてギミック` を検索し、**「＋」** を押して追加します。

![検索して追加]({{ "/assets/img/dakochite/vcc-search-package.webp" | relative_url }})

---

### 4) 2回目以降のアップデート

導入後は、VCCのマネージャー画面から更新ボタンを押すだけでアップデートできます。

![VCCでアップデート]({{ "/assets/img/dakochite/vcc-update.webp" | relative_url }})

---

## 方法2: BoothのZIP / UnityPackageで導入

[Booth](https://aramaa.booth.pm/items/7016968) からダウンロードしたパッケージをUnityに直接インポートする方法です。  
**VCCが使える環境では方法1を推奨**します。

1. UnityPackageを開く
2. Import内容を確認
3. Importして完了

![パッケージを開く]({{ "/assets/img/dakochite/install-unitypackage.webp" | relative_url }})
![インポート確認]({{ "/assets/img/dakochite/install-unitypackage-import.webp" | relative_url }})
![インポート完了]({{ "/assets/img/dakochite/install-unitypackage-done.webp" | relative_url }})

---

## うまくいかないとき（よくあるケース）

### Modular Avatar不足エラー

`Modular Avatar 1.12.5以上` が入っていない場合、エラーが発生します。  
先にModular Avatarを導入・更新してから、再度だこちてギミックを追加してください。

![Modular Avatar バージョン不足の例]({{ "/assets/img/dakochite/ma-version-error.webp" | relative_url }})
