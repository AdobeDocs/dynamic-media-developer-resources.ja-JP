---
description: クライアントキャッシュの有効期間。 有効期限が切れるまでの時間数。 クライアントおよびプロキシサーバーのキャッシュを管理するために使用します。
seo-description: クライアントキャッシュの有効期間。 有効期限が切れるまでの時間数。 クライアントおよびプロキシサーバーのキャッシュを管理するために使用します。
seo-title: 有効期限
solution: Experience Manager
title: 有効期限
topic: Scene7 Image Serving - Image Rendering API
uuid: 6dbd7d43-727c-42fc-8953-dba112209a45
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 2%

---


# 有効期限{#expiration}

クライアントキャッシュの有効期間。 有効期限が切れるまでの時間数。 クライアントおよびプロキシサーバーのキャッシュを管理するために使用します。

サーバは、送信日時にこの値を加算してNTTP応答データの有効期限日時を計算する。

ブラウザーは、ファイルの有効期限を使用してキャッシュを管理します。 サーバーに要求を渡す前に、ブラウザーはキャッシュをチェックして、ファイルが既にダウンロードされているかどうかを確認します。 その場合は、ファイルの有効期限が切れていない場合、ブラウザーは、通常のGETリクエストではなく、条件付きGETリクエスト（例えば、If-Modified-Since HTTPリクエストヘッダー）を送信します。 サーバは、「304」ステータスで応答し、画像を送信しないオプションを持つ。 次に、ブラウザーはキャッシュからファイルを読み込みます。 これにより、頻繁にアクセスされるデータの全体的なパフォーマンスが大幅に向上します。

サーバは、expires HTTP応答ヘッダを現在の日時に設定し、vignette::Expirationの最小値と、ビネットおよびレンダリング操作に関連するすべてのマテリアルのすべてのcatalog::Expiration値を加えます。

有効期限は主に画像データ応答に対して設定されます。 すべてのエラー応答やプロパティの返信を含め、特定の種類の応答は、常に即時有効期限（またはキャッシュ不可のタグ付け）としてマークされます。

## プロパティ {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

実数、-2、-1、0以上 応答画像が生成されてから有効期限切れになるまでの時間数。 0に設定すると、応答イメージが直ちに期限切れになります。これにより、クライアントのキャッシュが効果的に無効になります。 `never expire`とマークするには、-1に設定します。 この場合、サーバは、条件付き`GET`要求に応じて常に304ステータス（変更されていない）を返します。ファイルが実際に変更されたかどうかはチェックしません。 `attribute::Expiration`が提供するデフォルト値を使用するには、-2に設定します。

## 初期設定 {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration` は、フィールドが存在しない場合、値が —2の場合、またはフィールドが空の場合に使用されます。

## 関連項目 {#section-9d46a9d346fe42f3911edb3bd79f4121}

[attribute::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [vignette::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
