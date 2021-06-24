---
description: 初期設定の画像ファイルサフィックス パスにファイルサフィックスが含まれていない場合に、カタログのパス（またはカタログのマスクパス）フィールドの値に追加されます
solution: Experience Manager
title: DefaultExt
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 43b3e5b8-6374-458d-8503-8e04c8c84233
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# DefaultExt{#defaultext}

初期設定の画像ファイルサフィックス パスにファイルサフィックスが含まれない場合は、catalog::Path （またはcatalog::MaskPath）フィールド値に追加されます。

ファイルのサフィックスは、ピリオドと、ピリオドから文字列の末尾までの1つ以上の文字で構成されます。 パスがカタログエントリに解決されない場合、および最後のパス要素にファイルサフィックスが含まれない場合、サフィックスはhttpパスに追加されます。

## プロパティ {#section-b024e6450b414ccc8b83a48a3b4e00f9}

テキスト文字列。 先頭に「。」を含める必要があります。 と1つ以上の文字。

## 初期設定 {#section-1194c36ffe0748c5b9ff7d732a506588}

定義されていない場合は`default::DefaultExt`から継承されます。 このカタログを使用する場合、定義済みで空の場合、画像名にデフォルトのサフィックスは適用されません。

## 関連項目 {#section-d7c408b979844643adff8258f500eb7c}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) 、 [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
