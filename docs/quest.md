---
title: Quest対応（VRCQuestTools）
description: VRCQuestToolsでQuest向けに変換する手順と、よくある制約・回避策。
nav_order: 5
---

# Quest対応（VRCQuestTools）

同梱説明書の「10, Quest対応」に記載されている内容を、手順としてまとめたページです。

説明書では **クロツグミ様の VRCQuestTools** を利用する方法が案内されています。  
- Booth: [https://booth.pm/ja/items/2436054](https://booth.pm/ja/items/2436054)

---

## 手順（説明書の記載）

1. **PC版アバターを先にアップロード** して、正常に動作することを確認します（説明書）。
2. **VRCQuestTools を起動** します。

![VRCQuestTools起動]({{ site.baseurl }}/assets/img/dakochite/questtools-launch.webp)

3. `HoldGimickAndCamera` の以下のボーンを入れる、と説明書に記載があります。

![ボーン選択]({{ site.baseurl }}/assets/img/dakochite/questtools-bone-select.webp)

4. **変換する**（説明書）。

![変換]({{ site.baseurl }}/assets/img/dakochite/questtools-convert.webp)

---

## パーティクルをきれいにしたい場合（説明書の記載）

自動生成された `Assets/VRCQuestToolsOutput/アバターの名前/Materials` 内のマテリアル設定を、  
**「VRChat/Mobile/Particle Additive」** に変更するよう案内されています。

![生成マテリアル]({{ site.baseurl }}/assets/img/dakochite/questtools-materials.webp)
![Mobile/Particle Additive]({{ site.baseurl }}/assets/img/dakochite/questtools-mobile-shader.webp)
![例]({{ site.baseurl }}/assets/img/dakochite/questtools-material-example.webp)

---

## 注意

説明書の注意書き:

- **Quest版は「だこちて視点On」を利用できません。**

![Quest版では視点On不可]({{ site.baseurl }}/assets/img/dakochite/questtools-no-viewpoint.webp)

---

## アップデート後に Quest版をアップロードできない時

説明書の記載（要旨）:

- 基本は **PC用からVRCQuestToolsで作り直す** のが良い。
- 時間がない場合は、以下の部分（パーティクル、音、カメラ）を **EditorOnly** にするとビルドが通る、と説明書にあります。

![Hierarchy例]({{ site.baseurl }}/assets/img/dakochite/questtools-hierarchy-editoronly.webp)
![EditorOnly設定例1]({{ site.baseurl }}/assets/img/dakochite/questtools-editoronly-mark.webp)
![EditorOnly設定例2]({{ site.baseurl }}/assets/img/dakochite/questtools-editoronly-mark2.webp)

