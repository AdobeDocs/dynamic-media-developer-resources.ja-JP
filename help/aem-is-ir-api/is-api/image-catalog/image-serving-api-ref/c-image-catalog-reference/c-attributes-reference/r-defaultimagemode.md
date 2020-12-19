---
description: 初期設定の画像モード。 要求で指定された画像が見つからない場合に初期設定の画像を適用する方法を選択します。
seo-description: 初期設定の画像モード。 要求で指定された画像が見つからない場合に初期設定の画像を適用する方法を選択します。
seo-title: DefaultImageMode
solution: Experience Manager
title: DefaultImageMode
topic: Scene7 Image Serving - Image Rendering API
uuid: e5640f09-e1e3-473b-8fbc-84c6bfce2460
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---


# DefaultImageMode{#defaultimagemode}

初期設定の画像モード。 要求で指定された画像が見つからない場合に初期設定の画像を適用する方法を選択します。

## プロパティ {#section-7fa8acb63540490d9f5186231b5e77c3}

列挙。 「0」を指定すると、見つからない画像が複数のレイヤーの1つにすぎない場合でも、合成画像全体が置き換えられます。&#39;1&#39;を指定すると、見つからない各レイヤーソース画像が初期設定の画像に置き換えられ、通常どおり合成画像が返されます。

## 制限{#section-04cb0d50e8914564a8d226d0d4663c8b}

ネストされた画像レンダリング、FXGまたは`req=set`要求が失敗すると、画像サービングが`DefaultImageMode=0`に戻ります。

## 初期設定 {#section-9e318524a2a5496386901286748c7ee7}

定義されていない場合や空の場合は`default::DefaultImage`から継承されます。

## 関連項目 {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) ,  [attribute::DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
