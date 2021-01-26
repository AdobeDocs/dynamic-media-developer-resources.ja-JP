---
description: マテリアルの表面粗さ。 マテリアルサーフェスの相対的な粗さを指定します。
seo-description: マテリアルの表面粗さ。 マテリアルサーフェスの相対的な粗さを指定します。
seo-title: 粗い
solution: Experience Manager
title: 粗い
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d3b4ece1-cc2a-4012-ad81-2f313d3a370b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 2%

---


# rough{#rough}

マテリアルの表面粗さ。 マテリアルサーフェスの相対的な粗さを指定します。

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>表面粗さ(0 ～ 100 %)または —1を指定して、既定の粗さを選択します。 </p> </td> 
 </tr> 
</table>

3D反射レンダリング効果を制御するために使用します。 粗さの値を小さくすると、通常は滑らかな反射効果が得られます。この値を大きくすると、反射した画像のランダム化と散乱が発生します。

各マテリアルタイプ( `type=` )は、粗さに基づいて最小および最大の反射レンダリング効果を定義します。 材料の種類（例えば壁紙）によっては、`rough=`は反射の外観にほとんど影響を与えませんが、他の材料の種類（例えば、石やセラミック）では、効果が大幅に顕著になります。

`rough=-1` では、荒さをサーバ内部の既定値に設定します（標準的なマテリアルタイプでは40 %）。

## プロパティ {#section-515375758b254c80af576271bdb61bb8}

マテリアル属性 ビネットに3D反射機能がない場合、ターゲットオブジェクトに3Dジオメトリが関連付けられていない場合、またはターゲットオブジェクトにシーン内の他のオブジェクトが反映されていない場合は、無視されます。

## 初期設定 {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` 材料がカタログエントリを基にしている場合は、それ以外の場合は約40%です。

## 関連項目 {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) 、 [gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
