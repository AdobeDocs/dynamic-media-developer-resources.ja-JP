---
description: 要求が正常に完了しなかった場合、サーバーは、エラー画像または200以外のHTTP応答ステータスをエラーメッセージと共に返します。
seo-description: 要求が正常に完了しなかった場合、サーバーは、エラー画像または200以外のHTTP応答ステータスをエラーメッセージと共に返します。
seo-title: エラー
solution: Experience Manager
title: エラー
topic: Scene7 Image Serving - Image Rendering API
uuid: 5984fa9e-63c8-426b-be5f-48f66fc918c3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 2%

---


# エラー{#errors}

要求が正常に完了しなかった場合、サーバーは、エラー画像または200以外のHTTP応答ステータスをエラーメッセージと共に返します。

応答ステータスの値は、エラーのタイプに応じて異なります。最も一般的なエラーは「403」です。 イメージ以外の要求タイプのエラー応答は、`req=`で指定された形式に従います。 （現時点では一貫して実装されていない可能性があります）。

エラーメッセージに含まれる詳細の量は`attribute::ErrorDetail`で設定できます。

**エラー画像**

画像サービングは、画像にレンダリングされたエラーメッセージを返すように設定できます。 詳しくは、画像カタログリファレンスの`attribute::ErrorImage`を参照してください。 エラー画像が正常に生成された場合、HTTP応答ステータスは200です。 エラー画像の処理中にエラーが発生した場合は、標準のHTTPエラー応答とテキストメッセージがクライアントに返されます。

**関連項目**

[attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) ,  [attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
