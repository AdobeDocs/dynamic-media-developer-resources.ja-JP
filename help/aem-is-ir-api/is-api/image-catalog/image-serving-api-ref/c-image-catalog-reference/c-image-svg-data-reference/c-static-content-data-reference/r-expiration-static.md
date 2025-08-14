---
title: 有効期限
description: クライアントおよびプロキシサーバーのキャッシュを管理するために使用します。 サーバは、この値を送信日時に加算することにより、HTTP 応答データの有効期限日時を算出する。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 064dab12-5f58-4e19-a6b1-fbd20182e3aa
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 1%

---

# 有効期限{#expiration}

クライアントおよびプロキシサーバーのキャッシュを管理するために使用します。 サーバは、この値を送信日時に加算することにより、HTTP 応答データの有効期限日時を算出する。

ブラウザーは、ファイルの有効期限を使用してキャッシュを管理します。 リクエストをサーバーに渡す前に、ブラウザーはキャッシュをチェックして、ファイルが既にダウンロードされているかどうかを確認します。 その場合、およびファイルの有効期限がまだ切れていない場合、ブラウザーは通常のGET リクエストではなく、条件付きGET リクエストを送信します（例えば、リクエストヘッダーの If-Modified-Since フィールドが設定されている場合）。 サーバーには、画像を送信せずに「304」ステータスで応答するオプションがあります。 次に、ブラウザーはキャッシュからファイルを読み込みます。 これにより、頻繁にアクセスされるデータの全体的なパフォーマンスが大幅に向上する可能性があります。

有効期限は、次の応答タイプに使用されます。

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

特定のタイプの応答（エラー応答など）は、常に即時の有効期限がマークされる（またはキャッシュ不可としてタグ付けされる）一方、他の応答（プロパティやデフォルトの画像応答など）は特別な有効期限設定（`attribute::NonImgExpiration` と `attribute::DefaultExpiration`）を使用します。

## プロパティ {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

-2、-1、0 以上の実数。 応答画像が生成されてから有効期限が切れるまでの時間数。 常に返信画像をすぐに期限切れにする場合は 0 に設定します。これにより、クライアントのキャッシュが効果的に無効になります。 -1 に設定すると、*`never expire`* としてマークされます。 この場合、条件付きGET リクエストに応じて、サーバーは常に 304 ステータス（未変更）を返します。ファイルが実際に変更されたかどうかを確認する必要はありません。 `attribute::Expiration` が提供するデフォルトを使用するには、-2 に設定します。

## 初期設定 {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` は、フィールドが存在しない場合、値が–2 の場合、またはフィールドが空の場合に使用されます。

## 関連項目 {#section-0e5e8595aad641c689726828712a8902}

[attribute::Expiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7), [attribute::DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf), [attribute::NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d), [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
