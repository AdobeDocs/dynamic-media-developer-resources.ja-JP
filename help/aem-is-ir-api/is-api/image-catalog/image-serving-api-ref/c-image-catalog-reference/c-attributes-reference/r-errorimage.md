---
description: エラー応答画像。 画像サービングは、通常、エラーが発生すると、エラーステータスとテキストメッセージを返します。
solution: Experience Manager
title: ErrorImage
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: f412a379-525e-42fc-97bf-b10e00da6a20
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 1%

---

# ErrorImage{#errorimage}

エラー応答画像。 画像サービングは、通常、エラーが発生すると、エラーステータスとテキストメッセージを返します。

`attribute::ErrorImage` では、エラーが発生した場合に返す画像、カタログエントリ、またはテンプレートを設定できます。

>[!NOTE]
>
>見つからない画像は`attribute::DefaultImage`で処理することもできます。

画像サービングテンプレートを設定できます。これにより、エラーメッセージテキストが応答画像にレンダリングされる場合があります。 次の事前定義済みの変数を`$error.title`テンプレートに含めることができます。この変数は短いエラー説明で置き換えられます。`$error.message`は、より詳細なエラー説明で置き換えられます（詳細レベルは`attribute::ErrorDetail`で設定されます）。

エラーの画像/テンプレートが正常に処理できる場合は、HTTPステータス200が返されます。 この処理中にエラーが発生した場合は、HTTPエラーステータスとテキストメッセージが返されます。

## プロパティ {#section-f460c6c2dd1f46b29f9a79b093575f45}

テキスト文字列。 指定する場合、画像カタログの有効なcatalog::Id値、または`attribute::RootPath`の相対パス、またはImage Serverがアクセス可能な画像ファイルの絶対パスである必要があります。

## 初期設定 {#section-2885f289e5714ddca665a6aee401967f}

定義されていない場合は`default::ErrorImage`から継承されます。 定義済みで空の場合、`default::ErrorImage`が定義されていてもエラー画像の動作が無効になり、HTTPエラーステータスとテキストメッセージが返されます。

## 例 {#section-c92090abe1d247529542a8dd4960c2e6}

応答画像を、画像にレンダリングされるエラーメッセージと共に取得するには、まず画像カタログでテンプレートを定義する必要があります。 この場合、`onError`という名前のエントリを画像カタログに作成し、`catalog::Modifier`に次のエントリを含めます。

`size=300,300&bgc=ffffff&text=$error.message$`

テンプレートは`attribute::ErrorImage`に登録されています。

`ErrorImage=myCatalog/onError`

この例では、テキストはデフォルトのフォント、フォントカラー、フォントサイズを使用してレンダリングされます。

## 関連項目 {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) 、 [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)、 [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)、 [attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
