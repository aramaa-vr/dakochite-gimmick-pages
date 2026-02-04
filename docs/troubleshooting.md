---
title: トラブルシューティング
description: つかめない時の設定見直し、MissingReferenceException、既知の注意点まとめ。
nav_order: 6
---

# トラブルシューティング

同梱説明書（HTML）の「6, つかめない時に見直す設定」「8, 不具合」を元に、よくある詰まりどころをまとめています。

---

## 1) つかめない／抱っこできない時（設定の見直し）

### 自分の設定例（説明書）

説明書では、以下のメニューを確認する例が載っています。

- **大きなメニュー → アバター → アバターインタラクション**

![アバターインタラクション]({{ site.baseurl }}/assets/img/dakochite/settings-avatar-interaction.webp)

「相手が自分を掴めるか」を可視化する例として、説明書に画像が掲載されています。

![可視化1]({{ site.baseurl }}/assets/img/dakochite/settings-visualize1.webp)
![可視化2]({{ site.baseurl }}/assets/img/dakochite/settings-visualize2.webp)

### 相手側にしてもらう設定（説明書）

説明書では「抱っこしてもらいたい相手のステータスを見る」→（条件により）相手側に設定をお願いする必要がある、と書かれています。

![相手のステータス]({{ site.baseurl }}/assets/img/dakochite/settings-other-status.webp)
![相手にお願いする例]({{ site.baseurl }}/assets/img/dakochite/settings-other-ask.webp)

相手側にお願いする項目として、説明書には次が記載されています。

- **Show アバター** をお願いする
- **アバターインタラクション設定の上書き** をお願いする

![Showアバター]({{ site.baseurl }}/assets/img/dakochite/settings-other-show-avatar.webp)
![上書き]({{ site.baseurl }}/assets/img/dakochite/settings-other-override.webp)

---

## 2) 既知の不具合・注意点（説明書）

### PhysBoneつきギミックとの競合

- 説明書: 「耳の子などのPhysBoneを含んだギミックと競合する」  
- 説明書: 「1.0.5から競合するギミックを除外するリストを追加」

（対策として、セットアップツールに「一緒に動かしたいギミックを設定する」項目があることも、説明書「5, アバターにギミックを入れる方法」に記載されています）

---

### セットアップ時エラー（MissingReferenceException）

説明書の記載（要旨）:

- `MissingReferenceException` が稀に発生することがある  
- 対応方法: **Unityを終了して再起動** するとエラーが消える

![MissingReferenceException例1]({{ site.baseurl }}/assets/img/dakochite/issue-missingreference1.webp)
![MissingReferenceException例2]({{ site.baseurl }}/assets/img/dakochite/issue-missingreference2.webp)

---

### Hipのメッシュが飛び出る（AvatarPoseSystemと併用）

説明書の記載（要旨）:

- AvatarPoseSystem と一緒に入れると、抱っこした際にHipのメッシュが飛び出る場合がある  
- 対応方法: AvatarPoseSystem を最新にすると共存できる、とテスター報告がある

![Hipのメッシュ例]({{ site.baseurl }}/assets/img/dakochite/issue-hip-mesh.webp)

---

### 抱っこ視点の制約（説明書）

説明書の記載（要旨）:

- ミラーには未対応  
- デスクトップでは上下にしか視点移動できない  
- 3点トラッキングでは、頭を左右に回転しすぎると意図しない動作をする可能性があるため、上下移動を推奨

---

### プレハブの破損（古いパッケージ→VCC更新）

説明書の記載（要旨）:

- 古いパッケージ（1.0.0以前）がある状態で VCC に更新すると、プレハブが破損する  
- 対応方法: ツールで **削除→再生成**（アバターごとに一回）

![プレハブ破損の例]({{ site.baseurl }}/assets/img/dakochite/issue-prefab-broken.webp)

---

### 近づくと相手が見えなくなる

説明書の記載:

- 対応方法: **パーソナルスペースをOFF** にする

![パーソナルスペース]({{ site.baseurl }}/assets/img/dakochite/issue-personal-space.webp)

