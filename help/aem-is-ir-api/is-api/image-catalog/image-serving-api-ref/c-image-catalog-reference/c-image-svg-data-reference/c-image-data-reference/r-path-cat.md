---
description: 画像ファイルのパス
solution: Experience Manager
title: パス
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9d5417df-3aa2-4620-a614-ca71a96e2069
TQID: 'https://experienceleague.adobe.com/dpQY2E7P1LzEhYg05p6C5MQRvx9jgdMB-GrBReIIqig'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 147
ht-degree: 4%

---

# パス{#path}

画像ファイルのパス

このカタログレコードに関連付けられているソース画像ファイルの相対パスまたは絶対パスと名前。 サーバーは、Source Dataの管理に記載されているパス解決ルールを使用して、データファイルを検索します。

## プロパティ {#path-properties}

テキスト文字列。 画像レコードには必須です。テンプレートレコードには空の場合があります。 指定する場合は、有効な相対または絶対のImage Server ファイルパスである必要があります。 属性：:DefaultExtは、ファイルのサフィックスが存在しない場合に追加されます。

## サポートされている画像ファイル形式 {#path-supported-image-file-formats}

サポートされているファイル形式の完全なリストについては、Image Converter （IC）ユーティリティの説明を参照してください。

Dynamic MediaのピラミッドTIFF（PTIFF）の多解像度フォーマットを使用する場合、複数の異なる解像度の画像データを必要とするアプリケーションのパフォーマンスが最も高くなります。 IC ユーティリティは、サポートされている任意の画像形式からPTIFF画像を作成するために使用されます。

## 初期設定 {#path-default}

なし

## 関連項目 {#path-seealso}

[IC Utility](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md)、[属性：:RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)、[属性：:DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md)、[src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->
