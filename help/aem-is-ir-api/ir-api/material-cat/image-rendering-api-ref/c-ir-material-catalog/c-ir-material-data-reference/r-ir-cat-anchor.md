---
description: 画像アンカー： 繰り返し可能なテクスチャ、壁の境界線、デカール画像のアンカーポイント（ホットスポット）を指定します。
solution: Experience Manager
title: アンカー
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1336330e-86e5-418d-bea3-0c09368e3528
TQID: 'https://experienceleague.adobe.com/-TWQdh61Hkdr81vXooodDafEwQHTMvQdSQSf--HuPIg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 161
ht-degree: 3%

---

# アンカー{#anchor}

画像アンカー： 繰り返し可能なテクスチャ、壁の境界線、デカール画像のアンカーポイント（ホットスポット）を指定します。

繰り返し可能なテクスチャが周辺光量補正オブジェクトに適用され、テクスチャのアンカーポイントがオブジェクトのテクスチャの起点に配置されます。 デカール画像がビネット オブジェクトに適用され、デカール アンカーポイントがオブジェクトのデカール原点に配置されます。 壁の境界の場合は、x値のみが使用されます。y値は無視されます。

## プロパティ {#section-bc4bc8b897c64535b88681e57d72942f}

2つの整数。コンマで区切ります。 画像の左上隅を基準としたピクセルオフセット。 `catalog::Alignment=3`と単色およびキャビネットのマテリアルでは無視されます。

## 初期設定 {#section-b7ccc419a356415294706cd295ae96c9}

フィールドが空であるか存在しない場合は、繰り返し可能なテクスチャ素材の画像の左上隅（0,0）が使用されるか、デカール素材の場合は画像の中心が使用されます。

## 関連項目 {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[&#x200B; カタログ：：線形](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399)、[&#x200B; アンカー=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)

