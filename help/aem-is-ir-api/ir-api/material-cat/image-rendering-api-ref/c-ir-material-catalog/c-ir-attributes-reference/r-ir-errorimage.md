---
description: エラー応答画像。 画像レンダリングは、通常、エラーが発生した場合、エラーステータスとテキストメッセージを返します。 attribute ErrorImageを使用すると、エラーが発生した場合にイメージを返すように設定できます。
seo-description: エラー応答画像。 画像レンダリングは、通常、エラーが発生した場合、エラーステータスとテキストメッセージを返します。 attribute ErrorImageを使用すると、エラーが発生した場合にイメージを返すように設定できます。
seo-title: ErrorImage *
solution: Experience Manager
title: ErrorImage *
topic: Scene7 Image Serving - Image Rendering API
uuid: 6c8801d0-8cd0-4477-9a60-ccbb343a0747
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ErrorImage *{#errorimage}

エラー応答画像。 画像レンダリングは、通常、エラーが発生した場合、エラーステータスとテキストメッセージを返します。 attribute::ErrorImageを使用すると、エラーが発生した場合にイメージを返すように設定できます。

エラーが発生した場合、サーバはまず、の値を単純な画像フ `ImageRendering::attribute::ErrorImage`ァイルパスとして解釈します。 ファイルを開けない場合は、属性値とエラーの詳細が画像サービングに送信され、画像サービングは、の説明に従って処理しま `ImageServing::attribute::ErrorImage`す。 画像サービングが有効な応答画像を返さない場合、標準のHTTPエラーステータスとテキストメッセージがクライアントに送信されます。

HTTPステータス200のエラー画像が返されます。

## プロパティ {#section-4a4a7e37ed11483db0b9922dc68ea7db}

テキスト文字列。 指定する場合は、値、相対パス(または **`ImageServing::catalog::id`** を参照)、またはImage Serverがアクセス可能な **`ImageServing::attribute::RootPath`** 画像ファ **`ImageRendering::attribute::RootPath`**&#x200B;イルの絶対パスのいずれかを指定する必要があります。

## 初期設定 {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

定義されていな `default::ErrorImage` い場合は、から継承されます。 定義済みで空の場合は、定義済みであっても、エラー画像の動作が無 `default::ErrorImage` 効になり、HTTPエラーステータスが返されます。

## 関連項目 {#section-3e0308eaf4124451909dacd570e27695}

[attribute::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3), [catalog::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
