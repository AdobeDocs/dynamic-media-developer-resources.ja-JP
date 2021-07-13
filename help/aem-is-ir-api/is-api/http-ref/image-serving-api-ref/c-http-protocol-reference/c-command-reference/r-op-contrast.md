---
description: コントラストを調整する。 50%を超える明るさのピクセルの明るさを増やし、50%未満の明るさのピクセルの明るさを減らすことで、画像のコントラストを調整します。
solution: Experience Manager
title: op_contrast
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 0216f22e-a3b3-4dda-89c2-9c6c2c81cab3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---

# op_contrast{#op-contrast}

コントラストを調整する。 50%を超える明るさのピクセルの明るさを増やし、50%未満の明るさのピクセルの明るさを減らすことで、画像のコントラストを調整します。

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>コントラスト調整（パーセント単位）（ —100 ～ 100整数）。 </p></td> 
 </tr> 
</table>

## プロパティ {#section-d319ed55057344eab0a3c93f720acdbf}

レイヤコマンド `layer=comp`の場合は、現在のレイヤーまたは合成画像に適用されます。 エフェクトレイヤでは無視されます。

## 初期設定 {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`（コントラストは変わりません）。CMYK画像またはレイヤーは、操作が適用される前にRGBに変換されます。

## 例 {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

高画質の画像レイヤーのコントラストとシャープネスを減らし、低画質の背景写真と視覚的に一致させます。

... `&op_blur=3&op_contrast=-12&`

将来のリリースでは、50%の固定の明るさではなく、画像の中央値の明るさを使用する場合があります。
