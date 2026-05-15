---
description: 有効期限
solution: Experience Manager
title: 有効期限
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 62d2368b-ea56-4964-ab9c-07454e19540c
TQID: 'https://experienceleague.adobe.com/LwsIp6Z16Bx-VTgjbKVl5XVReg4Vt6QsoAdZ0CXY-mE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 277
ht-degree: 2%

---

# 有効期限{#expiration}

クライアントおよびプロキシ サーバーのキャッシュの管理に使用します。 サーバは、この値を送信日時に付加することにより、HTTP応答データの有効期限を算出する。

ブラウザーは、ファイルの有効期限を使用してキャッシュを管理します。 リクエストをサーバーに渡す前に、ブラウザーはキャッシュをチェックして、ファイルが既にダウンロードされているかどうかを確認します。 その場合、ファイルがまだ期限切れになっていない場合、ブラウザーは通常のGET リクエストではなく、条件付きGET リクエスト（リクエストヘッダーに設定されたIf-Modified-Since フィールドなど）を送信します。 サーバーには、「304」ステータスで応答し、画像を送信しないオプションがあります。 次に、ブラウザーはキャッシュからファイルを読み込みます。 これにより、頻繁にアクセスされるデータの全体的なパフォーマンスが大幅に向上する可能性があります。

有効期限は、次の応答タイプに使用されます。

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

特定の種類の応答（エラー応答など）は、常に即時の有効期限が設定されます（またはキャッシュ不可としてタグ付けされます）。その他の応答（プロパティやデフォルトの画像応答など）では、特別な有効期限の設定（`attribute::NonImgExpiration`および`attribute::DefaultExpiration`）が使用されます。

## プロパティ {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

実数、-2、-1、または0以上。 応答イメージが生成されてから有効期限が切れるまでの時間数。 0に設定すると、返信画像が即座に期限切れになり、クライアントのキャッシュが効果的に無効になります。 *`never expire`*&#x200B;としてマークするには–1に設定します。 この場合、サーバーは、条件付きGET リクエストに応答して、ファイルが実際に変更されたかどうかを確認することなく、常に304 ステータス（未変更）を返します。 `attribute::Expiration`が提供するデフォルトを使用するには、-2に設定します。

## 初期設定 {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration`は、フィールドが存在しない場合、値が–2の場合、またはフィールドが空の場合に使用されます。

## 関連項目 {#section-0e5e8595aad641c689726828712a8902}

[属性：：有効期限](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7)、[属性：:DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)、[属性：:NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)、[req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
