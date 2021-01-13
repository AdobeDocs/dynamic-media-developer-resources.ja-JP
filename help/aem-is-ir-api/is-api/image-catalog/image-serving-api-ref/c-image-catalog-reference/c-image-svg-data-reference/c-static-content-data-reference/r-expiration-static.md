---
description: 有効期限
solution: Experience Manager
title: 有効期限
topic: Scene7 Image Serving - Image Rendering API
uuid: a727bbfc-940b-4d65-96d6-b2159b70bac1
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 2%

---


# 有効期限{#expiration}

クライアントおよびプロキシサーバーのキャッシュを管理するために使用します。 サーバは、送信日時にこの値を加算して、HTTP応答データの有効期限日時を計算します。

ブラウザーは、ファイルの有効期限を使用してキャッシュを管理します。 サーバーに要求を渡す前に、ブラウザーはキャッシュをチェックして、ファイルが既にダウンロード済みかどうかを確認します。 その場合、まだファイルの有効期限が切れていない場合、ブラウザーは、条件付きGETリクエスト（例えば、リクエストヘッダーにIf-Modified-Sinceフィールドが設定されている場合）を、通常のGETリクエストではなく送信します。 サーバは、「304」ステータスで応答し、画像を送信しないオプションを持つ。 次に、ブラウザーはキャッシュからファイルを読み込みます。 これにより、頻繁にアクセスされるデータの全体的なパフォーマンスが大幅に向上します。

有効期限は、次の応答タイプに使用されます。

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

特定の種類の応答（エラー応答など）は常に即時有効期限（またはキャッシュ不可のタグ付け）としてマークされ、その他（プロパティやデフォルトの画像応答など）は特殊な有効期限設定（`attribute::NonImgExpiration`と`attribute::DefaultExpiration`）を使用します。

## プロパティ {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

実数、-2、-1または0以上。 応答画像が生成されてから有効期限切れになるまでの時間数。 0に設定すると、常に応答イメージが即時に期限切れになります。これにより、クライアントのキャッシュが効果的に無効になります。 *`never expire`*&#x200B;とマークするには、-1に設定します。 この場合、サーバーは、条件付きGET要求に対して常に304ステータス（変更されていない）を返します。ファイルが実際に変更されたかどうかは確認されません。 `attribute::Expiration`が提供するデフォルト値を使用するには、-2に設定します。

## 初期設定 {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` は、フィールドが存在しない場合、値が —2の場合、またはフィールドが空の場合に使用されます。

## 関連項目 {#section-0e5e8595aad641c689726828712a8902}

[attribute::Expiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7),  [attribute::DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf),  [attribute::NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d),  [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
