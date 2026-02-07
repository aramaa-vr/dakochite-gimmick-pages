---
title: 導入（VCC / パッケージ）
description: VCC（VRChat Creator Companion）での導入手順と、ZIP/UnityPackage導入の注意点。
nav_order: 2
---

# 導入（VCC / パッケージ）

最短で導入したい方は、**方法1: VCCで導入（推奨）**を選んでください。  
このページは、**迷わず完了できる順番**で説明しています。

---

## 最初にここだけ確認（1分）

- Unity: **2022.3.22f1**
- VCCで作成したアバタープロジェクト（例: `2022.3.22f1 avatar project`）
- 依存パッケージ
  - VRChat SDK: **3.10.1 以上**
  - [Modular Avatar](https://modular-avatar.nadena.dev/ja/): **1.12.5 以上** 

![VCCのUnityバージョン]({{ "/assets/img/dakochite/vcc-unity-version.webp" | relative_url }})

---

## 方法1: VCCで導入（推奨）

### 迷ったらこの4ステップ

1. Add to VCC でリポジトリ追加
2. VCCで対象プロジェクトを開く
3. `dakochite-gimmick` を検索して追加
4. 2回目以降はVCCで更新

> 目安時間: **3〜5分**

---

### 1) Add to VCC でリポジトリ追加

以下のページを開き、**Add to VCC** を押します。  
[https://aramaa-vr.github.io/vpm-repos/redirect.html](https://aramaa-vr.github.io/vpm-repos/redirect.html)

![VCCにリポジトリ追加する画面]({{ "/assets/img/dakochite/vcc-add-repo.webp" | relative_url }})

#### 「すでに追加済み」と表示された場合

`You have already added this repository. You can't add it again.` と表示される場合は、  
既にVCCにだこちてギミックが **追加済み** になります。  
なので、**手順2へ進んでください。**  

![VCCでリポジトリが追加済みと表示された画面]({{ "/assets/img/dakochite/vcc-settings-repo-added-q75.webp" | relative_url }})
![VCCで追加確認ダイアログが表示された画面]({{ "/assets/img/dakochite/vcc-confirm.webp" | relative_url }})

---

### 2) リポジトリの確認をする

- `Settings → Packages → Installed Repositories` で、**aramaa にチェックがある**ことを確認
- （チェックがないとリストに表示されません）

![VCCのInstalled Repositoriesでaramaaチェックを確認する画面]({{ "/assets/img/dakochite/vrcc_repo_opt_q82.webp" | relative_url }})

---

### 3) 対象プロジェクトを開く

- `Projects -> 導入したいプロジェクト` の **Manage Project** を押す
- そのまま **Manage Project 画面の Packages タブ**で、手順3の検索を行います

![VCCでManage Projectを開く画面]({{ "/assets/img/dakochite/vcc-manage-project.webp" | relative_url }})

---

### 4) `dakochite-gimmick` を検索して追加

`dakochite-gimmick - みんなでつかめるだこちてギミック` を検索し、**「＋」** を押して追加します。

![VCCでdakochite-gimmickを検索して追加する画面]({{ "/assets/img/dakochite/vcc-search-package.webp" | relative_url }})

![VCCリポジトリ追加の確認画面]({{ "/assets/img/dakochite/vcc-add-repo-confirm.webp" | relative_url }})

---

### 5) 2回目以降のアップデート

導入後は、VCCのマネージャー画面から更新ボタンを押すだけでアップデートできます。

![VCCでアップデートする画面]({{ "/assets/img/dakochite/vcc-update.webp" | relative_url }})

---

## 方法2: BoothのZIP / UnityPackageで導入

[Booth](https://aramaa.booth.pm/items/7016968) からダウンロードしたパッケージをUnityに直接インポートする方法です。  
**VCCが使える環境では方法1を推奨**します。

1. UnityPackageを開く
2. Importする
3. アップデート設定 

![Unityでパッケージを開く画面]({{ "/assets/img/dakochite/install-unitypackage.webp" | relative_url }})
![Unityでインポート内容を確認する画面]({{ "/assets/img/dakochite/install-unitypackage-import.webp" | relative_url }})

アップデートできるようにする
- Projects -> 導入したいプロジェクト の Manage Project -> Selected Repos -> Multiple Repositories -> aramaa をチェック
![Unityでインポートが完了した画面]({{ "/assets/img/dakochite/install-unitypackage-done.webp" | relative_url }})

---

## うまくいかないとき（よくあるケース）

まずは以下を確認してください。

- VRChat SDK が **3.10.1 以上** か
- Modular Avatar が **1.12.5 以上** か
- `Settings → Packages → Installed Repositories` で、**aramaa にチェックがある**か
- 追加先が目的のプロジェクトか（Manage Projectを開き間違えていないか）
- VCCを再起動し、Manage Projectを開き直したか

### Modular Avatar不足エラー

`Modular Avatar 1.12.5 以上` が入っていない場合、エラーが発生します。  
先にModular Avatarを導入・更新してから、再度だこちてギミックを追加してください。

![Modular Avatar バージョン不足エラーの例]({{ "/assets/img/dakochite/ma-version-error.webp" | relative_url }})
