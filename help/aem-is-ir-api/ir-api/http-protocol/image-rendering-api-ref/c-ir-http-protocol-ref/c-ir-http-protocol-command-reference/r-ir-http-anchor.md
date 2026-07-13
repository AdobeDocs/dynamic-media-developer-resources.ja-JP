---
title: アンカー
description: '画像アンカー（ホットスポット）: 繰り返し可能なテクスチャまたはデカール マテリアルのテクスチャ アンカーポイント（ホットスポット）を指定します。'
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2c5dce-6eb1-4f05-80bd-7336deb08b9e
TQID: 'https://experienceleague.adobe.com/fw1-eDsdT8jsgJfXBzb2bsLlcuTxKdLUmIeD5cFDiFE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 202
ht-degree: 2%

---

# アンカー{#anchor}

画像アンカー（ホットスポット）: 繰り返し可能なテクスチャまたはデカール マテリアルのテクスチャ アンカーポイント（ホットスポット）を指定します。

`anchor= *`x`*, *`y`*`

`anchorN= *`xn`*, *`yn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>、<span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>ソース画像の左上隅からのピクセルオフセット（int、int）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>、<span class="varname">yn</span> </p></td> 
  <td class="stentry"> <p>ソース画像の中心からの正規化されたオフセット（実数、実数）。 </p></td> 
 </tr> 
</table>

繰り返し可能なテクスチャが周辺光量補正オブジェクトに適用され、テクスチャ アンカーポイント（`anchor=`）がオブジェクトのテクスチャの起点に配置されます。

周辺光量補正オブジェクトにデカール画像が適用され、デカール アンカーポイントがオブジェクトのデカール原点に配置されます。 デカールの位置は、`pos=` コマンドを使用してさらに調整できます。

`anchorN=0,0`画像アンカーをソース画像の中央に配置します。 `anchorN=-0.5,-0.5`または`anchor=0,0`は左上隅にあり、`anchorN=0.5,0.5`はソース画像の右下隅にあります。

## プロパティ {#section-91f929d35cd745ab9e1eeecf45fcedae}

**マテリアル属性**。 `align=2`の場合、またはマテリアルが繰り返し可能なテクスチャ、壁紙、デカールでない場合は無視されます。

## 初期設定 {#section-b06d728c2f664c29bacf810eefcbde69}

資料がカタログ エントリに基づいている場合、`catalog::Anchor`。 それ以外は、繰り返し可能なテクスチャと壁紙の場合は`anchor=0,0` （画像の左上隅）、デカールの場合は`anchorN=0,0` （画像の中央）です。

## 関連項目 {#section-b18bf0b035644ca5aedebbc64373718e}

[catalog::Anchor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) , [align=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)

