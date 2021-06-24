---
description: カタログの一致オプション。
solution: Experience Manager
title: FullMatch
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 1a267c48-a8eb-426a-a70a-bdb9f5f20efb
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 2%

---

# FullMatch{#fullmatch}

カタログの一致オプション。

カタログエントリは、HTTPリクエストで`*`rootId`*/ *`imageId`*`のペアとして指定されます。 解析時に、`*`rootId`*`がカタログの`attribute::RootId`値と一致する場合にカタログが選択され、`*`imageId`*`と`catalog::Id`値が一致すると、カタログレコードが識別されます。 カタログが見つかったが、`*`imageId`*`に一致するカタログエントリがない場合、サーバーは次の2つのいずれかを実行できます。

`attribute::FullMatch`が設定されていない場合、サーバは一致するカタログの属性を使用します。 この場合、`*`rootId`*`は`attribute::RootPath`（このカタログで指定されていない場合は`default::RootPath`）で置き換えられます。

`attribute::FullMatch`が設定されている場合、一致するカタログがないかのように、サーバはカタログを完全に無視し、デフォルトのカタログ属性を使用して処理を進めます。 この場合、`*`rootId`*`はパスの一部のままです（`default::RootPath`の前に付きます）。

## プロパティ {#section-25e021dbe6574d00aadd08a7fa0b6e81}

フラグ。 デフォルトの動作の場合は0に、完全一致動作を有効にする場合は1に設定します。

## 初期設定 {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

`default::FullMatch`から継承されます（定義されていない場合または空の場合）。

## 関連項目 {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) 、 [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
