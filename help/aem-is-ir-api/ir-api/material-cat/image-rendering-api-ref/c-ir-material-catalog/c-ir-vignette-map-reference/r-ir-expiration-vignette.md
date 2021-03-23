---
description: クライアントキャッシュの有効期間。 有効期限が切れるまでの時間数。 クライアントおよびプロキシサーバーのキャッシュを管理するために使用します。
seo-description: クライアントキャッシュの有効期間。 有効期限が切れるまでの時間数。 クライアントおよびプロキシサーバーのキャッシュを管理するために使用します。
seo-title: 有効期限
solution: Experience Manager
title: 有効期限
uuid: fa267728-9a36-4705-97d6-d567148fc2d7
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 4%

---


# 有効期限{#expiration}

クライアントキャッシュの有効期間。 有効期限が切れるまでの時間数。 クライアントおよびプロキシサーバーのキャッシュを管理するために使用します。

詳細は` [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)`を参照してください。

## プロパティ {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

実数、-2、-1、0以上 応答画像が生成されてから有効期限切れになるまでの時間数。 0に設定すると、応答イメージが直ちに期限切れになります。これにより、クライアントのキャッシュが効果的に無効になります。 -1に設定して`never expire`とマークします。この場合、サーバーは常に条件付き`GET`要求に応答して403ステータスを返し、ファイルが実際に変更されたかどうかは確認しません。 `attribute::Expiration`が提供するデフォルト値を使用するには、-2に設定します。

## 初期設定 {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` は、フィールドが存在しない場合、値が —2の場合、またはフィールドが空の場合に使用されます。

## 関連項目 {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[attribute::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
