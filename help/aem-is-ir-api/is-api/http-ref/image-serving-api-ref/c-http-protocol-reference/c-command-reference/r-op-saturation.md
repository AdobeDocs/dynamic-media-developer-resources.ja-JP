---
description: 彩度を調整 レイヤーまたは合成画像の各表示ピクセルの彩度を変更します。
seo-description: 彩度を調整 レイヤーまたは合成画像の各表示ピクセルの彩度を変更します。
seo-title: op_saturation
solution: Experience Manager
title: op_saturation
topic: Scene7 Image Serving - Image Rendering API
uuid: 5e987841-0c3b-4f68-96b1-fad8757f3402
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 2%

---


# op_saturation{#op-saturation}

彩度を調整 レイヤーまたは合成画像の各表示ピクセルの彩度を変更します。

`op_saturation= *`adj`*`

<table id="simpletable_5F118A28FE674B06A16F6F19C56B4594"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>彩度の調整（ —100 ～ 100整数） </p></td> 
 </tr> 
</table>

`op_saturation=-100` 画像の彩度を完全に下げます。

## プロパティ {#section-9a3cc9ff060049449554dfa69d92fd53}

レイヤーコマンド `layer=comp`の場合は、現在のレイヤーまたは合成画像に適用されます。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-ef0e78f55c8b4d22aee09104dad6410a}

`op_saturation=0`（彩度の変化なし）。CMYK画像またはレイヤーは、操作の適用前にRGBに変換されます。

## 例 {#section-033b272f1b7e4efeb94e841fd8095357}

カラー写真を操作して「ハイキー」な外観にします。

`http://server/myRootId/myImageId?op_saturation=-60&op_brightness=45&op_contrast=-35`
