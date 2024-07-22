---
title: 粗い
description: 材料表面の粗さ。 材料表面の相対粗さを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8903b51c-c7d4-460f-8f28-00053eac9d6e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---

# 粗い{#rough}

材料表面の粗さ。 材料表面の相対粗さを指定します。

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>表面粗さ（0...100%）または–1 を指定して、デフォルトの粗さを選択します。 </p> </td> 
 </tr> 
</table>

3D 反射レンダリング効果を制御するために使用します。 粗さの値を小さくすると、一般的に反射エフェクトが滑らかになります。値を大きくすると、反射イメージがランダム化され、散乱します。

各マテリアル タイプ（`type=`）は、粗さに基づいて反射レンダリング効果の最小値と最大値を定義します。 壁紙などの一部のマテリアル タイプでは、反射の外観に対す `rough=` 影響は最小限ですが、石やセラミックなどの他のマテリアル タイプでは、効果がかなり顕著です。

`rough=-1` 粗さをサーバ内部の既定値（一般的なマテリアル タイプの場合は 40%）に設定します。

## プロパティ {#section-515375758b254c80af576271bdb61bb8}

マテリアル アトリビュート。 ビネットに 3D 反射機能がない場合、ターゲット オブジェクトに 3D ジオメトリが関連付けられていない場合、またはターゲット オブジェクトがシーン内の他のオブジェクトを反射していない場合は、無視されます。

## 初期設定 {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` 材料がカタログエントリに基づいている場合、それ以外の場合は約 40%。

## 関連項目 {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35) , [gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
