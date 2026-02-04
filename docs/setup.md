---
title: アバターに入れる（セットアップ）
description: Unityのセットアップツールで生成・削除し、アップロードまで行う手順。
nav_order: 3
---

# アバターに入れる（セットアップ）

だこちてギミックは、Unity上の **セットアップツール** でアバターへ生成します。

- ツールメニュー: `Aramaa/dakochite gimmick みんなでつかめるだこちてギミック`
- ボタン: **「ギミックを生成 / 削除」**  
  - ツール内のツールチップには「既にギミックがある場合は削除される」と記載があります（`GimickConstants`）。

---

## 1. ツールを開く

![ツールの場所]({{ site.baseurl }}/assets/img/dakochite/tool-menu.webp)

---

## 2. 競合対策（PhysBoneつきギミックを一緒に動かしたい場合）

説明書では「だこちてギミックと一緒に動かしたいギミック（PhysBone付き）をドラッグ&ドロップで設定できる」とあります。

![競合対策の設定]({{ site.baseurl }}/assets/img/dakochite/tool-conflict-dnd.webp)

---

## 3. ギミックを生成する

1. だこちてギミックを入れたいアバターを選んで、ツールで対象に指定します（説明書の手順画像）。

![アバターを指定]({{ site.baseurl }}/assets/img/dakochite/tool-select-avatar.webp)

2. **「ギミックを生成 / 削除」** を実行します。  
   - 説明書では、生成時にダイアログで **OK** を押す手順が記載されています。

![生成ダイアログ]({{ site.baseurl }}/assets/img/dakochite/tool-generate-dialog.webp)

3. セットアップ完了の例（説明書の表示例）。

![セットアップ完了]({{ site.baseurl }}/assets/img/dakochite/tool-done.webp)

> 説明書には「以下の改変を行った時など、PhysBoneをアバターに追加した際は再度セットアップしてください」と記載があります。  
> つまり **アバター側のPhysBone構成を変えたら、もう一度生成** が推奨されています。

---

## 4. アップロード

説明書では「GestureManagerなどでUnity上で一度プレイして動作確認後、いつものようにアップロード」と書かれています。

---

## 5. 削除したいとき

説明書では「ツールの『ギミックを生成 / 削除』をクリックすると削除される」と記載があります。

![削除]({{ site.baseurl }}/assets/img/dakochite/tool-delete.webp)

---

## 補足（内部の名称 / 生成物）

以下は **実装上の名称** です（トラブルシュート時の目印）。  
※仕様として保証するものではなく、バージョンで変わる可能性があります。

- ギミックプレハブ名: `HoldGimickAndCamera`（`GimickConstants.HOLD_GIMMICK_NAME`）
- PhysBone自動化のパラメータ名: `HoldType`（`GimickConstants.PHYSBONE_PARAMETER_NAME`）
- 生成アセットの出力パス（例）: `Assets/Aramaa/GeneratedAssets/...`（`GimickConstants.PHYSBONE_OUTPUT_BASE_PATH`）

