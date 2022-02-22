---
title: アンカー
description: 画像アンカー（ホットスポット） 繰り返し可能なテクスチャまたはデカールマテリアルのテクスチャアンカーポイント（ホットスポット）を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2c5dce-6eb1-4f05-80bd-7336deb08b9e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 3%

---

# アンカー{#anchor}

画像アンカー（ホットスポット） 繰り返し可能なテクスチャまたはデカールマテリアルのテクスチャアンカーポイント（ホットスポット）を指定します。

`anchor= *`x`*, *`y`*`

`anchorN= *`xn`*, *`yn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>, <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>ソース画像の左上隅からのピクセルオフセット（整数、整数）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>, <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>ソース画像の中心からの正規化されたオフセット（実数、実数）。 </p></td> 
 </tr> 
</table>

繰り返し可能なテクスチャがビネットオブジェクトに適用され、テクスチャのアンカーポイント ( `anchor=`) は、オブジェクトのテクスチャの原点にあります。

デカールのアンカーポイントがオブジェクトのデカールの原点にあるように、デカールイメージがビネットオブジェクトに適用されます。 デカールの位置は、 `pos=` コマンドを使用します。

`anchorN=0,0` 画像アンカーをソース画像の中央に配置します。 `anchorN=-0.5,-0.5` または `anchor=0,0` は左上隅にあり、 `anchorN=0.5,0.5` は、ソース画像の右下隅にあります。

## プロパティ {#section-91f929d35cd745ab9e1eeecf45fcedae}

**材料属性**. 次の場合は無視 `align=2`また、マテリアルが繰り返し可能なテクスチャでない場合、壁紙、デカール。

## 初期設定 {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`マテリアルがカタログエントリに基づいている場合は、 それ以外の場合は、 `anchor=0,0` 繰り返し可能なテクスチャや壁紙の場合は（画像の左上隅）、 `anchorN=0,0` （画像の中央）デカールの場合。

## 関連項目 {#section-b18bf0b035644ca5aedebbc64373718e}

[catalog::Anchor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) , [align=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
