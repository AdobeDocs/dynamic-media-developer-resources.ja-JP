---
description: 彩度を調整する。 レイヤーまたは合成画像の各可視ピクセルの彩度を変更します。
solution: Experience Manager
title: op_saturation
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: cd71e27e-6ccc-4ade-9bcf-af8e41bcf381
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---

# op_saturation{#op-saturation}

彩度を調整する。 レイヤーまたは合成画像の各可視ピクセルの彩度を変更します。

`op_saturation= *`adj`*`

<table id="simpletable_5F118A28FE674B06A16F6F19C56B4594"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>彩度の調整(-100...+100 int)。 </p></td> 
 </tr> 
</table>

`op_saturation=-100` 画像の彩度を完全に下げます。

## プロパティ {#section-9a3cc9ff060049449554dfa69d92fd53}

レイヤコマンド `layer=comp`の場合は、現在のレイヤーまたは合成画像に適用されます。 エフェクトレイヤでは無視されます。

## 初期設定 {#section-ef0e78f55c8b4d22aee09104dad6410a}

`op_saturation=0`（彩度の変更なし）。CMYK画像またはレイヤーは、操作が適用される前にRGBに変換されます。

## 例 {#section-033b272f1b7e4efeb94e841fd8095357}

カラー写真を操作して「ハイキー」な外観を実現する：

`http://server/myRootId/myImageId?op_saturation=-60&op_brightness=45&op_contrast=-35`
