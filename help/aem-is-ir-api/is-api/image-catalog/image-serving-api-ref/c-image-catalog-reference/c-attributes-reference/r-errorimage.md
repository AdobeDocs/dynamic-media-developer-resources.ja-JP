---
description: エラー応答画像。 通常、画像サービングは、エラーが発生するとエラーメッセージと共にエラーステータスを返します。
solution: Experience Manager
title: ErrorImage
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f412a379-525e-42fc-97bf-b10e00da6a20
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---

# ErrorImage{#errorimage}

エラー応答画像。 通常、画像サービングは、エラーが発生するとエラーメッセージと共にエラーステータスを返します。

`attribute::ErrorImage` を使用すると、エラーが発生した場合に返される画像、カタログエントリまたはテンプレートを設定できます。

>[!NOTE]
>
>不足している画像は `attribute::DefaultImage` でも処理できます。

画像サービングテンプレートを設定できます。これにより、エラーメッセージテキストが応答画像にレンダリングされる可能性があります。 `$error.title` テンプレートには、短いエラー説明に置き換えられる次の定義済みの変数、およびより詳細なエラー説明に置き換えられる `$error.message` を含めることができます（詳細レベルは `attribute::ErrorDetail` で設定されます）。

エラー画像/テンプレートが正常に処理できた場合、HTTP ステータス 200 が返されます。 この処理中にエラーが発生した場合は、HTTP エラーステータスとテキストメッセージが返されます。

## プロパティ {#section-f460c6c2dd1f46b29f9a79b093575f45}

テキスト文字列 指定する場合は、画像カタログの有効な catalog::Id 値、または Image Server からアクセス可能な画像ファイルへの相対パス（`attribute::RootPath` に対する相対パス）または絶対パスである必要があります。

## 初期設定 {#section-2885f289e5714ddca665a6aee401967f}

定義されていない場合は `default::ErrorImage` から継承します。 定義されていても空の場合、`default::ErrorImage` が定義されていても、エラー画像の動作は無効になり、HTTP エラーステータスおよびテキストメッセージが返されます。

## 例 {#section-c92090abe1d247529542a8dd4960c2e6}

エラーメッセージを画像にレンダリングして応答画像を取得するには、まず画像カタログでテンプレートを定義する必要があります。 この例では、`catalog::Modifier` に次を含む `onError` という名前のエントリを画像カタログに作成します。

`size=300,300&bgc=ffffff&text=$error.message$`

テンプレートは `attribute::ErrorImage` に登録されます。

`ErrorImage=myCatalog/onError`

この例では、テキストはデフォルトのフォント、フォントカラーおよびフォントサイズを使用してレンダリングされます。

## 関連項目 {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)、[catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)、[attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)、[attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
