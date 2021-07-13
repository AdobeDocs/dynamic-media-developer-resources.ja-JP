---
description: 画像ファイルのパス。 テクスチャまたはデカールイメージファイルの相対パスと名前。
solution: Experience Manager
title: パス *
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 28758709-26ae-4261-b11e-34e37b9d1b8c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 3%

---

# パス *{#path}

画像ファイルのパス。 テクスチャまたはデカールイメージファイルの相対パスと名前。

サーバーは、この値を`attribute::RootPath`と組み合わせて、実際の画像ファイルパスを作成します。 また、絶対パスでもかまいません。

テクスチャ、キャビネット、窓のカバーマテリアルのテクスチャイメージファイル、およびデカル転写と壁の境界マテリアルのRGBまたはRGBAイメージファイルを指定するために使用します。 キャビネットと窓のカバー材の一部には、繰り返し可能なテクスチャイメージが必要とは限りません。

## プロパティ {#section-8c12ea24f21d4472be677581893e6681}

テキスト文字列。 テクスチャマテリアルとデカールマテリアルに必須で、キャビネットや窓カバーマテリアルにオプションです。 指定する場合は、有効な相対パスまたは絶対パスを指定する必要があります。 べた塗りのマテリアルの場合は空にする必要があります。

## サポートされているファイル形式 {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

画像レンダリングは、Dynamic Media画像サービングと同じソース画像形式をサポートします。

複数の異なる解像度の画像データを必要とするアプリケーションは、Dynamic Media Pyramid TIFF(PTIFF)多解像度形式を使用する場合に最適です。 画像サービングには、サポートされている任意の形式からPTIFF画像を作成するImage Converter(IC)ユーティリティが含まれています。

サポートされているファイル形式の完全なリストについては、画像サービングのドキュメントのICユーティリティの説明を参照してください。

## 初期設定 {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

なし

## 関連項目 {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[ICユーティリティ](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) 、 [attribute::RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md)、 [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
