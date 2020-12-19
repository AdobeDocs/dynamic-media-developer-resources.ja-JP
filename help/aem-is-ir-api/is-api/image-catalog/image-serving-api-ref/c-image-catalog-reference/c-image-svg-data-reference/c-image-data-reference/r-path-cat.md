---
description: 画像ファイルのパス
solution: Experience Manager
title: パス
topic: Scene7 Image Serving - Image Rendering API
uuid: 0fca88bb-de00-4eff-83ad-c0f5e3b8ece0
translation-type: tm+mt
source-git-commit: 7b837020deef888a038a074d0aa826d43e60aeb6
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# パス{#path}

画像ファイルのパス

このカタログレコードに関連付けられているソース画像ファイルの相対パスまたは絶対パスと名前。 サーバーは、ソースデータの管理で説明されているパス解決ルールを使用して、データファイルを検索します。

## プロパティ {#path-properties}

テキスト文字列。 イメージレコードに対して必須です。テンプレートレコードに対しては空にすることができます。 指定する場合は、有効なImage Serverの相対ファイルパスまたは絶対ファイルパスを指定する必要があります。 ファイルのサフィックスがない場合は、attribute::DefaultExtが追加されます。

## サポートされる画像ファイル形式{#path-supported-image-file-formats}

サポートされるファイル形式の完全なリストについては、Image Converter(IC)ユーティリティの説明を参照してください。

複数の異なる解像度で画像データを必要とするアプリケーションは、Dynamic MediaピラミッドTIFF(PTIFF)マルチ解像度形式を使用する場合に最適です。 ICユーティリティは、サポートされている任意の画像形式からPTIFF画像を作成する場合に使用します。

## 初期設定 {#path-default}

なし

## 関連項目 {#path-seealso}

[ICユーティリティ](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) 、 [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) 、 [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) 、 [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->