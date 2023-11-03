---
description: パス
solution: Experience Manager
title: パス
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f2d17309-c4d0-477f-a8d8-b40f05a1a60b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 5%

---

# パス{#path}

サーバーは、 [ソースデータの管理](../../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173) をクリックして、データファイルを検索します。

## プロパティ {#section-72d9edc532ad43349afcb4df22e1c692}

テキスト文字列。 画像およびSVGレコードに必須です。テンプレートレコードの場合は空にすることができます。 指定する場合は、有効な相対または絶対 Image Server ファイルパスを指定する必要があります。 ファイルサフィックスが存在しない場合は、attribute::DefaultExt が追加されます。

## サポートされる画像ファイル形式 {#section-8d6443c883aa48aaa00316fe9661aaa8}

サポートされている画像ファイル形式の完全なリストについては、画像コンバーター (IC) ユーティリティの説明を参照してください。

複数の異なる解像度の画像データを必要とするアプリケーションは、Dynamic MediaピラミッドTIFF(PTIFF) 複数解像度形式を使用する場合に最も高いパフォーマンスを発揮します。 IC ユーティリティは、サポートされている任意の画像形式から PTIFF 画像を作成するために使用します。

## 初期設定 {#section-82dad83ec3f84ae8bf2f850b4139f63e}

なし

## 関連項目 {#section-b36074fae77d49f5bdfd63e9c36aa3ba}

[IC ユーティリティ](../../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [attribute::RootPath](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [attribute::DefaultExt](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md#reference-1b96c71a253049ddaeae09892d3484a0), [src=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)
