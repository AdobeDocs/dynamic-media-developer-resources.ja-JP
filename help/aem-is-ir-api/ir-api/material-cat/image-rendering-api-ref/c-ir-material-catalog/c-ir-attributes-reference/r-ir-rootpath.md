---
description: ソースデータのルートパス テキスト文字列値。 この画像カタログで参照されるすべてのビネット、テクスチャ、画像、ICCデータファイルのルートフォルダの絶対パスまたは相対パスセグメント。
seo-description: ソースデータのルートパス テキスト文字列値。 この画像カタログで参照されるすべてのビネット、テクスチャ、画像、ICCデータファイルのルートフォルダの絶対パスまたは相対パスセグメント。
seo-title: RootPath *
solution: Experience Manager
title: RootPath *
topic: Scene7 Image Serving - Image Rendering API
uuid: a23ea524-8ca4-47c4-83a5-64a174d8767e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# RootPath *{#rootpath}

ソースデータのルートパス テキスト文字列値。 この画像カタログで参照されるすべてのビネット、テクスチャ、画像、ICCデータファイルのルートフォルダの絶対パスまたは相対パスセグメント。

## プロパティ {#section-5ff1cf592dd24dfc8cfa470c753ab828}

テキスト文字列。 空、Image Rendering Serverの設定に対する相対パスセグメント、または有効な絶対フ `ir.resourceRootPaths`ァイルパスである必要があります。 パス要素の区切り文字の先頭と末尾を含めないでください。

## 初期設定 {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

定義されていな `default::RootPath` い場合は、から継承。 定義済みで空の場合、はソースファイルのルートパスに影響しません。

## 関連項目 {#section-92012cc1ce32448ea977e7e0484857e2}

[catalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) 、 [catalog::AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969)、 `ir.resourceRootPaths`
