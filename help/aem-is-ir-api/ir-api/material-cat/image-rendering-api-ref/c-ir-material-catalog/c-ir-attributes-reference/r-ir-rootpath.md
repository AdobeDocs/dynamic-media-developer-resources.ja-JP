---
description: ソースデータのルートパス テキスト文字列の値。 この画像カタログで参照されているすべてのビネット、テクスチャ、画像、ICCデータファイルのルートフォルダの絶対パスまたは相対パスセグメント。
solution: Experience Manager
title: RootPath *
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 3%

---


# RootPath *{#rootpath}

ソースデータのルートパス テキスト文字列の値。 この画像カタログで参照されているすべてのビネット、テクスチャ、画像、ICCデータファイルのルートフォルダの絶対パスまたは相対パスセグメント。

## プロパティ {#section-5ff1cf592dd24dfc8cfa470c753ab828}

テキスト文字列。 空、Image Rendering Server設定`ir.resourceRootPaths`に対する相対パスセグメント、または有効な絶対ファイルパスにする必要があります。 パス要素の区切り文字の先頭および末尾を含めないでください。

## 初期設定 {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

定義されていない場合は`default::RootPath`から継承されます。 定義済みで空の場合、はソースファイルのルートパスに影響しません。

## 関連項目 {#section-92012cc1ce32448ea977e7e0484857e2}

[catalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590) ,  [catalog::AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969),  `ir.resourceRootPaths`
