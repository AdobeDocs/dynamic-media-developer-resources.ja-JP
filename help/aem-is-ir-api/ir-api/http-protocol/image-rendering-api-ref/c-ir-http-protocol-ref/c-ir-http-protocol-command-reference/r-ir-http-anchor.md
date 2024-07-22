---
title: アンカー
description: 画像アンカー（ホットスポット）。 繰り返し可能なテクスチャまたはデカール マテリアルのテクスチャのアンカーポイント（ホットスポット）を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2c5dce-6eb1-4f05-80bd-7336deb08b9e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 2%

---

# アンカー{#anchor}

画像アンカー（ホットスポット）。 繰り返し可能なテクスチャまたはデカール マテリアルのテクスチャのアンカーポイント（ホットスポット）を指定します。

`anchor= *`x`*, *`y`*`

`anchorN= *`xn`*, *`yn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>, <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>ソース画像の左上隅からのピクセルオフセット （int、int）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>, <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>ソース イメージの中心からの正規化されたオフセット（実際、実際）。 </p></td> 
 </tr> 
</table>

繰り返し可能なテクスチャがビネット オブジェクトに適用され、テクスチャのアンカーポイント（`anchor=`）がオブジェクトのテクスチャ原点に配置されます。

デカル転写イメージはビネット オブジェクトに適用されるため、デカル転写アンカーポイントはオブジェクトのデカル転写の原点に配置されます。 デカル転写の位置は、[`pos=`] コマンドを使用してさらに調整できます。

`anchorN=0,0` 画像アンカーをソース画像の中央に配置します。 `anchorN=-0.5,-0.5` または `anchor=0,0` は左上隅にあり、`anchorN=0.5,0.5` はソース画像の右下隅にあります。

## プロパティ {#section-91f929d35cd745ab9e1eeecf45fcedae}

**マテリアル属性**. `align=2` の場合、またはマテリアルが繰り返し可能なテクスチャ、壁紙、デカル転写でない場合は無視されます。

## 初期設定 {#section-b06d728c2f664c29bacf810eefcbde69}

材料がカタログエントリに基づいている場合は `catalog::Anchor` します。 それ以外の場合は、繰り返し可能なテクスチャと壁紙の場合は `anchor=0,0` （画像の左上隅）、デカールの場合は `anchorN=0,0` （画像の中央）を使用します。

## 関連項目 {#section-b18bf0b035644ca5aedebbc64373718e}

[catalog::Anchor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) , [align=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
