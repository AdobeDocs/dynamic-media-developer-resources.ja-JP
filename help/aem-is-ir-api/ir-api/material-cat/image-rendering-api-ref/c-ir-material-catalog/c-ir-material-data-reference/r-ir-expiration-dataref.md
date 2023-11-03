---
title: 有効期限
description: クライアントキャッシュの有効期間。 有効期限が切れるまでの時間数。 クライアントおよびプロキシサーバーのキャッシュを管理するために使用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4f7e5a8-0021-4dd3-be1b-8cb656cabdac
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 1%

---

# 有効期限{#expiration}

クライアントキャッシュの有効期間。 有効期限が切れるまでの時間数。 クライアントおよびプロキシサーバーのキャッシュを管理するために使用します。

サーバは、送信日時にこの値を加算して、NTTP 応答データの有効期限を算出する。

ブラウザーは、ファイルの有効期限を使用してキャッシュを管理します。 サーバーにリクエストを渡す前に、ブラウザーはキャッシュをチェックして、ファイルが既にダウンロードされているかどうかを確認します。 その場合で、ファイルの有効期限が切れていない場合、ブラウザーは、条件付きGETリクエスト（例えば、If-Modified-Since HTTP リクエストヘッダーを含む）を通常のGETリクエストではなく送信します。 サーバーは、「304」ステータスで応答し、画像を送信しないオプションを持ちます。 次に、ブラウザーは、キャッシュからファイルを読み込むだけです。 これにより、頻繁にアクセスするデータの全体的なパフォーマンスが大幅に向上する場合があります。

サーバは、有効期限切れの HTTP 応答ヘッダーを現在の日時に設定し、ビネット：:Expiration と、レンダリング操作に関係するすべてのマテリアルのビネットとすべての catalog::Expiration の最小値を追加します。

有効期限は、主に画像データ応答に対して設定されます。 すべてのエラー応答やプロパティ応答を含め、特定のタイプの応答は、常に即時有効期限（またはキャッシュ不可としてタグ付け）としてマークされます。

## プロパティ {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

実数、-2、-1、0 以上。 応答画像が生成されてから有効期限が切れるまでの時間数。 常に応答イメージを即座に期限切れにするには、0 に設定します。これにより、クライアントのキャッシュが効果的に無効になります。 -1 に設定して次の名前にします。 `never expire`. この場合、サーバーは常に条件に応じて 304 ステータス（未変更）を返します `GET` リクエストを送信する際に、ファイルが実際に変更されたかどうかを確認する必要はありません。 -2 に設定すると、 `attribute::Expiration`.

## 初期設定 {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration` フィールドが存在しない場合、値が —2 の場合、またはフィールドが空の場合に、が使用されます。

## 関連項目 {#section-9d46a9d346fe42f3911edb3bd79f4121}

[attribute::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) , [vignette::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
