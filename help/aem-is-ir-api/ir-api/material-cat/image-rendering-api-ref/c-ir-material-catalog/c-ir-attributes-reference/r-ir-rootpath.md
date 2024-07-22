---
title: RootPath
description: Source データのルートパス。 テキスト文字列値。 この画像カタログが参照するすべてのビネット、テクスチャ、画像および ICC データファイルのルートフォルダーの絶対パスまたは相対パスセグメント。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0eecb125-8147-4115-883a-cb6c38333270
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 2%

---

# RootPath{#rootpath}

Source データのルートパス。 テキスト文字列値。 この画像カタログが参照するすべてのビネット、テクスチャ、画像および ICC データファイルのルートフォルダーの絶対パスまたは相対パスセグメント。

## プロパティ {#section-5ff1cf592dd24dfc8cfa470c753ab828}

テキスト文字列 空、画像レンダリングサーバー設定 `ir.resourceRootPaths` を基準とした有効なパスセグメント、または有効な絶対ファイルパスを指定する必要があります。 先頭および末尾のパス要素の区切り文字を含めないでください。

## 初期設定 {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

定義されていない場合は `default::RootPath` から継承します。 定義されていても空の場合、ソースファイルのルートパスには影響しません。

## 関連項目 {#section-92012cc1ce32448ea977e7e0484857e2}

[catalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590)、[catalog::AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969)、`ir.resourceRootPaths`
