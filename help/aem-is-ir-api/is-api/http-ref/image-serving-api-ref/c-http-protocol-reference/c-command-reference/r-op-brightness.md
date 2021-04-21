---
description: 明るさを調整 画像の明るさを増減します。
solution: Experience Manager
title: op_brightness
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
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
