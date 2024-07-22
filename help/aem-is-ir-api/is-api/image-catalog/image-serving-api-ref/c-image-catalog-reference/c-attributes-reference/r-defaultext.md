---
description: デフォルトの画像ファイルサフィックス。 パスにファイルサフィックスが含まれていない場合に、カタログの「パス」（またはカタログの「MaskPath」）フィールド値に追加されます
solution: Experience Manager
title: DefaultExt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 43b3e5b8-6374-458d-8503-8e04c8c84233
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---

# DefaultExt{#defaultext}

デフォルトの画像ファイルサフィックス。 パスにファイルのサフィックスが含まれていない場合は、catalog::Path （または catalog::MaskPath） フィールドの値に追加します。

ファイルサフィックスは、ピリオドと、文字列のピリオドから末尾までの 1 つ以上の文字で構成されます。 パスがカタログエントリを解決せず、最後のパス要素にファイルサフィックスが含まれていない場合、サフィックスが http パスに追加されます。

## プロパティ {#section-b024e6450b414ccc8b83a48a3b4e00f9}

テキスト文字列 先頭に「。」を含める必要があります。 1 文字以上の文字。

## 初期設定 {#section-1194c36ffe0748c5b9ff7d732a506588}

定義されていない場合は `default::DefaultExt` から継承します。 定義されているが空の場合、このカタログを使用するときに画像名にデフォルトのサフィックスは適用されません。

## 関連項目 {#section-d7c408b979844643adff8258f500eb7c}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md)、[catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
