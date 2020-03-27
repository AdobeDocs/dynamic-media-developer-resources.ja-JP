---
description: 画像アンカー（ホットスポット） 繰り返し可能なテクスチャまたはデカールマテリアルのテクスチャアンカーポイント（ホットスポット）を指定します。
seo-description: 画像アンカー（ホットスポット） 繰り返し可能なテクスチャまたはデカールマテリアルのテクスチャアンカーポイント（ホットスポット）を指定します。
seo-title: アンカー
solution: Experience Manager
title: アンカー
topic: Scene7 Image Serving - Image Rendering API
uuid: 1e695882-f97a-4208-b595-2851b91bdbfe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# アンカー{#anchor}

画像アンカー（ホットスポット） 繰り返し可能なテクスチャまたはデカールマテリアルのテクスチャアンカーポイント（ホットスポット）を指定します。

`anchor= *``*, *`xy`*`

`anchorN= *`シニ`*, *`ン`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>、 <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>ソース画像の左上隅からのピクセルオフセット（整数、整数）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>, <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>ソース画像の中心からの正規化されたオフセット（実数、実数）。 </p></td> 
 </tr> 
</table>

繰り返し可能なテクスチャは、ビネットオブジェクトに適用され、テクスチャのアンカーポイント( `anchor=`)がオブジェクトのテクスチャの原点に配置されます。

デカールのアンカーポイントがオブジェクトのデカールの原点に配置されるように、デカールのイメージがビネットオブジェクトに適用されます。 デカール位置は、コマンドを使用してさらに調整で `pos=` きます。

`anchorN=0,0` ソース画像の中央に画像アンカーを配置します。 `anchorN=-0.5,-0.5` また `anchor=0,0` は、がソース画像の左上隅 `anchorN=0.5,0.5` 、および右下隅にある場合。

## プロパティ {#section-91f929d35cd745ab9e1eeecf45fcedae}

**マテリアル属性**。 マテリアルが `align=2`繰り返し可能なテクスチャ、壁紙、デカールでない場合は無視されます。

## 初期設定 {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`に基づくマテリアルの場合は、 それ以外 `anchor=0,0` の場合は、（イメージの左上隅）が繰り返し可能なテクスチャとウォールペーパー、 `anchorN=0,0` （イメージの中心）がデカールになります。

## 関連項目 {#section-b18bf0b035644ca5aedebbc64373718e}

[catalog::Anchor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) , [align=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
