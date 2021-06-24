---
description: パス
solution: Experience Manager
title: パス
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 9f273f32-1699-4bc3-8dd0-f1dfefaa6e27
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 5%

---

# パス{#path}

サーバーは、[ソースデータの管理](../../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173)で説明されているパス解決ルールを使用して、データファイルを検索します。

## プロパティ {#section-72d9edc532ad43349afcb4df22e1c692}

テキスト文字列。 画像およびSVGレコードに必須で、テンプレートレコードの場合は空にすることができます。 指定する場合は、有効な相対パスまたは絶対パスのImage Serverファイルパスを指定する必要があります。 attribute:：ファイルサフィックスが存在しない場合は、DefaultExtが追加されます。

## サポートされる画像ファイル形式 {#section-8d6443c883aa48aaa00316fe9661aaa8}

サポートされている画像ファイル形式の完全なリストについては、 Image Converter(IC)ユーティリティの説明を参照してください。

複数の異なる解像度の画像データを必要とするアプリケーションは、Dynamic Media Pyramid TIFF(PTIFF)多解像度形式を使用する場合に最適です。 ICユーティリティは、サポートされている任意の画像形式からPTIFF画像を作成するために使用します。

## 初期設定 {#section-82dad83ec3f84ae8bf2f850b4139f63e}

なし

## 関連項目 {#section-b36074fae77d49f5bdfd63e9c36aa3ba}

[ICユーティリティ](../../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b)、 [attribute::RootPath](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)、 [attribute::DefaultExt](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md#reference-1b96c71a253049ddaeae09892d3484a0)、 [src=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)
