---
description: 透かしセレクター： 透かし画像またはテンプレートとして使用するカタログレコードのカタログ IDを指定します。
solution: Experience Manager
title: 透かし
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c27ea0-e87f-41ce-ae8d-71c9fabe412e
TQID: 'https://experienceleague.adobe.com/zajYc7BBw0BfJ6qvnTFiHY79quRa91-LdY3j1YynxVc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 104
ht-degree: 2%

---

# 透かし{#watermark}

透かしセレクター： 透かし画像またはテンプレートとして使用するカタログレコードのcatalog::Idを指定します。

指定した場合、サーバーは、すべての画像要求（`req=img`）に対して、要求された画像データに透かしを適用します。

## プロパティ {#section-fad6ffff4c5f4b5c8010281bc1377055}

テキスト文字列。 指定する場合は、この画像カタログの有効な`Catalog::Id`値である必要があります（または[!DNL default.ini]で指定する場合は、デフォルトのカタログの値）。

## 初期設定 {#section-f8a2029b5b8740b2af149bdbfa28fbae}

定義されていない場合、`default::Watermark`から継承されます。 定義されていても空の場合、`default::Watermark`が定義されていても、この画像カタログには透かしは適用されません。

## 関連項目 {#section-f15dbe31013849828d78588742dde58e}

[catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
