---
description: カタログマッチングオプション：
solution: Experience Manager
title: FullMatch
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a267c48-a8eb-426a-a70a-bdb9f5f20efb
TQID: 'https://experienceleague.adobe.com/5eTvORUSVsXHReAaiVMGSizooDQ9Wq--dXrBo0c9C7c'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 160
ht-degree: 1%

---

# FullMatch{#fullmatch}

カタログマッチングオプション：

カタログエントリは、HTTP リクエストで`*`rootId`*/ *`imageId`*` ペアとして指定されます。 パース時に、`*`rootId`*`がカタログの`attribute::RootId`値と一致し、`*`imageId`*`が`catalog::Id`値と一致することでカタログレコードが識別される場合、カタログが選択されます。 カタログが見つかっても、`*`imageId`*`に一致するカタログエントリがない場合、サーバーは2つのいずれかを実行できます。

`attribute::FullMatch`が設定されていない場合、サーバーは一致したカタログの属性を使用します。 この場合、`*`rootId`*`は`attribute::RootPath` （このカタログで指定されていない場合は`default::RootPath`）に置き換えられます。

`attribute::FullMatch`が設定されている場合、カタログが一致していないかのように、サーバーはカタログを完全に無視し、デフォルトのカタログ属性を使用して続行します。 この場合、`*`rootId`*`はパスの一部のままになります（先頭に`default::RootPath`）。

## プロパティ {#section-25e021dbe6574d00aadd08a7fa0b6e81}

フラグ： デフォルトの動作は0に設定し、フルマッチングを有効にするには1に設定します。

## 初期設定 {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

定義されていない場合や空の場合は、`default::FullMatch`から継承されます。

## 関連項目 {#section-42da0ba53e0b4c089c62108785faf5a9}

[属性：:RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)、[&#x200B; カタログ：:Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
