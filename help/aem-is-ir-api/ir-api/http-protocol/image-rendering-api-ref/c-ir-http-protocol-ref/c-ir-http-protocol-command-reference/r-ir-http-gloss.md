---
title: 光沢
description: マテリアル サーフェスの光沢。 マテリアル サーフェスの相対的な光沢を指定します。 照明マップを選択し、光沢効果と 3D 反射のレンダリングを制御するために使用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6df6cd05-9462-4c1e-a7ac-efac3461cf11
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# 光沢{#gloss}

マテリアル サーフェスの光沢。 マテリアル サーフェスの相対的な光沢を指定します。 照明マップを選択し、光沢効果と 3D 反射のレンダリングを制御するために使用します。

`gloss= *`val`*`

<table id="simpletable_82166CA080AD401180404462FB2407D7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>グロス（0...100%）または–1 （デフォルト（参照）グロス値） </p></td> 
 </tr> 
</table>

一般的に、光沢値を大きくすると、より強くシャープな反射が得られます。また、光沢効果をビネットで有効にすると、主に照明コントラストを高めることによって、マテリアル表面の鏡面反射光ハイライトが強くなります。 各マテリアル タイプ（`type=`）は、最小および最大のレンダリング効果を定義します。 壁紙などの一部のマテリアル タイプでは、レンダリング効果の外観に対す `gloss=` 影響は最小限ですが、石やセラミックなどの他のマテリアル タイプでは、レンダリング効果が大幅に顕著になります。

ビネットが複数のイルミネーション マップを定義している場合、`gloss=` は現在のレンダリング操作に使用するイルミネーション マップを `illum=-1` 択します。 レンダラーは、指定された光沢に最も近い光沢値を持つ照明マップを選択します。

`gloss=-1` 選択した照明マップの参照光沢値を選択します。この値は、ビネットのビュープロパティで定義されています。 この値を使用すると、光沢効果が有効な場合でも、作成したとおりに正確に照明マップが使用され、さらに変更が加えられることはありません。 `illum=-1` の場合、ビネットビューの最初の照明マップの参照光沢値が使用されます。

## プロパティ {#section-92c20c7890fc4aad8d1725d1a1f82da6}

マテリアル アトリビュート。 ビネットに複数の照明マップが定義されていない場合は無視されます。 `illum=` が指定されている場合、ビネットに 3D 反射データが含まれていないとき。 または、現在のオブジェクトが 3D 反射をサポートしていない場合や、ビネットで光沢効果が無効になっている場合です。

## 初期設定 {#section-3722fb5f85c24bc29bdf9c92ce04e678}

`attribute::Gloss` マテリアルがカタログ エントリに基づいている場合は、既定値の照明マップまたは `illum=` で指定された照明マップの参照光沢値。

## 関連項目 {#section-29f5b761481a4c52a499a2e16e63c70b}

[attribute::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb)、[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35)、[rough=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180)、[glossmap=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a)、[illum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-illum.md#reference-8efe483a30684022bfe711eb73efbee6)
