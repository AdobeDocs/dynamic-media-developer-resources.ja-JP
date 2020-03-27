---
description: 'null'
seo-description: 'null'
seo-title: 有効期限
solution: Experience Manager
title: 有効期限
topic: Scene7 Image Serving - Image Rendering API
uuid: a727bbfc-940b-4d65-96d6-b2159b70bac1
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0

---


# 有効期限{#expiration}

クライアントおよびプロキシサーバーのキャッシュを管理するために使用します。 サーバは、この値を送信日時に加算して、HTTP応答データの有効期限日時を計算します。

ブラウザーは、ファイルの有効期限を使用してキャッシュを管理します。 サーバーに要求を渡す前に、ブラウザーはキャッシュをチェックし、ファイルが既にダウンロードされているかどうかを確認します。 その場合、まだファイルの有効期限が切れていない場合は、ブラウザは、通常のGETリクエストではなく、条件付きのGETリクエスト（例えば、リクエストヘッダーにIf-Modified-Sinceフィールドが設定されている場合）を送信します。 サーバは、「304」ステータスで応答し、画像を送信しないオプションを持つ。 次に、ブラウザーはキャッシュからファイルを読み込みます。 これにより、頻繁にアクセスされるデータの全体的なパフォーマンスが大幅に向上します。

有効期限は、次の応答タイプで使用されます。

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

特定のタイプの応答（エラー応答など）は、常に即時有効期限（またはキャッシュ不可としてタグ付け）でマークされ、その他（プロパティやデフォルトの画像応答など）は特別な有効期限設定(および `attribute::NonImgExpiration``attribute::DefaultExpiration`)を使用します。

## プロパティ {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

実数、-2、-1または0以上。 応答画像が生成されてから有効期限切れになるまでの時間数。 0に設定すると、常に応答イメージの有効期限が直ちに切れます。これにより、クライアントのキャッシュが事実上無効になります。 -1に設定すると、としてマークされま *`never expire`*&#x200B;す。 この場合、サーバは常に304ステータス（変更なし）を返し、条件付きのGET要求に応答します。ファイルが実際に変更されたかどうかは確認されません。 で指定されたデフォルトを使用する場合は、-2に設定しま `attribute::Expiration`す。

## 初期設定 {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` が使用されるのは、フィールドが存在しない場合、値が —2の場合、またはフィールドが空の場合です。

## 関連項目 {#section-0e5e8595aad641c689726828712a8902}

[attribute::Expiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7), [attribute::DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf), [attribute::NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d), [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
