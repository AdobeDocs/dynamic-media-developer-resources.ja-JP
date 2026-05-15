---
title: ラフ
description: 材料表面の粗さ： マテリアル サーフェスの相対的な粗さを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8903b51c-c7d4-460f-8f28-00053eac9d6e
TQID: 'https://experienceleague.adobe.com/FhLagzJwQodPihSxkEyBl8zSnEU0gDq0zevixYMApUY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 182
ht-degree: 1%

---

# ラフ{#rough}

材料表面の粗さ： マテリアル サーフェスの相対的な粗さを指定します。

` rough= *`val`*`

<table id="simpletable_432E33EC87144AC7A2A8D9406F862708"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>サーフェスの粗さ（0...100%）または–1を指定して、デフォルトの粗さを選択します。 </p> </td> 
 </tr> 
</table>

3D リフレクションレンダーエフェクトの制御に使用します。 ラフネス値が小さいと、通常は反射効果が滑らかになります。値が大きいほど、反射画像のランダム化と拡散が生じます。

各マテリアルタイプ（`type=`）は、ラフネスに基づいて最小および最大の反射レンダリングエフェクトを定義します。 一部のマテリアルタイプ（壁紙など）では、`rough=`が反射の外観に与える影響は最小限ですが、他のマテリアルタイプ（石やセラミックなど）では、効果は大幅に顕著です。

`rough=-1`粗さをサーバー内部のデフォルト値（一般的なマテリアル タイプの場合は40%）に設定します。

## プロパティ {#section-515375758b254c80af576271bdb61bb8}

マテリアル属性： ビネットに3D反射機能がない場合、ターゲット オブジェクトに3D ジオメトリが関連付けられていない場合、またはターゲット オブジェクトがシーン内の他のオブジェクトを反射していない場合は、無視されます。

## 初期設定 {#section-11861a5e6e8649ee988267d2707fd7cc}

`catalog::Roughness` マテリアルがカタログ エントリに基づいている場合、そうでない場合は約40%。

## 関連項目 {#section-d232fff7237443cc95c4bb50cb3d32bb}

[type=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35)、[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
