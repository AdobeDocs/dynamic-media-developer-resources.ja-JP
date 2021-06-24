---
description: クライアントキャッシュの有効期間。 有効期限が切れるまでの時間数。 クライアントおよびプロキシサーバーのキャッシュを管理するために使用します。
solution: Experience Manager
title: 有効期限
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 5717d568-467e-495b-b963-9b3d42e866a6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 4%

---

# 有効期限{#expiration}

クライアントキャッシュの有効期間。 有効期限が切れるまでの時間数。 クライアントおよびプロキシサーバーのキャッシュを管理するために使用します。

詳細は` [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)`を参照。

## プロパティ {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

実数、-2、-1、0以上。 応答イメージが生成されてから有効期限が切れるまでの時間数。 0に設定すると、常に応答イメージの有効期限が即座に切れ、クライアントのキャッシュが効果的に無効になります。 -1に設定して`never expire`とマークします。この場合、サーバーは常に、条件付き`GET`リクエストに対して、ファイルが実際に変更されたかどうかを確認せずに403ステータスを返します。 `attribute::Expiration`が提供するデフォルトを使用するには、-2に設定します。

## 初期設定 {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` が使用されるのは、フィールドが存在しない場合、値が —2の場合、またはフィールドが空の場合です。

## 関連項目 {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[attribute::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) 、 [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)、 [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
