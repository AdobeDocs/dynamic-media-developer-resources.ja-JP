---
title: エラー
description: リクエストを正常に完了できない場合、サーバーはエラーイメージまたは 200 以外の HTTP 応答ステータスをエラーメッセージと共に返します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e45e3968-3659-470b-a88a-fe7ba73d8207
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 1%

---

# エラー{#errors}

リクエストを正常に完了できない場合、サーバーはエラーイメージまたは 200 以外の HTTP 応答ステータスをエラーメッセージと共に返します。

応答ステータスの値は、エラーのタイプに応じて異なります。最も一般的なエラーの場合は、「403」です。 非画像リクエストタイプのエラー応答は、`req=` で指定された形式に準拠しています。 （現在、一貫して実装されていない可能性があります）。

エラーメッセージに含まれる詳細の量は、`attribute::ErrorDetail` で設定できます。

**エラー画像**

画像サービングは、画像にレンダリングされたエラーメッセージを返すように設定できます。 詳しくは、画像カタログの参照の `attribute::ErrorImage` を参照してください。 エラーイメージが正常に生成された場合、HTTP 応答ステータスは 200 になります。 エラー画像の処理中にエラーが発生した場合は、標準の HTTP エラー応答とテキストメッセージがクライアントに返されます。

**関連トピック**

[attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b)、[attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
