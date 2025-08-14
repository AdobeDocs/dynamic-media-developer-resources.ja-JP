---
description: デフォルトの画像モード。 リクエストで指定された画像が見つからない場合のデフォルト画像の適用方法を選択します。
solution: Experience Manager
title: DefaultImageMode
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b30ce72f-7c74-407c-bd4a-042b84c469e9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 2%

---

# DefaultImageMode{#defaultimagemode}

デフォルトの画像モード。 リクエストで指定された画像が見つからない場合のデフォルト画像の適用方法を選択します。

## プロパティ {#section-7fa8acb63540490d9f5186231b5e77c3}

列挙値。 「0」：足りない画像がいくつかのレイヤーの 1 つにすぎない場合でも、合成画像全体を置き換えます。「1」：足りない各レイヤーソース画像をデフォルトの画像に置き換え、通常どおり合成を返します。

## 制限 {#section-04cb0d50e8914564a8d226d0d4663c8b}

ネストされた画像レンダリング、FXG または `DefaultImageMode=0` リクエストが失敗すると、画像サービングは `req=set` に戻ります。

## 初期設定 {#section-9e318524a2a5496386901286748c7ee7}

定義されていない場合または空の場合は `default::DefaultImage` から継承します。

## 関連項目 {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) , [attribute::DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
