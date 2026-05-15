---
description: リクエストが正常に完了しない場合、サーバーはエラーイメージまたは200以外のHTTP応答ステータスをエラーメッセージと共に返します。
solution: Experience Manager
title: エラー
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9314782f-703b-4e9c-a026-62970d1c752f
TQID: 'https://experienceleague.adobe.com/qqe0JDlFGu08lAe-K3Ww9AtefwQInwBzZswiXsvqryo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 203
ht-degree: 1%

---

# エラー{#errors}

リクエストが正常に完了しない場合、サーバーはエラーイメージまたは200以外のHTTP応答ステータスをエラーメッセージと共に返します。

応答ステータスの値は、エラーのタイプによって異なります。最も一般的なエラーは「403」です。 画像以外のリクエストタイプのエラー応答は、`req=`で指定された形式に準拠しています。 （現時点では一貫して実装されていない可能性があります）。

エラーメッセージに含まれる詳細の量は、`attribute::ErrorDetail`で設定可能です。

## エラー画像 {#section-92e9b20b2507433daa96923abc95f777}

画像サービングは、画像にレンダリングされたエラーメッセージを返すように設定できます。

詳しくは、画像カタログのリファレンスの[属性：:ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)を参照してください。

エラー画像が正常に生成された場合、HTTP応答ステータスは200になります。 エラー画像の処理中にエラーが発生した場合、標準のHTTP エラー応答とテキストメッセージがクライアントに返されます。

## デフォルト画像 {#section-66bf25fe6b434081bfae96d38d9be25e}

画像サービングは、欠落している画像をデフォルトの画像に置き換えるように設定できます。 デフォルトの画像は、`attribute::DefaultImage`または`defaultImage=` コマンドで指定できます。

## 関連項目 {#section-e261d7f224ca4546bb64bf8cb909db08}

[属性：:ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)、[属性：:ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)、[属性：:DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)、[defaultImage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
