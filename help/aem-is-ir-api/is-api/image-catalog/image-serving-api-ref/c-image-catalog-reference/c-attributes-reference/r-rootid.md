---
description: カタログ識別子。 リクエストの画像オブジェクト指定子内でこのカタログを識別するために使用される HTTP パス要素。
solution: Experience Manager
title: RootId
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9224f06d-28a9-4a23-9a3a-735b2b9f87ff
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 4%

---

# RootId{#rootid}

カタログ識別子。 リクエストの画像オブジェクト指定子内でこのカタログを識別するために使用される HTTP パス要素。

## プロパティ {#section-9a49da71de634378a06d2347790898a0}

テキスト文字列値。 HTTP パスで有効な文字のみを含めることができます。

## 初期設定 {#section-c5296f4e52394984bf1c0d265ecde940}

なし。 各カタログには、一意の `attribute::RootId` 値が必要です。 通常、[!DNL default.ini] には空の `attribute::RootId` があります。

## 関連項目 {#section-5297eaaf736b4db5901e0b37e7cb8bbe}

[catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)、[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)
