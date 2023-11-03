---
description: 有効期限
solution: Experience Manager
title: 有効期限
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 62d2368b-ea56-4964-ab9c-07454e19540c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 2%

---

# 有効期限{#expiration}

クライアントおよびプロキシサーバーのキャッシュを管理するために使用します。 サーバは、送信日時にこの値を加算して、HTTP 応答データの有効期限を算出する。

ブラウザーは、ファイルの有効期限を使用してキャッシュを管理します。 サーバーにリクエストを渡す前に、ブラウザーはキャッシュをチェックして、ファイルが既にダウンロードされているかどうかを確認します。 その場合で、ファイルの有効期限が切れていない場合、ブラウザーは、条件付きGETリクエスト（例えば、リクエストヘッダーに If-Modified-Since フィールドが設定されたもの）を、通常のGETリクエストではなく送信します。 サーバーは、「304」ステータスで応答し、画像を送信しないオプションを持ちます。 次に、ブラウザーはキャッシュからファイルを読み込みます。 これにより、頻繁にアクセスするデータの全体的なパフォーマンスが大幅に向上する場合があります。

有効期限は、次の応答タイプに使用されます。

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

特定のタイプの応答（エラー応答など）は、常に即時有効期限（またはキャッシュ不可能としてタグ付け）としてマークされ、それ以外（例えば、プロパティやデフォルトの画像応答）は特別な有効期限設定 ( `attribute::NonImgExpiration` および `attribute::DefaultExpiration`) をクリックします。

## プロパティ {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

実数、-2、-1、0 以上。 応答画像が生成されてから有効期限が切れるまでの時間数。 常に返信画像の有効期限を即座に切れるようにするには、0 に設定します。これにより、クライアントのキャッシュが効果的に無効になります。 -1 に設定して次の名前にします。 *`never expire`*. この場合、サーバーは常に、条件付きGETリクエストに対して 304 ステータス（未変更）を返します。この際、ファイルが実際に変更されたかどうかは確認しません。 -2 に設定すると、 `attribute::Expiration`.

## 初期設定 {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` フィールドが存在しない場合、値が —2 の場合、またはフィールドが空の場合に、が使用されます。

## 関連項目 {#section-0e5e8595aad641c689726828712a8902}

[attribute::Expiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7), [attribute::DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf), [attribute::NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d), [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
