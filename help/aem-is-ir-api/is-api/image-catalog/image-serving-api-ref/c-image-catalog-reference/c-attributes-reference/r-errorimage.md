---
description: エラー応答画像。 画像サービングは、通常、エラーが発生した場合に、テキストメッセージと共にエラーステータスを返します。
solution: Experience Manager
title: ErrorImage
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f412a379-525e-42fc-97bf-b10e00da6a20
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 1%

---

# ErrorImage{#errorimage}

エラー応答画像。 画像サービングは、通常、エラーが発生した場合に、テキストメッセージと共にエラーステータスを返します。

`attribute::ErrorImage` では、エラーが発生した場合に返される画像、カタログエントリ、またはテンプレートを設定できます。

>[!NOTE]
>
>見つからない画像は、 `attribute::DefaultImage`.

画像サービングテンプレートを設定して、エラーメッセージテキストを応答画像にレンダリングする場合があります。 次の事前定義済みの変数を `$error.title` 短いエラーの説明に置き換えられるテンプレート `$error.message`は、より詳細なエラーの説明で置き換えられます ( 詳細レベルは `attribute::ErrorDetail`) をクリックします。

エラーの画像/テンプレートを正常に処理できる場合は、HTTP ステータス 200 が返されます。 この処理中にエラーが発生した場合は、HTTP エラーステータスとテキストメッセージが返されます。

## プロパティ {#section-f460c6c2dd1f46b29f9a79b093575f45}

テキスト文字列。 指定する場合、画像カタログの有効な catalog::Id 値、または画像カタログの相対値 ( `attribute::RootPath`) または Image Server がアクセスできる画像ファイルの絶対パス。

## 初期設定 {#section-2885f289e5714ddca665a6aee401967f}

継承元 `default::ErrorImage` （定義されていない場合） 定義済みだが空の場合、エラー画像の動作は無効 ( `default::ErrorImage` が定義され、HTTP エラーステータスとテキストメッセージが返されます。

## 例 {#section-c92090abe1d247529542a8dd4960c2e6}

エラーメッセージが表示された応答画像を画像に取り込むには、まず画像カタログでテンプレートを定義する必要があります。 この場合、画像カタログに `onError`（に以下を含む） `catalog::Modifier`:

`size=300,300&bgc=ffffff&text=$error.message$`

テンプレートはに登録されています。 `attribute::ErrorImage`:

`ErrorImage=myCatalog/onError`

この例では、テキストはデフォルトのフォント、フォントカラー、フォントサイズを使用してレンダリングされます。

## 関連項目 {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) , [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md), [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
