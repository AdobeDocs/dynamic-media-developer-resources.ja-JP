---
description: デフォルトの画像ファイルサフィックス。 パスにファイルサフィックスが含まれていない場合は、カタログパス（またはカタログマスクパス）フィールド値に追加されます
solution: Experience Manager
title: DefaultExt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 43b3e5b8-6374-458d-8503-8e04c8c84233
TQID: 'https://experienceleague.adobe.com/3juJVbcGdP1Z-F5inwe-Do7vkk80T-SNJmAiotjU6iw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 139
ht-degree: 2%

---

# DefaultExt{#defaultext}

デフォルトの画像ファイルサフィックス。 パスにファイルサフィックスが含まれていない場合は、catalog::Path （またはcatalog::MaskPath）フィールド値に追加されます

ファイルの接尾辞は、ピリオドと、ピリオドと文字列の末尾の間の1つ以上の文字で構成されます。 サフィックスは、パスがカタログエントリに解決しない場合、および最後のパス要素にファイルサフィックスが含まれていない場合に、http パスに追加されます。

## プロパティ {#section-b024e6450b414ccc8b83a48a3b4e00f9}

テキスト文字列。 先頭に「。」と1文字以上を含める必要があります。

## 初期設定 {#section-1194c36ffe0748c5b9ff7d732a506588}

定義されていない場合、`default::DefaultExt`から継承されます。 定義されていても空の場合、このカタログを使用する際に、画像名にデフォルトのサフィックスは適用されません。

## 関連項目 {#section-d7c408b979844643adff8258f500eb7c}

[ カタログ：：パス ](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md)、[ カタログ：:MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
