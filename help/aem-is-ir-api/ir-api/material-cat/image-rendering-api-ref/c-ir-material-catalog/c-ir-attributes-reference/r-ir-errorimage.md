---
title: ErrorImage
description: エラー応答画像。 画像レンダリングでは、通常、エラーが発生すると、エラーステータスとテキストメッセージが返されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ed48482f-79b0-4c81-b5cd-cf997f27d3ab
TQID: 'https://experienceleague.adobe.com/RRWlVPBpoUXafivRlOtzZoe5vExwnRB409SCOwhSRJI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 193
ht-degree: 1%

---

# ErrorImage {#errorimage}

エラー応答画像。 画像レンダリングでは、通常、エラーが発生すると、エラーステータスとテキストメッセージが返されます。 `attribute::ErrorImage`では、エラーが発生した場合に返される画像の設定を許可しています。

エラーが発生すると、サーバーは`ImageRendering::attribute::ErrorImage`の値を単純な画像ファイルパスとして解釈しようとします。 ファイルを開けない場合は、属性値とエラーの詳細を画像サービングに送信します。この処理は`ImageServing::attribute::ErrorImage`で説明されているように処理されます。 Image Servingが有効な応答画像を返さない場合、標準のHTTP エラーステータスとテキストメッセージがクライアントに送信されます。

エラー画像は、HTTP ステータス 200で返されます。

## プロパティ {#section-4a4a7e37ed11483db0b9922dc68ea7db}

テキスト文字列。 指定する場合は、**`ImageServing::catalog::id`**&#x200B;値、相対パス（**`ImageServing::attribute::RootPath`**&#x200B;または&#x200B;**`ImageRendering::attribute::RootPath`**）またはImage Serverからアクセスできる画像ファイルへの絶対パスのいずれかである必要があります。

## 初期設定 {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

定義されていない場合は、`default::ErrorImage`から継承されます。 定義されていても空の場合、`default::ErrorImage`が定義されていても、エラー画像の動作は無効になり、HTTP エラーステータスが返されます。

## 関連項目 {#section-3e0308eaf4124451909dacd570e27695}

[属性：:DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)、[属性：:ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b)、[属性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)、[&#x200B; カタログ：:Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)

