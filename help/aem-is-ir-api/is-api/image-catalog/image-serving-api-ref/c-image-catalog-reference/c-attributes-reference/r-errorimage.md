---
description: エラー応答画像。 画像サービングは、通常、エラーが発生した場合、エラーステータスとテキストメッセージを返します。
seo-description: エラー応答画像。 画像サービングは、通常、エラーが発生した場合、エラーステータスとテキストメッセージを返します。
seo-title: ErrorImage
solution: Experience Manager
title: ErrorImage
topic: Scene7 Image Serving - Image Rendering API
uuid: b071c0cd-e7b8-422b-9b23-d93f504d9ce5
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# ErrorImage{#errorimage}

エラー応答画像。 画像サービングは、通常、エラーが発生した場合、エラーステータスとテキストメッセージを返します。

`attribute::ErrorImage` エラーが発生した場合に返す画像、カタログエントリまたはテンプレートを設定できます。

>[!NOTE]
>
>見つからない画像は、を使用して処理することもできま `attribute::DefaultImage`す。

画像サービングテンプレートを設定すると、応答画像にエラーメッセージテキストが表示される場合があります。 次の事前定義された変数をテンプレートに含めることができます。この変数は、短いエラーの説明で置き換えられ、より詳細なエラーの説明で置き換えられます `$error.title` (詳細レベルは、を使用して設定されま `$error.message``attribute::ErrorDetail`す)。

エラー画像/テンプレートが正常に処理できる場合、HTTPステータス200が返されます。 この処理中にエラーが発生した場合は、HTTPエラーステータスとテキストメッセージが返されます。

## プロパティ {#section-f460c6c2dd1f46b29f9a79b093575f45}

テキスト文字列。 指定する場合、画像カタログ内の有効なcatalog::Id値、またはImage Serverがアクセス可能な画像ファイルの相対パス( `attribute::RootPath`～)または絶対パスである必要があります。

## 初期設定 {#section-2885f289e5714ddca665a6aee401967f}

定義されていな `default::ErrorImage` い場合は、から継承。 定義済みで空の場合、エラー画像の動作は、定義済みの場合でも無効になり、HTTP `default::ErrorImage` エラーステータスとテキストメッセージが返されます。

## 例 {#section-c92090abe1d247529542a8dd4960c2e6}

応答画像を取得し、画像にエラーメッセージをレンダリングするには、まず画像カタログでテンプレートを定義する必要があります。 この場合、画像カタログに次のエントリを含む、とい `onError`うエントリを作成しま `catalog::Modifier`す。

`size=300,300&bgc=ffffff&text=$error.message$`

テンプレートの登録には、次のものが使用されま `attribute::ErrorImage`す。

`ErrorImage=myCatalog/onError`

この例では、テキストはデフォルトのフォント、フォントの色、フォントサイズを使用してレンダリングされます。

## 関連項目 {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) 、 [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)、 [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)、 [attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
