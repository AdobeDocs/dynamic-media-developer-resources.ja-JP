---
description: マテリアルの表面粗さ。 マテリアルサーフェスの相対的な粗さを指定します。
solution: Experience Manager
title: 粗い
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 8903b51c-c7d4-460f-8f28-00053eac9d6e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---

# 粗い{#rough}

マテリアルの表面粗さ。 マテリアルサーフェスの相対的な粗さを指定します。

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>表面粗さ(0...100%)または —1：デフォルトの粗さを選択します。 </p> </td> 
 </tr> 
</table>

3D反射レンダリング効果を制御するために使用します。 粗さの値を小さくすると、通常は滑らかな反射効果が得られます。値を大きくすると、反射したイメージのランダム化と散乱が生じます。

各マテリアルタイプ( `type=` )は、粗さに基づいて、最小および最大の反射レンダリング効果を定義します。 壁紙などの材料の種類によっては、`rough=`は反射の外観にほとんど影響を与えず、他の材料の種類（石やセラミックなど）では、効果は実質的に顕著です。

`rough=-1` 粗さを、サーバ内部の既定値（一般的なマテリアルタイプでは40%）に設定します。

## プロパティ {#section-515375758b254c80af576271bdb61bb8}

マテリアル属性。 ビネットに3D反射機能がない場合、ターゲットオブジェクトに3Dジオメトリが関連付けられていない場合、またはターゲットオブジェクトがシーン内の他のオブジェクトを反映していない場合は無視されます。

## 初期設定 {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` 材料がカタログエントリに基づいている場合は、それ以外の場合は約40%です。

## 関連項目 {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) ,  [gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
