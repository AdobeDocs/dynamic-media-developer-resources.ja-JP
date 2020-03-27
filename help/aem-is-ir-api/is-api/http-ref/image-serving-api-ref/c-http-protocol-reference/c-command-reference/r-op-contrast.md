---
description: コントラストを調整 50%を超える明るさのピクセルの明るさを増やし、50%未満の明るさのピクセルの明るさを減らして、画像のコントラストを調整します。
seo-description: コントラストを調整 50%を超える明るさのピクセルの明るさを増やし、50%未満の明るさのピクセルの明るさを減らして、画像のコントラストを調整します。
seo-title: op_contrast
solution: Experience Manager
title: op_contrast
topic: Scene7 Image Serving - Image Rendering API
uuid: d17b0b49-792b-41ce-a154-5e7635c9ab43
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_contrast{#op-contrast}

コントラストを調整 50%を超える明るさのピクセルの明るさを増やし、50%未満の明るさのピクセルの明るさを減らして、画像のコントラストを調整します。

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>コントラスト調整(%)(-100 ～ 100 int)。 </p></td> 
 </tr> 
</table>

## プロパティ {#section-d319ed55057344eab0a3c93f720acdbf}

レイヤーコマンド 現在のレイヤーまたは合成画像（の場合）に適用されま `layer=comp`す。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`の場合は、コントラストを変更しません。 CMYK画像またはレイヤーは、操作の適用前にRGBに変換されます。

## 例 {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

高画質の画像レイヤーのコントラストとシャープを下げて、低画質の背景写真に合わせます。

… `&op_blur=3&op_contrast=-12&`

将来のリリースでは、50 %の明るさを固定するのではなく、画像の明るさの中央値を使用する場合があります。
