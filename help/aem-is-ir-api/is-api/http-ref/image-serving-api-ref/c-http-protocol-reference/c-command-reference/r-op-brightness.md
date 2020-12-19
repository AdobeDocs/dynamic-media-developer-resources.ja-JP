---
description: 明るさを調整 画像の明るさを増減します。
seo-description: 明るさを調整 画像の明るさを増減します。
seo-title: op_brightness
solution: Experience Manager
title: op_brightness
topic: Scene7 Image Serving - Image Rendering API
uuid: 751ec9e5-4a70-438d-950c-deff4db034b1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 3%

---


# op_brightness{#op-brightness}

明るさを調整 画像の明るさを増減します。

`op_brightness= *`adj`*`

<table id="simpletable_2B5DB95B1FF044C8BD226D4F8311E806"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>明るさの調整（ —100 ～ 100整数） </p></td> 
 </tr> 
</table>

## プロパティ {#section-c7e757f63b2c4b5ebaacbadb51c72ce4}

レイヤーコマンド `layer=comp`の場合は、現在のレイヤーまたは合成画像に適用されます。 エフェクトレイヤーでは無視されます。 CMYK画像またはレイヤーは、操作の適用前にRGBに変換されます。

## 初期設定 {#section-be56be0759634c79b4f264f194a94dbc}

`op_brightness=0`（明るさを変えない）。

## 例 {#section-c25f952f1b77409abb9ccf885862d75c}

画像の背景を少し暗くして、前景のコンテンツを強調します。

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
