---
description: マテリアルの表面粗さ。 マテリアルサーフェスの相対的な粗さを指定します。
seo-description: マテリアルの表面粗さ。 マテリアルサーフェスの相対的な粗さを指定します。
seo-title: 粗雑な
solution: Experience Manager
title: 粗雑な
topic: Scene7 Image Serving - Image Rendering API
uuid: d3b4ece1-cc2a-4012-ad81-2f313d3a370b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 粗雑な{#rough}

マテリアルの表面粗さ。 マテリアルサーフェスの相対的な粗さを指定します。

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>サーフェスの粗さ(0 ～ 100 %)または —1を指定して、既定の粗さを選択します。 </p> </td> 
 </tr> 
</table>

3D反射レンダリング効果を制御するために使用します。 粗さの値を小さくすると、通常は滑らかな反射効果が得られます。この値を大きくすると、反射された画像のランダム化と散乱が発生します。

各マテリアルタイプ( `type=`)では、粗さに基づいて、最小および最大の反射レンダリング効果を定義します。 一部の材料タイプ（壁紙など）では、反射の外観にほとんど影響を与えませんが、他の材料タイプ（石やセラミックなど）では、効果が大幅に顕著になります。 `rough=`

`rough=-1` では、粗さをサーバ内部の既定値（標準的なマテリアルタイプでは40%）に設定します。

## プロパティ {#section-515375758b254c80af576271bdb61bb8}

マテリアル属性。 ビネットに3D反射機能がない場合、ターゲットオブジェクトに3Dジオメトリが関連付けられていない場合、またはターゲットオブジェクトにシーン内の他のオブジェクトが反映されていない場合は無視されます。

## 初期設定 {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` 材料がカタログエントリを基にしている場合、それ以外の場合は約40%です。

## 関連項目 {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) , [gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
