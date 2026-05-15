---
title: 有効期限
description: クライアントキャッシュの稼働時間： 有効期限までの時間数。 クライアントおよびプロキシ サーバーのキャッシュの管理に使用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4f7e5a8-0021-4dd3-be1b-8cb656cabdac
TQID: 'https://experienceleague.adobe.com/dFnSsD8mmC0aPefS3Z0GujF1A-p1nCQyiNpzMXxOBEQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 325
ht-degree: 1%

---

# 有効期限{#expiration}

クライアントキャッシュの稼働時間： 有効期限までの時間数。 クライアントおよびプロキシ サーバーのキャッシュの管理に使用します。

サーバは、この値を送信日時に付加することにより、NTTP応答データの有効期限を算出する。

ブラウザーは、ファイルの有効期限を使用してキャッシュを管理します。 リクエストをサーバーに渡す前に、ブラウザーはキャッシュをチェックして、ファイルが既にダウンロードされているかどうかを確認します。 その場合、ファイルがまだ期限切れになっていない場合、ブラウザーは通常のGET リクエストではなく、条件付きGET リクエスト（例えば、If-Modified-Since HTTP リクエストヘッダー）を送信します。 サーバーには、「304」ステータスで応答し、画像を送信しないオプションがあります。 ブラウザーはキャッシュからファイルを読み込むだけです。 これにより、頻繁にアクセスされるデータの全体的なパフォーマンスが大幅に向上する可能性があります。

サーバーは、有効期限HTTP応答ヘッダーを、現在の日時に、周辺光量補正：：有効期限の最小値を加え、周辺光量補正とすべてのカタログ：：有効期限の値を、レンダリング操作に関連するすべてのマテリアルに設定します。

有効期限は、主に画像データの応答に設定されます。 特定のタイプの応答は、すべてのエラー応答やプロパティ応答を含め、即時の有効期限（またはキャッシュ不可としてタグ付け）が常にマークされます。

## プロパティ {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

実数、-2、-1、0以上。 応答イメージが生成されてから有効期限が切れるまでの時間数。 0に設定すると、応答イメージが即座に期限切れになり、クライアントのキャッシュが効果的に無効になります。 `never expire`としてマークするには–1に設定します。 この場合、サーバーは、条件付き`GET`要求に応答して常に304 ステータス（未変更）を返します。ファイルが実際に変更されたかどうかを確認する必要はありません。 `attribute::Expiration`が提供するデフォルトを使用するには、-2に設定します。

## 初期設定 {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration`は、フィールドが存在しない場合、値が–2の場合、またはフィールドが空の場合に使用されます。

## 関連項目 {#section-9d46a9d346fe42f3911edb3bd79f4121}

[属性：：有効期限](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996)、[&#x200B; ビネット：：有効期限](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)、[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
