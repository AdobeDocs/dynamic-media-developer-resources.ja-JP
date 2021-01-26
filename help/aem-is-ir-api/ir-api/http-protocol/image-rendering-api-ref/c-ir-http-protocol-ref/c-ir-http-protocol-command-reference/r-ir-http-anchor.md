---
description: 画像アンカー（ホットスポット） 繰り返し可能なテクスチャまたはデカールマテリアルのテクスチャアンカーポイント（ホットスポット）を指定します。
seo-description: 画像アンカー（ホットスポット） 繰り返し可能なテクスチャまたはデカールマテリアルのテクスチャアンカーポイント（ホットスポット）を指定します。
seo-title: アンカー
solution: Experience Manager
title: アンカー
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 1e695882-f97a-4208-b595-2851b91bdbfe
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 3%

---


# アンカー{#anchor}

画像アンカー（ホットスポット） 繰り返し可能なテクスチャまたはデカールマテリアルのテクスチャアンカーポイント（ホットスポット）を指定します。

`anchor= *``*, *`xy`*`

`anchorN= *``*, *`xnyn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>,  <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>ソース画像の左上隅からのピクセルオフセット（整数、整数）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>,  <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>ソース画像の中心からの正規化されたオフセット(real、real)。 </p></td> 
 </tr> 
</table>

繰り返し可能なテクスチャは、ビネットオブジェクトに適用され、テクスチャのアンカーポイント(`anchor=`)がオブジェクトのテクスチャ接触チャネルポイントに配置されます。

デカールのアンカーポイントがオブジェクトのデカールの接触チャネルポイントに配置されるように、デカールのイメージがビネットオブジェクトに適用されます。 デカールの位置は、`pos=`コマンドを使用してさらに調整できます。

`anchorN=0,0` ソース画像の中央に画像アンカーを配置します。`anchorN=-0.5,-0.5` または、 `anchor=0,0` が左上隅で、 `anchorN=0.5,0.5` がソース画像の右下隅にあります。

## プロパティ {#section-91f929d35cd745ab9e1eeecf45fcedae}

**マテリアル属性**。`align=2`の場合、またはマテリアルが繰り返し可能なテクスチャでない場合、壁紙、デカールでない場合は無視されます。

## 初期設定 {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`材料がカタログエントリに基づいている場合は、それ以外の場合は、繰り返し可能なテクスチャやウォールペーパーには`anchor=0,0`（イメージの左上隅）、デカールには`anchorN=0,0`（イメージの中心）が使用されます。

## 関連項目 {#section-b18bf0b035644ca5aedebbc64373718e}

[catalog::Anchor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) ,  [align=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
