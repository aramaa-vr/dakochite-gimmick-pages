---
title: アバターに入れる（セットアップ）
description: Unityのセットアップツールで生成・削除し、アップロードまで行う手順。
nav_order: 3
---

# アバターに入れる（セットアップ）

だこちてギミックは、Unity上の **セットアップツール** でアバターへ生成します。

- ツールメニュー: `Aramaa/dakochite gimmick みんなでつかめるだこちてギミック`
- ボタン: **「ギミックを生成 / 削除」**  
  - 既にギミックがある場合は削除されます。

---

## 1. ツールを開く

![ツールの場所]({{ "/assets/img/dakochite/pages/setup/tool-menu.webp" | relative_url }})

---

## 2. 競合対策（PhysBoneつきギミックを一緒に動かしたい場合）

だこちてギミックと一緒に動かしたいギミック（PhysBone付き）をドラッグ&ドロップで設定できます。

![競合対策の設定]({{ "/assets/img/dakochite/pages/setup/tool-conflict-dnd.webp" | relative_url }})

---

## 3. ギミックを生成する

1. だこちてギミックを入れたいアバターを選んで、ツールで対象に指定します。

![アバターを指定]({{ "/assets/img/dakochite/pages/setup/tool-select-avatar.webp" | relative_url }})

2. **「ギミックを生成 / 削除」** を実行します。  
   - 生成時にダイアログで **OK** を押します。

![生成ダイアログ]({{ "/assets/img/dakochite/pages/setup/tool-generate-dialog.webp" | relative_url }})

3. セットアップ完了の例。

![セットアップ完了]({{ "/assets/img/dakochite/pages/setup/tool-done.webp" | relative_url }})

> 以下の改変を行った時など、PhysBoneをアバターに追加した際は再度セットアップしてください。  
> つまり **アバター側のPhysBone構成を変えたら、もう一度生成** が推奨されています。

---

## 4. アップロード

GestureManagerなどでUnity上で一度プレイして動作確認後、いつものようにアップロードしてください。

---

## 5. 削除したいとき

ツールの『ギミックを生成 / 削除』をクリックすると削除されます。

![削除]({{ "/assets/img/dakochite/pages/setup/tool-delete.webp" | relative_url }})

---

## 補足（内部の名称 / 生成物）

以下は **実装上の名称** です（トラブルシュート時の目印）。  
※仕様として保証するものではなく、バージョンで変わる可能性があります。

- ギミックプレハブ名: `HoldGimickAndCamera`（`GimickConstants.HOLD_GIMMICK_NAME`）
- PhysBone自動化のパラメータ名: `HoldType`（`GimickConstants.PHYSBONE_PARAMETER_NAME`）
- 生成アセットの出力パス（例）: `Assets/Aramaa/GeneratedAssets/...`（`GimickConstants.PHYSBONE_OUTPUT_BASE_PATH`）

