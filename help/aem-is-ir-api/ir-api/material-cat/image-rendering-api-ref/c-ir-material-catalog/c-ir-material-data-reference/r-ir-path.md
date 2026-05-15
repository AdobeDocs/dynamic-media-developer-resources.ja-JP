---
description: 画像ファイルのパス テクスチャまたはデカール画像ファイルの相対パスと名前。
solution: Experience Manager
title: パス *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28758709-26ae-4261-b11e-34e37b9d1b8c
TQID: 'https://experienceleague.adobe.com/ndDZ1MOPM1GHqOKFkwwMnJoZHVjaCeVVEHudb-5fPk0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 208
ht-degree: 1%

---

# パス *{#path}

画像ファイルのパス テクスチャまたはデカール画像ファイルの相対パスと名前。

サーバーは、この値と`attribute::RootPath`を組み合わせて、実際の画像ファイルのパスを構築します。 絶対パスにもできます。

テクスチャ、キャビネット、窓カバーのマテリアルのテクスチャ画像ファイル、デカールや壁の境界線のマテリアルのRGBまたはRGBA画像ファイルを指定するために使用します。 すべてのキャビネットと窓のカバー材料が別々の繰り返し可能なテクスチャ画像を必要とするわけではありません。

## プロパティ {#section-8c12ea24f21d4472be677581893e6681}

テキスト文字列。 テクスチャやデカール素材に必要で、キャビネットや窓のカバー素材にはオプションです。 指定する場合は、有効な相対または絶対ファイルパスである必要があります。 単色マテリアルの場合は空にする必要があります。

## サポートされるファイル形式 {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

画像レンダリングでは、Dynamic Media Image Servingと同じソース画像形式をサポートしています。

Dynamic MediaのピラミッドTIFF（PTIFF）の多解像度フォーマットを使用する場合、複数の異なる解像度の画像データを必要とするアプリケーションが最も効果的に機能します。 Image Servingには、サポートされている任意の形式からPTIFF画像を作成するImage Converter （IC）ユーティリティが含まれています。

サポートされているファイル形式の完全なリストについては、「画像サービング」ドキュメントのIC ユーティリティの説明を参照してください。

## 初期設定 {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

なし

## 関連項目 {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[IC ユーティリティ &#x200B;](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md)、[属性：:RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md)、[src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
