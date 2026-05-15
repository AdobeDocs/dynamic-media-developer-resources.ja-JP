---
title: エラー
description: リクエストが正常に完了しない場合、サーバーはエラーイメージまたは200以外のHTTP応答ステータスをエラーメッセージと共に返します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e45e3968-3659-470b-a88a-fe7ba73d8207
TQID: 'https://experienceleague.adobe.com/TSTpmfiuEppAPSUxX1ga5lfQSgWRkI2Wh1CXoalSU9A'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 1%

---

# エラー{#errors}

リクエストが正常に完了しない場合、サーバーはエラーイメージまたは200以外のHTTP応答ステータスをエラーメッセージと共に返します。

応答ステータスの値は、エラーのタイプによって異なります。最も一般的なエラーは、「403」です。 画像以外のリクエストタイプのエラー応答は、`req=`で指定された形式に準拠しています。 （現在は一貫して実装されていない可能性があります）。

エラーメッセージに含まれる詳細の量は、`attribute::ErrorDetail`で設定可能です。

**エラー画像**

画像サービングは、画像にレンダリングされたエラーメッセージを返すように設定できます。 詳しくは、画像カタログのリファレンスの`attribute::ErrorImage`を参照してください。 エラー画像が正常に生成された場合、HTTP応答ステータスは200になります。 エラー画像の処理中にエラーが発生した場合、標準のHTTP エラー応答とテキストメッセージがクライアントに返されます。

**関連項目**

[属性：:ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b)、[属性：:ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
