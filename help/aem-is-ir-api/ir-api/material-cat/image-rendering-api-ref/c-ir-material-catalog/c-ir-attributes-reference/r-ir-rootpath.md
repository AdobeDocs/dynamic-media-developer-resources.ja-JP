---
title: RootPath
description: Source データルートパス。 テキスト文字列値。 この画像カタログで参照されるすべての周辺光量補正、テクスチャ、画像、およびICC データファイルのルートフォルダーの絶対パスまたは相対パスセグメント。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0eecb125-8147-4115-883a-cb6c38333270
TQID: 'https://experienceleague.adobe.com/yCtXjcZDG0HCqydirr7TDe5-e0oWtHmlvAxHDl-gfac'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 2%

---

# RootPath{#rootpath}

Source データルートパス。 テキスト文字列値。 この画像カタログで参照されるすべての周辺光量補正、テクスチャ、画像、およびICC データファイルのルートフォルダーの絶対パスまたは相対パスセグメント。

## プロパティ {#section-5ff1cf592dd24dfc8cfa470c753ab828}

テキスト文字列。 空、画像レンダリング サーバー設定設定`ir.resourceRootPaths`に関連する有効なパスセグメント、または有効な絶対ファイルパスである必要があります。 先頭と末尾のパス要素の区切り文字を含めないでください。

## 初期設定 {#section-4a7f3ab22b0c4090b3896d29bd192b8a}

定義されていない場合、`default::RootPath`から継承されます。 定義されていても空の場合は、ソースファイルのルートパスには影響しません。

## 関連項目 {#section-92012cc1ce32448ea977e7e0484857e2}

[ カタログ：：パス ](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590)、[ カタログ：:AuxPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969)、`ir.resourceRootPaths`
