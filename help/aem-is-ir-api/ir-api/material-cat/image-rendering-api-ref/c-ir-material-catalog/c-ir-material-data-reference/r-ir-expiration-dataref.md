---
description: クライアントキャッシュの有効期間。 有効期限が切れるまでの時間数。 クライアントおよびプロキシサーバーのキャッシュを管理するために使用します。
solution: Experience Manager
title: 有効期限
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: e4f7e5a8-0021-4dd3-be1b-8cb656cabdac
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 1%

---

# 有効期限{#expiration}

クライアントキャッシュの有効期間。 有効期限が切れるまでの時間数。 クライアントおよびプロキシサーバーのキャッシュを管理するために使用します。

サーバは、送信日時にこの値を加算してNTTP応答データの有効期限日時を計算する。

ブラウザーは、ファイルの有効期限を使用してキャッシュを管理します。 サーバーにリクエストを渡す前に、ブラウザーはそのキャッシュをチェックして、ファイルが既にダウンロードされているかどうかを確認します。 その場合、まだファイルの有効期限が切れていない場合、ブラウザーは、通常のGETリクエストではなく、条件付きGETリクエスト（例えば、If-Modified-Since HTTPリクエストヘッダー）を送信します。 サーバーは、「304」ステータスで応答し、画像を送信しないオプションを持ちます。 次に、ブラウザーは、キャッシュからファイルを読み込むだけです。 これにより、頻繁にアクセスするデータの全体的なパフォーマンスが大幅に向上する可能性があります。

サーバは、有効期限切れのHTTP応答ヘッダーを、現在の日時と、vignette::Expirationの最小値と、レンダリング操作に関係するすべてのビネットおよびマテリアルのすべてのcatalog::Expiration値に設定します。

有効期限は、主に画像データ応答に対して設定されます。 すべてのエラー応答やプロパティの応答を含め、特定のタイプの応答は、常に即時有効期限（またはキャッシュ不可能としてタグ付け）が設定されます。

## プロパティ {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

実数、-2、-1、0以上。 応答イメージが生成されてから有効期限が切れるまでの時間数。 0に設定すると、常に応答イメージの有効期限が即座に切れ、クライアントのキャッシュが効果的に無効になります。 -1に設定すると、`never expire`としてマークされます。 この場合、サーバーは常に、条件付き`GET`要求に応答して304ステータス（変更なし）を返します。ファイルが実際に変更されたかどうかは確認されません。 `attribute::Expiration`が提供するデフォルトを使用するには、-2に設定します。

## 初期設定 {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration` が使用されるのは、フィールドが存在しない場合、値が —2の場合、またはフィールドが空の場合です。

## 関連項目 {#section-9d46a9d346fe42f3911edb3bd79f4121}

[attribute::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) 、 [vignette::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)、 [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
