---
description: クライアントキャッシュの稼働時間： 有効期限までの時間数。 クライアントおよびプロキシ サーバーのキャッシュの管理に使用します。
solution: Experience Manager
title: 有効期限
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5717d568-467e-495b-b963-9b3d42e866a6
TQID: 'https://experienceleague.adobe.com/VHARdBKoak-pB54FrPO6u0Gpmd-1sQZUF-78j3ixB2U'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 3%

---

# 有効期限{#expiration}

クライアントキャッシュの稼働時間： 有効期限までの時間数。 クライアントおよびプロキシ サーバーのキャッシュの管理に使用します。

詳しくは、[ カタログ：：有効期限](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md)を参照してください。

## プロパティ {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

実数、-2、-1、0以上。 応答イメージが生成されてから有効期限が切れるまでの時間数。 0に設定すると、応答イメージが即座に期限切れになり、クライアントのキャッシュが効果的に無効になります。 `never expire`としてマークするには–1に設定します。この場合、サーバーは常に403 ステータスを返します。このステータスは、条件付き`GET`要求に応答し、ファイルが実際に変更されたかどうかを確認しません。 `attribute::Expiration`が提供するデフォルトを使用するには、-2に設定します。

## 初期設定 {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration`は、フィールドが存在しない場合、値が–2の場合、またはフィールドが空の場合に使用されます。

## 関連項目 {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[属性：：有効期限](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996)、[ カタログ：：有効期限](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)、[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)

