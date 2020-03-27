---
description: マテリアルサーフェスの光沢 マテリアルサーフェスの相対的な光沢を指定します。 照明マップを選択し、光沢効果と3D反射のレンダリングを制御するために使用します。
seo-description: マテリアルサーフェスの光沢 マテリアルサーフェスの相対的な光沢を指定します。 照明マップを選択し、光沢効果と3D反射のレンダリングを制御するために使用します。
seo-title: 光沢
solution: Experience Manager
title: 光沢
topic: Scene7 Image Serving - Image Rendering API
uuid: 3774e08b-d24e-4cf2-8719-32a21bb9bcb6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 光沢{#gloss}

マテリアルサーフェスの光沢 マテリアルサーフェスの相対的な光沢を指定します。 照明マップを選択し、光沢効果と3D反射のレンダリングを制御するために使用します。

`gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>光沢(0...100%)または —1(既定（参照）の光沢値)。 </p></td> 
 </tr> 
</table>

一般に、光沢の値を高くすると、より強くシャープな反射が生じ、ビネットで光沢効果を有効にすると、主に照明のコントラストを高くして、マテリアルサーフェスの鏡面反射光ハイライトを強化します。 各マテリアルタイプ( `type=`)は、最小と最大のレンダリング効果を定義します。 一部のマテリアルタイプ（壁紙など）では、レンダリング効果の外観にほとんど影響を与えませんが、他のマテリアルタイプ（石やセラミックなど）では、効果が大幅に顕著になります。 `gloss=`

ビネット `illum=-1` が複数のイルミネーションマップを定義している場合、およびビネッ `gloss=` トが現在のレンダリング操作に使用するイルミネーションマップを選択します。 レンダラーは、指定された光沢に最も近い光沢値を持つ照明マップを選択します。

`gloss=-1` ビネットのビュープロパティで定義されている、選択した照明マップの参照光沢値を選択します。 これにより、光沢効果が有効になっていても、照明マップがオーサリングされた状態でそのまま使用され、さらに修正を加えることなくなります。 同様 `illum=-1` に、ビネットビューの最初の照明マップの参照光沢値も使用されます。

## プロパティ {#section-92c20c7890fc4aad8d1725d1a1f82da6}

マテリアル属性。 ビネットが複数の照明マップを定義しない場合、またはを指定した場合、ビネットに3D反射データが含まれない場合、または現在のオブジェクトが3D反射をサポートしない場合、またはビネットで光沢効果が無効な場合は無視されます。 `illum=`

## 初期設定 {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` マテリアルがカタログエントリに基づいている場合、それ以外の場合は、既定の照明マップまたはで指定された照明マップの参照光沢値 `illum=`。

## 関連項目 {#section-29f5b761481a4c52a499a2e16e63c70b}

[attribute::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35), [rough=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180), [glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a), [glossillum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)
