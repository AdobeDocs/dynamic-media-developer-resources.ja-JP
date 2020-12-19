---
description: デフォルトの返信画像形式。 返信画像の初期設定の形式を指定します。
seo-description: デフォルトの返信画像形式。 返信画像の初期設定の形式を指定します。
seo-title: 形式
solution: Experience Manager
title: 形式
topic: Scene7 Image Serving - Image Rendering API
uuid: d09b0a45-ea89-4c00-a6ac-065ffad51611
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 11%

---


# 形式{#format}

デフォルトの返信画像形式。 返信画像の初期設定の形式を指定します。

## プロパティ {#section-3cbea775a174443aaf14e9e58a3c2300}

テキスト文字列。 `fmt=`コマンドでサポートされる形式トークンの1つである必要があります。

`jpg | jpeg | png | png-alpha | tif | tif-alpha | swf | swf-alpha | pdf | eps | gif | gif-alpha`

## 初期設定 {#section-256b0f8afdd846eaac68ec2019258708}

定義されていない場合や空の場合は`default::Format`から継承されます。

## 関連項目 {#section-d6dc53ae28ab4133a9f8f9ec0bc159a6}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)
