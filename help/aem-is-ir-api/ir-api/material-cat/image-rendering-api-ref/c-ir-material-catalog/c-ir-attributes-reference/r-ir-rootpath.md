---
description: ソースデータのルートパス。 テキスト文字列の値。 この画像カタログで参照されるすべてのビネット、テクスチャ、画像、ICCデータファイルのルートフォルダの絶対パスまたは相対パスセグメント。
solution: Experience Manager
title: RootPath *
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 0eecb125-8147-4115-883a-cb6c38333270
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---

# RootPath *{#rootpath}

ソースデータのルートパス。 テキスト文字列の値。 この画像カタログで参照されるすべてのビネット、テクスチャ、画像、ICCデータファイルのルートフォルダの絶対パスまたは相対パスセグメント。

## プロパティ {#section-5ff1cf592dd24dfc8cfa470c753ab828}

テキスト文字列。 空、画像レンダリングサーバーの設定`ir.resourceRootPaths`を基準とした相対パスセグメント、または有効な絶対ファイルパスを指定する必要があります。 先頭と末尾にパス要素の区切り文字を含めないでください。

## 初期設定 {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

定義されていない場合は`default::RootPath`から継承されます。 定義されているが空の場合、はソースファイルのルートパスに影響しません。

## 関連項目 {#section-92012cc1ce32448ea977e7e0484857e2}

[catalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) 、 [catalog::AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969)、  `ir.resourceRootPaths`
