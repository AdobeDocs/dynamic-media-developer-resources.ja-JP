---
description: エラー応答画像。 画像レンダリングは、エラーが発生すると、通常はエラーステータスとテキストメッセージを返します。 attribute ErrorImageを使用すると、エラーが発生した場合に返される画像を設定できます。
solution: Experience Manager
title: ErrorImage *
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: ed48482f-79b0-4c81-b5cd-cf997f27d3ab
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---

# ErrorImage *{#errorimage}

エラー応答画像。 画像レンダリングは、エラーが発生すると、通常はエラーステータスとテキストメッセージを返します。 attribute::ErrorImageを使用すると、エラーが発生した場合に返される画像を設定できます。

エラーが発生した場合、サーバはまず`ImageRendering::attribute::ErrorImage`の値を単純なイメージファイルパスとして解釈しようとします。 ファイルを開けない場合は、属性値とエラーの詳細が画像サービングに送信され、`ImageServing::attribute::ErrorImage`の説明に従って処理されます。 画像サービングが有効な応答画像を返さない場合、標準のHTTPエラーステータスとテキストメッセージがクライアントに送信されます。

エラー画像はHTTPステータス200で返されます。

## プロパティ {#section-4a4a7e37ed11483db0b9922dc68ea7db}

テキスト文字列。 指定する場合は、**`ImageServing::catalog::id`**&#x200B;値、相対パス（**`ImageServing::attribute::RootPath`**&#x200B;または&#x200B;**`ImageRendering::attribute::RootPath`**）、またはImage Serverからアクセス可能な画像ファイルへの絶対パスを指定する必要があります。

## 初期設定 {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

`default::ErrorImage`から継承されます（定義されていない場合）。 定義されているが空の場合、`default::ErrorImage`が定義されていても、エラー画像の動作が無効になり、HTTPエラーステータスが返されます。

## 関連項目 {#section-3e0308eaf4124451909dacd570e27695}

[attribute::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)、 [attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b)、 [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)、 [catalog::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
