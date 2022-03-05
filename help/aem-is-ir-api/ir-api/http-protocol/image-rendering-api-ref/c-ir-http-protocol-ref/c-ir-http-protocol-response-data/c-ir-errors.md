---
title: エラー
description: リクエストが正常に完了しなかった場合、サーバーはエラーイメージまたは 200 以外の HTTP 応答ステータスをエラーメッセージと共に返します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e45e3968-3659-470b-a88a-fe7ba73d8207
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 2%

---

# エラー{#errors}

リクエストが正常に完了しなかった場合、サーバーはエラーイメージまたは 200 以外の HTTP 応答ステータスをエラーメッセージと共に返します。

応答ステータスの値は、エラーのタイプによって異なります。最も一般的なエラーは「403」です。 イメージ以外のリクエストタイプに対するエラー応答は、 `req=`. （現在、一貫して実装されていない可能性があります）

エラーメッセージに含まれる詳細の量は、 `attribute::ErrorDetail`.

**エラー画像**

画像サービングは、画像内にレンダリングされたエラーメッセージを返すように設定できます。 詳しくは、 `attribute::ErrorImage` （画像カタログリファレンス）を参照してください。 エラー画像が正常に生成された場合、HTTP 応答のステータスは 200 です。 エラー画像の処理中にエラーが発生した場合は、標準の HTTP エラー応答とテキストメッセージがクライアントに返されます。

**関連項目**

[attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) , [attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
