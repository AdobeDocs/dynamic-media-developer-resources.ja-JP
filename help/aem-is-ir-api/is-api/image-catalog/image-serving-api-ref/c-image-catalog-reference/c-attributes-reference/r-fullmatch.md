---
description: カタログの一致オプション
seo-description: カタログの一致オプション
seo-title: FullMatch
solution: Experience Manager
title: FullMatch
topic: Scene7 Image Serving - Image Rendering API
uuid: 0c69ba92-1411-4cb7-ac28-d26fe035222f
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 2%

---


# FullMatch{#fullmatch}

カタログの一致オプション

カタログエントリは、HTTPリクエストで` *`rootId`*/ *`imageId`*`のペアとして指定されます。 解析時に、` *`rootId`*`がカタログの`attribute::RootId`値と一致する場合はカタログが選択され、` *`imageId`*`と`catalog::Id`値が一致するとカタログレコードが識別されます。 カタログが見つかったが、` *`imageId`*`に一致するカタログエントリがない場合、サーバは次の2つのいずれかを実行できます。

`attribute::FullMatch`が設定されていない場合、サーバは一致したカタログの属性を使用します。 この場合、` *`rootId`*`は`attribute::RootPath`(または`default::RootPath`（このカタログで指定されていない場合）に置き換えられます。

`attribute::FullMatch`が設定されている場合、一致するカタログがない場合と同様に、サーバはカタログを完全に無視し、初期設定のカタログ属性を使用して処理を続行します。 この場合、` *`rootId`*`はパスの一部として残ります（`default::RootPath`の先頭に付加されます）。

## プロパティ {#section-25e021dbe6574d00aadd08a7fa0b6e81}

フラグ。 初期設定の動作は0に、完全一致動作は1に設定します。

## 初期設定 {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

定義されていない場合や空の場合は`default::FullMatch`から継承されます。

## 関連項目 {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) ,  [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
