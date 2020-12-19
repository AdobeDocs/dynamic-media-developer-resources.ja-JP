---
description: エラー応答画像。 画像レンダリングは、通常、エラーが発生した場合に、エラーステータスとテキストメッセージを返します。 attribute ErrorImageを使用すると、エラーが発生した場合にイメージが返されるように設定できます。
seo-description: エラー応答画像。 画像レンダリングは、通常、エラーが発生した場合に、エラーステータスとテキストメッセージを返します。 attribute ErrorImageを使用すると、エラーが発生した場合にイメージが返されるように設定できます。
seo-title: ErrorImage *
solution: Experience Manager
title: ErrorImage *
topic: Scene7 Image Serving - Image Rendering API
uuid: 6c8801d0-8cd0-4477-9a60-ccbb343a0747
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 1%

---


# ErrorImage *{#errorimage}

エラー応答画像。 画像レンダリングは、通常、エラーが発生した場合に、エラーステータスとテキストメッセージを返します。 attribute::ErrorImageを使用すると、エラーが発生した場合に返すイメージを設定できます。

エラーが発生した場合、サーバはまず`ImageRendering::attribute::ErrorImage`の値を単純なイメージファイルパスとして解釈しようとします。 ファイルを開けない場合は、属性値とエラーの詳細を画像サービングに送信します。画像サービングは`ImageServing::attribute::ErrorImage`の説明に従って処理します。 画像サービングから有効な応答画像が返されない場合、標準のHTTPエラーステータスとテキストメッセージがクライアントに送信されます。

HTTPステータス200のエラー画像が返されます。

## プロパティ {#section-4a4a7e37ed11483db0b9922dc68ea7db}

テキスト文字列。 指定する場合は、**`ImageServing::catalog::id`**&#x200B;値、相対パス（**`ImageServing::attribute::RootPath`**&#x200B;または&#x200B;**`ImageRendering::attribute::RootPath`**&#x200B;へのパス）、またはImage Serverがアクセス可能な画像ファイルの絶対パスのいずれかにする必要があります。

## 初期設定 {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

`default::ErrorImage`から継承します（定義されていない場合）。 定義されているが空の場合、`default::ErrorImage`が定義されていて、HTTPエラーステータスが返された場合でも、エラーイメージの動作は無効になります。

## 関連項目 {#section-3e0308eaf4124451909dacd570e27695}

[attribute::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f),  [attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3),  [catalog::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
