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

このカタログレコードに関連付けられているソース画像ファイルの相対パスまたは絶対パスと名前。 サーバーは、Source データの管理で説明されているパス解決ルールを使用して、データファイルを検索します。

## プロパティ {#path-properties}

テキスト文字列 画像レコードには必須ですが、テンプレートレコードでは空にすることができます。 Image Server の有効な相対ファイルパスまたは絶対ファイルパスを指定する必要があります。 attribute::DefaultExt は、ファイルのサフィックスが存在しない場合に追加されます。

## サポートされる画像ファイル形式 {#path-supported-image-file-formats}

サポートされるファイル形式の完全なリストについては、イメージ コンバータ（IC）ユーティリティの説明を参照してください。

Dynamic Media Pyramid Format （PTIFF）マルチレゾリューションTIFFを使用する場合、複数の異なる解像度の画像データが必要なアプリケーションのパフォーマンスが最も高くなります。 IC ユーティリティは、サポートされている任意の画像形式から PTIFF 画像を作成するために使用されます。

## 初期設定 {#path-default}

なし

## 関連項目 {#path-seealso}

[IC ユーティリティ ](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md)、[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)、[attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md)、[src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->
