---
description: リクエストが正常に完了しなかった場合、サーバーはエラーイメージまたは 200 以外の HTTP 応答ステータスをエラーメッセージと共に返します。
solution: Experience Manager
title: エラー
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9314782f-703b-4e9c-a026-62970d1c752f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 2%

---

# エラー{#errors}

リクエストが正常に完了しなかった場合、サーバーはエラーイメージまたは 200 以外の HTTP 応答ステータスをエラーメッセージと共に返します。

応答ステータスの値は、エラーのタイプによって異なります。最も一般的なエラーは「403」です。 イメージ以外のリクエストタイプに対するエラー応答は、 `req=`. （現時点では一貫して実装されていない場合があります）。

エラーメッセージに含まれる詳細の量は、 `attribute::ErrorDetail`.

## エラー画像 {#section-92e9b20b2507433daa96923abc95f777}

画像サービングは、画像にレンダリングされたエラーメッセージを返すように設定できます。

詳しくは、 [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c) （画像カタログリファレンス）を参照してください。

エラー画像が正常に生成された場合、HTTP 応答のステータスは 200 です。 エラー画像の処理中にエラーが発生した場合は、標準の HTTP エラー応答とテキストメッセージがクライアントに返されます。

## デフォルトの画像 {#section-66bf25fe6b434081bfae96d38d9be25e}

画像サービングは、見つからない画像をデフォルトの画像に置き換えるように設定できます。 デフォルトの画像は、 `attribute::DefaultImage` または `defaultImage=` コマンドを使用します。

## 関連項目 {#section-e261d7f224ca4546bb64bf8cb909db08}

[attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561) , [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c), [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [defaultImage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
