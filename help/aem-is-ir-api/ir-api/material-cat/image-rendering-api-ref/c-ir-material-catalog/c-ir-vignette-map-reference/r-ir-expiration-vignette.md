---
description: クライアントキャッシュの有効期限。 有効期限までの時間数。 クライアントおよびプロキシサーバーのキャッシュを管理するために使用します。
solution: Experience Manager
title: 有効期限
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5717d568-467e-495b-b963-9b3d42e866a6
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 3%

---

# 有効期限{#expiration}

クライアントキャッシュの有効期限。 有効期限までの時間数。 クライアントおよびプロキシサーバーのキャッシュを管理するために使用します。

詳しくは、[catalog::Expiration](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md) を参照してください。

## プロパティ {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

-2、-1、0 以上の実数。 応答画像が生成されてから有効期限が切れるまでの時間数。 常にレスポンスイメージの有効期限が直ちに切れるように 0 に設定すると、クライアントキャッシュが効果的に無効になります。 -1 に設定すると、`never expire` としてマークされます。この場合、サーバーは常に、条件付き `GET` リクエストに応答して 403 ステータスを返し、ファイルが実際に変更されたかどうかを確認しません。 `attribute::Expiration` が提供するデフォルトを使用するには、-2 に設定します。

## 初期設定 {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` は、フィールドが存在しない場合、値が–2 の場合、またはフィールドが空の場合に使用されます。

## 関連項目 {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[attribute::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996)、[catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)、[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
