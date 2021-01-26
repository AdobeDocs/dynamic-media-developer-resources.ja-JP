---
description: 要求が正常に完了しなかった場合、サーバーは、エラー画像または200以外のHTTP応答ステータスをエラーメッセージと共に返します。
seo-description: 要求が正常に完了しなかった場合、サーバーは、エラー画像または200以外のHTTP応答ステータスをエラーメッセージと共に返します。
seo-title: エラー
solution: Experience Manager
title: エラー
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a08f3f5a-3013-4d35-9612-25190a4c99fa
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 2%

---


# エラー{#errors}

要求が正常に完了しなかった場合、サーバーは、エラー画像または200以外のHTTP応答ステータスをエラーメッセージと共に返します。

応答ステータスの値は、エラーのタイプに応じて異なります。最も一般的なエラーは「403」です。 イメージ以外の要求タイプのエラー応答は、`req=`で指定された形式に従います。 （現時点では一貫して実装されていない可能性があります）。

エラーメッセージに含まれる詳細の量は`attribute::ErrorDetail`で設定できます。

## エラーイメージ{#section-92e9b20b2507433daa96923abc95f777}

画像サービングは、画像にレンダリングされたエラーメッセージを返すように設定できます。

詳しくは、画像カタログ参照の[attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)を参照してください。

エラー画像が正常に生成された場合、HTTP応答ステータスは200です。 エラー画像の処理中にエラーが発生した場合は、標準のHTTPエラー応答とテキストメッセージがクライアントに返されます。

## デフォルトの画像{#section-66bf25fe6b434081bfae96d38d9be25e}

画像サービングは、見つからない画像を初期設定の画像に置き換えるように設定できます。 デフォルトの画像は、`attribute::DefaultImage`または`defaultImage=`コマンドを使用して指定できます。

## 関連項目 {#section-e261d7f224ca4546bb64bf8cb909db08}

[attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561) ,  [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c),  [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [defaultImage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
