---
title: トラブルシューティング
description: つかめない時の設定見直し、MissingReferenceException、既知の注意点まとめ。
nav_order: 6
---

# トラブルシューティング

よくある詰まりどころをまとめています。

---

## 1) つかめない／抱っこできない時（設定の見直し）

### 自分の設定例

以下のメニューを確認してください。

- **大きなメニュー → アバター → アバターインタラクション**

![アバターインタラクション]({{ "/assets/img/dakochite/pages/troubleshooting/settings-avatar-interaction.webp" | relative_url }})

「相手が自分を掴めるか」を可視化する例

![可視化1]({{ "/assets/img/dakochite/pages/troubleshooting/settings-visualize1.webp" | relative_url }})
![可視化2]({{ "/assets/img/dakochite/pages/troubleshooting/settings-visualize2.webp" | relative_url }})

### 相手側にしてもらう設定

「抱っこしてもらいたい相手のステータスを見る」→（条件により）相手側に設定をお願いする必要があります。

![相手のステータス]({{ "/assets/img/dakochite/pages/troubleshooting/settings-other-status.webp" | relative_url }})
![相手にお願いする例]({{ "/assets/img/dakochite/pages/troubleshooting/settings-other-ask.webp" | relative_url }})

相手側にお願いする項目

- **Show アバター** をお願いする
- **アバターインタラクション設定の上書き** をお願いする

![Showアバター]({{ "/assets/img/dakochite/pages/troubleshooting/settings-other-show-avatar.webp" | relative_url }})
![上書き]({{ "/assets/img/dakochite/pages/troubleshooting/settings-other-override.webp" | relative_url }})

---

## 2) 既知の不具合・注意点

### PhysBoneつきギミックとの競合

- <a href="{{ site.baseurl }}{% link setup.md %}">アバターに入れる（セットアップ）</a> の競合対策（PhysBoneつきギミックを一緒に動かしたい場合）を確認してください

---

### セットアップ時エラー（MissingReferenceException）

- `MissingReferenceException` が稀に発生することがある  
- 対応方法: **Unityを終了して再起動** するとエラーが消える

![MissingReferenceException例1]({{ "/assets/img/dakochite/pages/troubleshooting/issue-missingreference1.webp" | relative_url }})
![MissingReferenceException例2]({{ "/assets/img/dakochite/pages/troubleshooting/issue-missingreference2.webp" | relative_url }})

---

### Hipのメッシュが飛び出る（AvatarPoseSystemと併用）

- AvatarPoseSystem と一緒に入れると、抱っこした際にHipのメッシュが飛び出る場合がある  
- 対応方法: AvatarPoseSystem を最新にすると共存できる、とテスター報告がある

![Hipのメッシュ例]({{ "/assets/img/dakochite/pages/troubleshooting/issue-hip-mesh.webp" | relative_url }})

---

### 抱っこ視点の制約

- ミラーには未対応  
- デスクトップでは上下にしか視点移動できない  
- 3点トラッキングでは、頭を左右に回転しすぎると意図しない動作をする可能性があるため、上下移動を推奨

---

### プレハブの破損（古いパッケージ→VCC更新）

- 古いパッケージ（1.0.0以前）がある状態で VCC に更新すると、プレハブが破損する  
- 対応方法: ツールで **削除→再生成**（アバターごとに一回）

![プレハブ破損の例]({{ "/assets/img/dakochite/pages/troubleshooting/issue-prefab-broken.webp" | relative_url }})

---

### 近づくと相手が見えなくなる

- 対応方法: **パーソナルスペースをOFF** にする

![パーソナルスペース]({{ "/assets/img/dakochite/pages/troubleshooting/issue-personal-space.webp" | relative_url }})

