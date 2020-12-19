---
description: エラー応答画像。 画像サービングは、通常、エラーが発生した場合に、テキストメッセージと共にエラーステータスを返します。
seo-description: エラー応答画像。 画像サービングは、通常、エラーが発生した場合に、テキストメッセージと共にエラーステータスを返します。
seo-title: ErrorImage
solution: Experience Manager
title: ErrorImage
topic: Scene7 Image Serving - Image Rendering API
uuid: b071c0cd-e7b8-422b-9b23-d93f504d9ce5
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 1%

---


# ErrorImage{#errorimage}

エラー応答画像。 画像サービングは、通常、エラーが発生した場合に、テキストメッセージと共にエラーステータスを返します。

`attribute::ErrorImage` エラーが発生した場合に返す画像、カタログエントリ、またはテンプレートを設定できます。

>[!NOTE]
>
>見つからない画像は`attribute::DefaultImage`で処理することもできます。

画像サービングテンプレートを設定すると、エラーメッセージテキストが応答画像にレンダリングされる場合があります。 次の定義済みの変数を`$error.title`テンプレートに含めることができます。このテンプレートは短いエラー説明で置き換えられます。`$error.message`は、より詳細なエラー説明で置き換えられます（詳細レベルは`attribute::ErrorDetail`で設定されます）。

エラーの画像/テンプレートを正常に処理できる場合、HTTPステータス200が返されます。 この処理中にエラーが発生した場合は、HTTPエラーステータスとテキストメッセージが返されます。

## プロパティ {#section-f460c6c2dd1f46b29f9a79b093575f45}

テキスト文字列。 指定する場合、画像カタログ内の有効なcatalog::Id値、またはImage Serverがアクセスできる画像ファイルの相対パス（`attribute::RootPath`から）または絶対パスである必要があります。

## 初期設定 {#section-2885f289e5714ddca665a6aee401967f}

定義されていない場合は`default::ErrorImage`から継承されます。 定義済みで空の場合、`default::ErrorImage`が定義されていて、HTTPエラーステータスとテキストメッセージが返される場合でも、エラーイメージの動作は無効になります。

## 例 {#section-c92090abe1d247529542a8dd4960c2e6}

応答画像を取得し、画像にレンダリングされるエラーメッセージを表示するには、まず画像カタログでテンプレートを定義する必要があります。 この場合、画像カタログに`onError`というエントリを作成し、`catalog::Modifier`に次のエントリを含めます。

`size=300,300&bgc=ffffff&text=$error.message$`

テンプレートは`attribute::ErrorImage`に登録されています：

`ErrorImage=myCatalog/onError`

次の例では、テキストはデフォルトのフォント、フォントの色、フォントサイズを使用してレンダリングされます。

## 関連項目 {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) 、 [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)、 [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)、 [attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
