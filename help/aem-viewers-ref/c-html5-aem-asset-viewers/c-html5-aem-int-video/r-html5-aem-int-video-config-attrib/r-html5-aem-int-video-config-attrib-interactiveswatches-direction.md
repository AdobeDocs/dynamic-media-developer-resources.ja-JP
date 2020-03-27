---
description: インタラクティブビデオビューアの設定属性。
seo-description: インタラクティブビデオビューアの設定属性。
seo-title: InteractiveSwatches.direction
solution: Experience Manager
title: InteractiveSwatches.direction
topic: Dynamic media
uuid: 08095ab5-f74b-4da6-8f8d-df377995455e
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# InteractiveSwatches.direction{#interactiveswatches-direction}

インタラクティブビデオビューアの設定属性。

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p> ビュー内でのスウォッチの表示方法を指定します。 </p> <p>左から <span class="codeph"> 右へ </span> の入力順序を設定するには、leftに設定します。 </p> <p>右に設 <span class="codeph"> 定す </span> ると順序が逆になり、右から左、上から下の方向でビューが埋められます。 </p> <p>autoを設 <span class="codeph"> 定す </span> ると、ロケールが「ja」に設定されている場合はrightモードが適用 <span class="codeph"> され </span>ます。それ以外の場合 <span class="codeph"> は、left </span> が使用されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

（オプション）

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`auto`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
direction=right
```

