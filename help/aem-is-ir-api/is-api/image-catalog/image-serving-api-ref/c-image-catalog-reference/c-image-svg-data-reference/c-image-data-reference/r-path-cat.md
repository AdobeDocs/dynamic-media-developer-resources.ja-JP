---
description: 画像ファイルのパス。
solution: Experience Manager
title: パス
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9d5417df-3aa2-4620-a614-ca71a96e2069
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 4%

---

# パス{#path}

画像ファイルのパス。

このカタログレコードに関連付けられたソース画像ファイルの相対パスまたは絶対パスと名前。 サーバーは、ソース・データの管理で説明されているパス解決ルールを使用して、データ・ファイルを検索します。

## プロパティ {#path-properties}

テキスト文字列。 画像レコードに必須です。テンプレートレコードの場合は空にすることができます。 指定する場合は、有効な相対または絶対 Image Server ファイルパスを指定する必要があります。 ファイルサフィックスが存在しない場合は、attribute::DefaultExt が追加されます。

## サポートされている画像ファイル形式 {#path-supported-image-file-formats}

サポートされているファイル形式の完全なリストについては、画像コンバーター (IC) ユーティリティの説明を参照してください。

複数の異なる解像度の画像データを必要とするアプリケーションは、Dynamic Media PTIFF(Pyramid Resolution) マルチTIFF形式を使用する場合に最も高いパフォーマンスを発揮します。 IC ユーティリティは、サポートされている任意の画像形式から PTIFF 画像を作成するために使用します。

## 初期設定 {#path-default}

なし

## 関連項目 {#path-seealso}

[IC ユーティリティ](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) , [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->
