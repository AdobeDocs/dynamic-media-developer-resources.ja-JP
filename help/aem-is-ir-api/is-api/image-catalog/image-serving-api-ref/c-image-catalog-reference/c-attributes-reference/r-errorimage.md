---
description: エラー応答画像。 Image Servingは通常、エラーが発生すると、エラーステータスをテキストメッセージで返します。
solution: Experience Manager
title: ErrorImage
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f412a379-525e-42fc-97bf-b10e00da6a20
TQID: 'https://experienceleague.adobe.com/eV8TNAf3uQZgspn0DjSE463ltmCNL0xwl7Kd2hT7gHk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 1%

---

# ErrorImage{#errorimage}

エラー応答画像。 Image Servingは通常、エラーが発生すると、エラーステータスをテキストメッセージで返します。

`attribute::ErrorImage`では、エラーが発生した場合に、画像、カタログ エントリ、またはテンプレートを返すように設定できます。

>[!NOTE]
>
>画像が見つからない場合は、`attribute::DefaultImage`でも処理できます。

画像サービングテンプレートは、エラーメッセージテキストを応答画像にレンダリングするように設定できます。 次の定義済み変数は、`$error.title` テンプレートに含めることができます。このテンプレートは、短いエラーの説明で置き換えられ、`$error.message`は、より詳細なエラーの説明で置き換えられます（詳細レベルは`attribute::ErrorDetail`で設定されています）。

エラー画像/テンプレートを正常に処理できる場合は、HTTP ステータス 200が返されます。 この処理中にエラーが発生した場合、HTTP エラーステータスとテキストメッセージが返されます。

## プロパティ {#section-f460c6c2dd1f46b29f9a79b093575f45}

テキスト文字列。 指定する場合は、画像カタログ内の有効なカタログ : : Id値、または画像サーバーがアクセスできる画像ファイルへの相対パス（`attribute::RootPath`）または絶対パスである必要があります。

## 初期設定 {#section-2885f289e5714ddca665a6aee401967f}

定義されていない場合、`default::ErrorImage`から継承されます。 定義されていても空の場合、`default::ErrorImage`が定義されていても、エラー画像の動作は無効になり、HTTP エラーステータスとテキストメッセージが返されます。

## 例 {#section-c92090abe1d247529542a8dd4960c2e6}

エラーメッセージが画像にレンダリングされた応答画像を取得するには、まず画像カタログでテンプレートを定義する必要があります。 この場合、`onError`という名前の画像カタログにエントリを作成し、`catalog::Modifier`に以下を含めます。

`size=300,300&bgc=ffffff&text=$error.message$`

テンプレートは`attribute::ErrorImage`に登録されています：

`ErrorImage=myCatalog/onError`

この例では、デフォルトのフォント、フォントカラー、フォントサイズを使用してテキストがレンダリングされます。

## 関連項目 {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[属性：:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)、[&#x200B; カタログ：:Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)、[属性：:DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)、[属性：:ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
