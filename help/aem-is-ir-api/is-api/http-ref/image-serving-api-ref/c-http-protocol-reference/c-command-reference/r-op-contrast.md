---
description: コントラストを調整 50 %を超える明るさのピクセルの明るさを増やし、50 %を超える明るさのピクセルの明るさを減らして、画像のコントラストを調整します。
seo-description: コントラストを調整 50 %を超える明るさのピクセルの明るさを増やし、50 %を超える明るさのピクセルの明るさを減らして、画像のコントラストを調整します。
seo-title: op_contrast
solution: Experience Manager
title: op_contrast
topic: Scene7 Image Serving - Image Rendering API
uuid: d17b0b49-792b-41ce-a154-5e7635c9ab43
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 1%

---


# op_contrast{#op-contrast}

コントラストを調整 50 %を超える明るさのピクセルの明るさを増やし、50 %を超える明るさのピクセルの明るさを減らして、画像のコントラストを調整します。

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>コントラスト調整（パーセント単位）(-100 ～ 100 int) </p></td> 
 </tr> 
</table>

## プロパティ {#section-d319ed55057344eab0a3c93f720acdbf}

レイヤーコマンド `layer=comp`の場合は、現在のレイヤーまたは合成画像に適用されます。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`の場合は、コントラストを変更しません。CMYK画像またはレイヤーは、操作の適用前にRGBに変換されます。

## 例 {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

高画質の画像レイヤーのコントラストとシャープを低くして、低画質の背景の写真と視覚的に一致させます。

... `&op_blur=3&op_contrast=-12&`

将来のリリースでは、50 %の固定の明るさではなく、画像の中央値の明るさが使用される場合があります。
