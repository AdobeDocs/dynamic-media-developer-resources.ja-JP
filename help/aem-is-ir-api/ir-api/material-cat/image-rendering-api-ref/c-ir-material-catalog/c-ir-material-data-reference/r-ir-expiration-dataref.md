---
title: 有効期限
description: クライアントキャッシュの有効期限。 有効期限までの時間数。 クライアントおよびプロキシサーバーのキャッシュを管理するために使用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4f7e5a8-0021-4dd3-be1b-8cb656cabdac
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 1%

---

# 有効期限{#expiration}

クライアントキャッシュの有効期限。 有効期限までの時間数。 クライアントおよびプロキシサーバーのキャッシュを管理するために使用します。

サーバは、この値を送信日時に加算することにより、NTTP 応答データの有効期限日時を算出する。

ブラウザーは、ファイルの有効期限を使用してキャッシュを管理します。 リクエストをサーバーに渡す前に、ブラウザーはキャッシュをチェックして、ファイルが既にダウンロードされているかどうかを確認します。 その場合、およびファイルの有効期限がまだ切れていない場合、ブラウザーは通常のGET リクエストではなく、条件付きGET リクエストを送信します（例：If-Modified-Since HTTP リクエストヘッダーを使用）。 サーバーには、画像を送信せずに「304」ステータスで応答するオプションがあります。 その後、ブラウザーは単にキャッシュからファイルを読み込みます。 これにより、頻繁にアクセスされるデータの全体的なパフォーマンスが大幅に向上する可能性があります。

サーバーは、expires HTTP 応答ヘッダーを、現在の日時に最小のビネット：:Expiration とすべてのカタログ：:Expiration の値を加えた値に設定します。ビネットと、レンダリング操作に関連するすべてのマテリアルの値です。

有効期限は主に画像データの応答に対して設定されます。 特定のタイプの応答は、すべてのエラー応答やプロパティ応答を含め、常に即時の有効期限がマークされます（または、キャッシュ不可としてタグ付けされます）。

## プロパティ {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

-2、-1、0 以上の実数。 応答画像が生成されてから有効期限が切れるまでの時間数。 常にレスポンスイメージの有効期限が直ちに切れるように 0 に設定すると、クライアントキャッシュが効果的に無効になります。 -1 に設定すると、`never expire` としてマークされます。 この場合、サーバーは、条件付き `GET` リクエストに応答して、ファイルが実際に変更されたかどうかを確認せずに、常に 304 ステータス（未変更）を返します。 `attribute::Expiration` が提供するデフォルトを使用するには、-2 に設定します。

## 初期設定 {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration` は、フィールドが存在しない場合、値が–2 の場合、またはフィールドが空の場合に使用されます。

## 関連項目 {#section-9d46a9d346fe42f3911edb3bd79f4121}

[attribute::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) , [vignette::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
