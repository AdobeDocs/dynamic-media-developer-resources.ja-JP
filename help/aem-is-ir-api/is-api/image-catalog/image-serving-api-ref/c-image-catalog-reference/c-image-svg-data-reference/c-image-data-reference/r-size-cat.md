---
description: 画像サイズ： カタログパスで参照されるフル解像度イメージのピクセルサイズ。
solution: Experience Manager
title: サイズ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f06cbb-d70f-4334-966c-624b49c3bb9b
TQID: 'https://experienceleague.adobe.com/wS28XEIvINBBoYZSI-frpSbCikCyC5AhT6TyDgMsGFg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 5%

---

# サイズ{#size}

画像サイズ： カタログ：:Pathで参照されるフル解像度イメージのピクセルサイズ。

この値が指定されている場合、画像サービングでは、実際の画像サイズを取得するために画像を開く必要がないようにするためにこの値が使用されます。

>[!NOTE]
>
>`catalog::Size`が指定されていて、実際の全解像度の画像サイズと同じでない場合、未定義の動作が発生する可能性があります。

## プロパティ {#section-5c914ec8b1444a8e99d811b647cd42a3}

0より大きい2つの整数値をコンマで区切ります。 オプション。

## 初期設定 {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

フィールドが存在しない場合、またはフィールドが空の場合は、画像の実際のサイズが使用されます。

## 関連項目 {#section-e63797357d5a4119a10db1e6e088f6e9}

[&#x200B; カタログ：：パス &#x200B;](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c)、[res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
