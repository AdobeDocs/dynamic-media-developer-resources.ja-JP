---
description: 画像ファイルのパス テクスチャまたはデカールイメージファイルの相対パスと名前。
seo-description: 画像ファイルのパス テクスチャまたはデカールイメージファイルの相対パスと名前。
seo-title: パス *
solution: Experience Manager
title: パス *
topic: Scene7 Image Serving - Image Rendering API
uuid: 9e85a358-3f2f-4b8b-a98f-03de2a1a8a4c
translation-type: tm+mt
source-git-commit: 7d3902803d42f5d479dd04ac9470a4088809f3d6

---


# パス *{#path}

画像ファイルのパス テクスチャまたはデカールイメージファイルの相対パスと名前。

サーバは、この値をと組み合わせて、実 `attribute::RootPath` 際の画像ファイルパスを作成します。 また、絶対パスにすることもできます。

テクスチャ、キャビネット、窓カバリングマテリアルのテクスチャイメージファイル、およびデカルと壁の境界マテリアルのRGBまたはRGBAイメージファイルを指定するために使用します。 キャビネットとウィンドウカバリングマテリアルの中には、繰り返し可能なテクスチャイメージを別途必要としないものもあります。

## プロパティ {#section-8c12ea24f21d4472be677581893e6681}

テキスト文字列。 テクスチャおよびデカルの材料には必須で、キャビネットおよび窓カバリング材料にはオプションです。 指定する場合、有効な相対パスまたは絶対ファイルパスを指定する必要があります。 べた塗りのマテリアルの場合は空にする必要があります。

## サポートされるファイル形式 {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

画像レンダリングは、Scene7画像サービングと同じソース画像形式をサポートします。

複数の異なる解像度の画像データを必要とするアプリケーションは、Scene7 Pyramid TIFF(PTIFF)の複数解像度形式を使用する場合に最適です。 画像サービングには、サポートされている任意の形式からPTIFF画像を作成するImage Converter(IC)ユーティリティが含まれています。

サポートされるファイル形式の完全なリストについては、画像サービングのドキュメントのICユーティリティの説明を参照してください。

## 初期設定 {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

なし

## 関連項目 {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[ICユーテ](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) ィリティ， attribute::RootPath [,](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md)[src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
