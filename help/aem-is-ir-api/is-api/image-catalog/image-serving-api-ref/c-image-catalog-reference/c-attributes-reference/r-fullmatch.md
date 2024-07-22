---
description: カタログマッチングオプション。
solution: Experience Manager
title: FullMatch
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a267c48-a8eb-426a-a70a-bdb9f5f20efb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 1%

---

# FullMatch{#fullmatch}

カタログマッチングオプション。

カタログエントリは、HTTP リクエストで `*`rootId`*/ *`imageId`*` ペアとして指定されます。 構文解析時には、`*`rootId`*` がカタログの `attribute::RootId` 値と一致する場合にカタログが選択され、`*`imageId`*` が `catalog::Id` 値と一致することでカタログレコードが識別されます。 カタログが見つかったが、`*`imageId`*` と一致するカタログエントリがない場合、サーバーは次の 2 つのいずれかを実行できます。

`attribute::FullMatch` が設定されていない場合、サーバーは一致したカタログの属性を使用します。 この場合、`*`rootId`*` は `attribute::RootPath` （または、このカタログで指定されていない場合は `default::RootPath`）に置き換えられます。

`attribute::FullMatch` が設定されている場合、サーバーは、カタログが一致しなかったかのようにカタログを完全に無視し、デフォルトのカタログ属性を使用して続行します。 この場合、`*`rootId`*` はパスの一部のままになります（パスの先頭には `default::RootPath` が付きます）。

## プロパティ {#section-25e021dbe6574d00aadd08a7fa0b6e81}

フラグ。 デフォルトの動作の場合は 0 に、フルマッチの動作を有効にする場合は 1 に設定します。

## 初期設定 {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

定義されていない場合または空の場合は `default::FullMatch` から継承します。

## 関連項目 {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) , [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
