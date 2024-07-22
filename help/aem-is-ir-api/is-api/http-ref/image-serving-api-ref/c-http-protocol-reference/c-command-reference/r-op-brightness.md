---
title: op_brightness
description: 明るさを調整します。 画像の明るさを増減します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 390ed812-87ae-41e7-8021-65dd95915ae8
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 2%

---

# op_brightness{#op-brightness}

明るさを調整します。 画像の明るさを増減します。

`op_brightness= *`adj`*`

<table id="simpletable_2B5DB95B1FF044C8BD226D4F8311E806"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>明るさの調整（–100...+100 整数） </p></td> 
 </tr> 
</table>

## プロパティ {#section-c7e757f63b2c4b5ebaacbadb51c72ce4}

[ 画層 ] コマンド： 現在のレイヤーまたは合成イメージ（`layer=comp` の場合）に適用されます。 エフェクトレイヤーで無視されます。 CMYK 画像またはレイヤーは、操作が適用される前にRGBに変換されます。

## 初期設定 {#section-be56be0759634c79b4f264f194a94dbc}

明るさを変更しない場合は、`op_brightness=0` をクリックします。

## 例 {#section-c25f952f1b77409abb9ccf885862d75c}

画像の背景を少し暗くして、前景コンテンツを強調します。

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_brightness=-10&layer=1&src=myRootId/myImageId`
