---
title: ErrorImage
description: エラー応答画像。 通常、画像レンダリングは、エラーが発生するとエラーメッセージと共にエラーステータスを返します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ed48482f-79b0-4c81-b5cd-cf997f27d3ab
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---

# ErrorImage {#errorimage}

エラー応答画像。 通常、画像レンダリングは、エラーが発生するとエラーメッセージと共にエラーステータスを返します。 `attribute::ErrorImage` では、エラーが発生した場合に返す画像を設定できます。

エラーが発生すると、サーバーは `ImageRendering::attribute::ErrorImage` の値を単純な画像ファイルパスとして解釈しようとします。 ファイルを開くことができない場合は、属性値とエラーの詳細が画像サービングに送信されます。画像サービングは、`ImageServing::attribute::ErrorImage` に説明されているように処理されます。 画像サービングで有効な応答画像が返されない場合、標準の HTTP エラーステータスとテキストメッセージがクライアントに送信されます。

エラー画像は、HTTP ステータス 200 で返されます。

## プロパティ {#section-4a4a7e37ed11483db0b9922dc68ea7db}

テキスト文字列 指定する場合は、**`ImageServing::catalog::id`** 値、相対パス（**`ImageServing::attribute::RootPath`** または **`ImageRendering::attribute::RootPath`**）または Image Server からアクセス可能な画像ファイルへの絶対パスのいずれかを指定する必要があります。

## 初期設定 {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

`default::ErrorImage` から継承（定義されていない場合）。 定義されていても空の場合、エラーイメージの動作は、`default::ErrorImage` が定義されていても無効になり、HTTP エラーステータスが返されます。

## 関連項目 {#section-3e0308eaf4124451909dacd570e27695}

[attribute::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)、[attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b)、[attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)、[catalog::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
