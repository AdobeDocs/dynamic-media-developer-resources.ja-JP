---
description: 'null'
seo-description: 'null'
seo-title: パス
solution: Experience Manager
title: パス
topic: Scene7 Image Serving - Image Rendering API
uuid: d1ed8a98-60eb-4bdb-884e-ea08c018d834
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0

---


# パス{#path}

サーバーは、「ソースデータの管理」で説明されてい [るパス解決ルールを使用し](../../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173) 、データファイルを検索します。

## プロパティ {#section-72d9edc532ad43349afcb4df22e1c692}

テキスト文字列。 画像およびSVGレコードには必須です。テンプレートレコードには空の場合があります。 指定する場合、有効なImage Serverの相対パスまたは絶対パスを指定する必要があります。 attribute:：ファイルのサフィックスが存在しない場合は、DefaultExtが追加されます。

## サポートされる画像ファイル形式 {#section-8d6443c883aa48aaa00316fe9661aaa8}

サポートされているイメージファイル形式の完全なリストについては、Image Converter(IC)ユーティリティの説明を参照してください。

複数の異なる解像度の画像データを必要とするアプリケーションは、Scene7 Pyramid TIFF(PTIFF)の複数解像度形式を使用する場合に最適です。 ICユーティリティは、サポートされている任意のイメージ形式からPTIFFイメージを作成するために使用します。

## 初期設定 {#section-82dad83ec3f84ae8bf2f850b4139f63e}

なし

## 関連項目 {#section-b36074fae77d49f5bdfd63e9c36aa3ba}

[ICユーテ](../../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b)ィリティ， attribute::RootPath [,](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)attribute::DefaultExt [,](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md#reference-1b96c71a253049ddaeae09892d3484a0)[src=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)
