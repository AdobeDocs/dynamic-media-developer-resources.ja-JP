---
description: アセットタイプ. カタログ画像セットに公開されるセットのタイプを識別するために使用します。
solution: Experience Manager
title: AssetType
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 84530842-4d2a-402a-b94b-45356cec5dc1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 13%

---

# AssetType{#assettype}

アセットタイプ. catalog::ImageSetに公開されるセットのタイプを識別するために使用します。

アセットタイプによって、`req=set`リクエストに対して生成する応答のタイプが決まります。 値が指定されていない場合、自動検出ルールは`req=set`応答タイプを決定します。

## プロパティ {#properties}

次のセットの列挙値：

MEDIASET

SPINSET

SPINSET2D

VIDEOSET

IMAGESET

ECATALOG

## 初期設定 {#section-b94ce61423194729918456103ef3f72c}

なし

## 関連項目 {#section-235f9f5522024d3682ee7cc0101eb7ba}

[catalog::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) 、 [req=set](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)、メディアセッ [トの要求](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md)
