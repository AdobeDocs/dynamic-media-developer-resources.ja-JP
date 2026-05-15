---
description: パス
solution: Experience Manager
title: パス
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f2d17309-c4d0-477f-a8d8-b40f05a1a60b
TQID: 'https://experienceleague.adobe.com/qnIlWUf10fmdiQQYWeQ40c2fZojWh-AX87EsJ1zTy-A'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 129
ht-degree: 5%

---

# パス{#path}

サーバーは、[Source データの管理](../../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173)で説明されているパス解決ルールを使用して、データファイルを検索します。

## プロパティ {#section-72d9edc532ad43349afcb4df22e1c692}

テキスト文字列。 画像レコードおよびSVG レコードに必要です。テンプレートレコードには空の場合があります。 指定する場合は、有効な相対または絶対のImage Server ファイルパスである必要があります。 属性：:DefaultExtは、ファイルのサフィックスが存在しない場合に追加されます。

## サポートされる画像ファイル形式 {#section-8d6443c883aa48aaa00316fe9661aaa8}

サポートされている画像ファイル形式の完全なリストについては、画像コンバーター（IC）ユーティリティの説明を参照してください。

Dynamic MediaのピラミッドTIFF（PTIFF）の多解像度フォーマットを使用する場合、複数の異なる解像度の画像データを必要とするアプリケーションが最も効果的に機能します。 IC ユーティリティは、サポートされている任意の画像形式からPTIFF画像を作成するために使用されます。

## 初期設定 {#section-82dad83ec3f84ae8bf2f850b4139f63e}

なし

## 関連項目 {#section-b36074fae77d49f5bdfd63e9c36aa3ba}

[IC Utility](../../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b)、[属性：:RootPath](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)、[属性：:DefaultExt](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md#reference-1b96c71a253049ddaeae09892d3484a0)、[src=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)
