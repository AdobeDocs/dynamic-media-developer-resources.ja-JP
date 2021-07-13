---
description: ファイルパスをマスクします。 このカタログレコードに関連付けられているマスクイメージファイルの相対パスまたは絶対パスと名前。
solution: Experience Manager
title: MaskPath
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: b67e0b62-d2cc-4b05-bd09-65b206466df5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 3%

---

# MaskPath{#maskpath}

ファイルパスをマスクします。 このカタログレコードに関連付けられているマスクイメージファイルの相対パスまたは絶対パスと名前。

別々のマスクを画像にアタッチできます。

サーバーは、[ソースデータの管理](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md)で説明されているパス解決ルールを使用して、データファイルを検索します。

## プロパティ {#section-cdc3b7e2811e41008479cd97887c01b7}

テキスト文字列の値。 （オプション）指定する場合は、有効な相対パスまたは絶対パスのImage Serverファイルパスを指定する必要があります。 `attribute::DefaultExt` ファイルサフィックスがない場合はが追加されます。

カタログレコードにメイン画像(`catalog::Path`)とマスク画像(`catalog::MaskPath`)の両方が定義されている場合、両方の画像が同じピクセルサイズである必要があります。 マスク画像は、8ビットのグレースケールにする必要があります。

`mask=` を指定しま `catalog::MaskPath`す。

`catalog::MaskPath` メインイメージのアルファチャンネル（存在する場合） `catalog::Path`と、アルファチャンネルの関連付けが解除されている（つまり、プリマルチプライされていない）場合は、アルファチャンネルを上書きします。イメージのアルファがプリマルチプライされた場合、`catalog::MaskPath`は無視され、アルファチャンネルが常に使用されます。

## 初期設定 {#section-78533e35bfec469ba087cb68a35bb81b}

なし

## 関連項目 {#section-68d262f5949c4959b8723ba44611d1dc}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) 、 [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md)、 [catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c)、 [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md)、 [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
