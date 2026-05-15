---
title: 有効期限
description: デフォルトのクライアントキャッシュの有効期間。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6d9cca06-f675-4ae4-a187-9cd716e7c554
TQID: 'https://experienceleague.adobe.com/UkPYVP3aAoseZcXo5zLTVIiejTIPv5HXHekcIgS-B4U'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 4%

---

# 有効期限{#expiration}

デフォルトのクライアントキャッシュの有効期間。 特定のカタログレコードに有効な`catalog::Expiration`または`vignette::Expiration`値が含まれていない場合に備えて、デフォルトの有効期限を指定します。 または、ビネットファイルまたはマテリアルファイルに直接アクセスする場合は、カタログレコードを使用する必要はありません。

## プロパティ {#section-8e2bade105ec4905ae5c4911f500279f}

実数（`0`以上）。 返信データが生成されてから有効期限が切れるまでの時間数。 `0`に設定すると、返信画像が常にすぐに期限切れになり、クライアントのキャッシュが効果的に無効になります。 `-1`に設定すると、*期限切れになりません*&#x200B;としてマークされます。

## 初期設定 {#section-18cfce46edb441bfae7dd9d3e0217ba9}

定義されていない場合や空の場合は、`default::Expiration`から継承されます。

## 関連項目 {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[&#x200B; カタログ：：有効期限](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)、[周辺光量補正：：有効期限](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
