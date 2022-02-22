---
title: 光沢
description: マテリアルサーフェス光沢度。 マテリアルサーフェスの相対光沢を指定します。 照明マップを選択し、光沢効果と 3D 反射のレンダリングを制御するために使用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6df6cd05-9462-4c1e-a7ac-efac3461cf11
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 1%

---

# 光沢{#gloss}

マテリアルサーフェス光沢度。 マテリアルサーフェスの相対光沢を指定します。 照明マップを選択し、光沢効果と 3D 反射のレンダリングを制御するために使用します。

`gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>デフォルト（参照）の光沢値の場合は、光沢 (0...100%) または —1。 </p></td> 
 </tr> 
</table>

光沢の値が大きいと、通常は強くシャープな反射が生じ、ビネットで光沢効果が有効になると、主に照明のコントラストを大きくすることで、マテリアルサーフェスのスペキュラハイライトが強化されます。 各マテリアルタイプ ( `type=`) は、最小と最大のレンダリング効果を定義します。 一部の材料タイプ（壁紙など）の場合、 `gloss=` レンダリング効果の外観への影響は最小限ですが、他のマテリアルタイプ（石やセラミックなど）の場合は、効果が大幅に顕著です。

If `illum=-1` ビネットが複数の照明マップを定義する場合は、 `gloss=` 現在のレンダリング操作に使用するイルミネーションマップを選択します。 レンダラーは、指定された光沢に最も光沢値が近い照明マップを選択します。

`gloss=-1` ビネットのビュープロパティで定義された、選択した照明マップの参照光沢値を選択します。 この値により、光沢効果が有効になっている場合でも、これ以上の変更を加えることなく、照明マップが作成したとおりに使用されます。 If `illum=-1` 次に、ビネットビューの第 1 照明マップの基準光沢値を使用する。

## プロパティ {#section-92c20c7890fc4aad8d1725d1a1f82da6}

材料属性。 ビネットで複数のイルミネーションマップが定義されていない場合は無視されます。 または、 `illum=` ビネットに 3D 反射データが含まれていない場合は、が指定されます。 または、現在のオブジェクトが 3D 反射をサポートしていない場合や、ビネットで光沢効果が無効な場合に使用できます。

## 初期設定 {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` マテリアルがカタログエントリに基づいている場合は、それ以外の場合は、既定の照明マップの参照光沢値、または `illum=`.

## 関連項目 {#section-29f5b761481a4c52a499a2e16e63c70b}

[attribute::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35), [rough=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180), [glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a), [illum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)
