---
description: 透かしセレクター 透かし画像またはテンプレートとして使用するカタログレコードのカタログIDを指定します。
solution: Experience Manager
title: 透かし
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 54c27ea0-e87f-41ce-ae8d-71c9fabe412e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 5%

---

# 透かし{#watermark}

透かしセレクター 透かし画像またはテンプレートとして使用するカタログレコードのcatalog::Idを指定します。

指定した場合、サーバは要求されたすべてのイメージ要求(`req=img`)のイメージデータに透かしを適用する。

## プロパティ {#section-fad6ffff4c5f4b5c8010281bc1377055}

テキスト文字列。 指定する場合、この画像カタログ（または[!DNL default.ini]で指定する場合はデフォルトのカタログ）の有効な`Catalog::Id`値である必要があります。

## 初期設定 {#section-f8a2029b5b8740b2af149bdbfa28fbae}

定義されていない場合は`default::Watermark`から継承されます。 定義済みで空の場合、`default::Watermark`が定義されていても、この画像カタログに透かしは適用されません。

## 関連項目 {#section-f15dbe31013849828d78588742dde58e}

[catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
