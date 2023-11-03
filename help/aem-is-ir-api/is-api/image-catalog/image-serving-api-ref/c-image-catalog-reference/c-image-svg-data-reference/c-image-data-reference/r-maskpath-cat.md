---
description: マスクファイルのパス。 このカタログレコードに関連付けられているマスク画像ファイルの相対パスまたは絶対パスと名前。
solution: Experience Manager
title: MaskPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b67e0b62-d2cc-4b05-bd09-65b206466df5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 2%

---

# MaskPath{#maskpath}

マスクファイルのパス。 このカタログレコードに関連付けられているマスク画像ファイルの相対パスまたは絶対パスと名前。

別のマスクを画像にアタッチできます。

サーバーは、 [ソースデータの管理](/help/aem-is-ir-api/is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md) をクリックして、データファイルを検索します。

## プロパティ {#section-cdc3b7e2811e41008479cd97887c01b7}

テキスト文字列値。 オプション。指定する場合は、有効な相対または絶対 Image Server ファイルパスを指定する必要があります。 `attribute::DefaultExt` ファイルサフィックスが存在しない場合はが追加されます。

両方のメイン画像 ( `catalog::Path`) とマスク画像 ( `catalog::MaskPath`) がカタログレコードで定義される場合は、両方ともピクセルサイズが同じである必要があります。 マスク画像は、8 ビットグレースケールにする必要があります。

`mask=` リクエストの上書きで `catalog::MaskPath`.

`catalog::MaskPath` メイン画像のアルファチャンネル ( `catalog::Path`) が存在する場合は、アルファチャンネルが関連付けられていない場合（つまり、プリマルチプライではない場合）は、です。 イメージのアルファがプリマルチプライされている場合、 `catalog::MaskPath` が無視され、アルファチャンネルが常に使用されます。

## 初期設定 {#section-78533e35bfec469ba087cb68a35bb81b}

なし

## 関連項目 {#section-68d262f5949c4959b8723ba44611d1dc}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md), [catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c), [mask=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md), [req=mask](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)
