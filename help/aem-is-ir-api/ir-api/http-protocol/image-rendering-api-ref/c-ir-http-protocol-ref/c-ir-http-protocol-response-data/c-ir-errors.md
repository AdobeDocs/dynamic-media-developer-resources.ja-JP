---
description: リクエストが正常に完了できない場合、サーバーはエラーイメージまたは200以外のHTTP応答ステータスをエラーメッセージと共に返します。
solution: Experience Manager
title: エラー
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: e45e3968-3659-470b-a88a-fe7ba73d8207
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 2%

---

# エラー{#errors}

リクエストが正常に完了できない場合、サーバーはエラーイメージまたは200以外のHTTP応答ステータスをエラーメッセージと共に返します。

応答ステータスの値は、エラーのタイプによって異なります。最も一般的なエラーは「403」です。 イメージ以外のリクエストタイプに対するエラー応答は、`req=`で指定された形式に従います。 （現時点では、一貫して実装されていない可能性があります）。

エラーメッセージに含まれる詳細の量は`attribute::ErrorDetail`で設定できます。

**エラー画像**

画像サービングは、画像にレンダリングされたエラーメッセージを返すように設定できます。 詳しくは、画像カタログリファレンスの`attribute::ErrorImage`を参照してください。 エラー画像が正常に生成された場合、HTTP応答ステータスは200です。 エラー画像の処理中にエラーが発生した場合は、標準のHTTPエラー応答とテキストメッセージがクライアントに返されます。

**関連項目**

[attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) ,  [attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
