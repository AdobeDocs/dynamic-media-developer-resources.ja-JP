---
description: マテリアルサーフェス光沢度 マテリアルサーフェスの相対光沢度を指定します。 照明マップを選択し、光沢効果と3D反射のレンダリングを制御するために使用します。
solution: Experience Manager
title: 光沢
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 6df6cd05-9462-4c1e-a7ac-efac3461cf11
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 1%

---

# 光沢{#gloss}

マテリアルサーフェス光沢度 マテリアルサーフェスの相対光沢度を指定します。 照明マップを選択し、光沢効果と3D反射のレンダリングを制御するために使用します。

`gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>デフォルト（参照）の光沢値は、光沢(0...100%)または —1です。 </p></td> 
 </tr> 
</table>

光沢の値が高いと、通常は強く、シャープな反射が生じ、ビネットで光沢効果が有効になると、主に照明のコントラストを大きくすることで、マテリアルサーフェスの鏡面反射光ハイライトが強くなります。 各マテリアルタイプ( `type=` )は、最小と最大のレンダリング効果を定義します。 壁紙などの材料の種類によっては、`gloss=`はレンダリング効果の外観にほとんど影響を与えませんが、他の材料の種類（石やセラミックなど）では、効果が大幅に顕著になります。

`illum=-1`でビネットが複数のイルミネーションマップを定義している場合、 `gloss=`は現在のレンダリング操作に使用するイルミネーションマップを選択します。 レンダラーは、指定された光沢に最も近い光沢値を持つ照明マップを選択します。

`gloss=-1` ビネットのビュープロパティで定義されている、選択した照明マップの参照光沢値を選択します。これにより、光沢効果が有効になっていても、さらに修正を加えることなく、作成したとおりに照明マップが使用されます。 `illum=-1`の場合は、ビネットビューの第1照明マップの基準光沢値を使用します。

## プロパティ {#section-92c20c7890fc4aad8d1725d1a1f82da6}

マテリアル属性。 ビネットが複数の照明マップを定義しない場合や`illum=`が指定されている場合、ビネットに3D反射データが含まれていない場合、または現在のオブジェクトが3D反射をサポートしていない場合、またはビネットで光沢効果が無効な場合は無視されます。

## 初期設定 {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` マテリアルがカタログエントリに基づいている場合は、それ以外の場合は、既定の照明マップまたはで指定された照明マップの参照光沢値 `illum=`。

## 関連項目 {#section-29f5b761481a4c52a499a2e16e63c70b}

[attribute::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb)、 [type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35)、 [rough=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180)、 [glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a)、 [illum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)
