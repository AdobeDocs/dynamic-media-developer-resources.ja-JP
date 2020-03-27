---
description: カタログの一致オプション。
seo-description: カタログの一致オプション。
seo-title: FullMatch
solution: Experience Manager
title: FullMatch
topic: Scene7 Image Serving - Image Rendering API
uuid: 0c69ba92-1411-4cb7-ac28-d26fe035222f
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# FullMatch{#fullmatch}

カタログの一致オプション。

カタログエントリは、HTTPリクエストで ` *``*/ *`rootIdimageId`*` のペアとして指定されます。 解析時に、 ` *`rootId`*` がカタログの値と一致 `attribute::RootId` する場合はカタログが選択され、imageIdと値の一致でカタログレコードが ` *`識別され`*``catalog::Id` ます。 カタログが見つかったが、imageIdに一致するカタログエントリがな ` *`い場合`*`、サーバは次の2つのいずれかを実行できます。

が設定 `attribute::FullMatch` されていない場合、一致したカタログの属性が使用されます。 この場合、 ` *`rootIdは`*` (またはこのカ `attribute::RootPath` タログ `default::RootPath`で指定されていない場合は)に置き換えられます。

を設定 `attribute::FullMatch` すると、一致するカタログがない場合と同様に、サーバはカタログを完全に無視し、初期設定のカタログ属性を使用して処理を続行します。 この場合、 ` *`rootId`*` はパスの一部(先頭に「」が付く `default::RootPath`)のままです。

## プロパティ {#section-25e021dbe6574d00aadd08a7fa0b6e81}

フラグ。 デフォルトの動作を0に設定するか、完全一致動作を有効にする場合は1に設定します。

## 初期設定 {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

定義されていな `default::FullMatch` い場合や空の場合に継承されます。

## 関連項目 {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) , [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
