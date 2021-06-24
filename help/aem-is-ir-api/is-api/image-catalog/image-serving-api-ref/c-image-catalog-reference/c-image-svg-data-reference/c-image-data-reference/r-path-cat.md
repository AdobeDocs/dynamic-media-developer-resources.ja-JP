---
description: 画像ファイルのパス。
solution: Experience Manager
title: パス
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 9d5417df-3aa2-4620-a614-ca71a96e2069
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 4%

---

# パス{#path}

画像ファイルのパス。

このカタログレコードに関連付けられているソース画像ファイルの相対パスまたは絶対パスと名前。 サーバーは、ソースデータの管理で説明されているパス解決ルールを使用して、データファイルを検索します。

## プロパティ {#path-properties}

テキスト文字列。 イメージレコードの場合は必須です。テンプレートレコードの場合は空にすることができます。 指定する場合は、有効な相対パスまたは絶対パスのImage Serverファイルパスを指定する必要があります。 attribute:：ファイルサフィックスが存在しない場合は、DefaultExtが追加されます。

## サポートされる画像ファイル形式 {#path-supported-image-file-formats}

サポートされているファイル形式の完全なリストについては、 Image Converter(IC)ユーティリティの説明を参照してください。

複数の異なる解像度の画像データを必要とするアプリケーションは、Dynamic Media Pyramid TIFF(PTIFF)多解像度形式を使用する場合に最適です。 ICユーティリティは、サポートされている任意の画像形式からPTIFF画像を作成するために使用します。

## 初期設定 {#path-default}

なし

## 関連項目 {#path-seealso}

[ICユーティリティ](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) 、 [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) 、 [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) 、 [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->
