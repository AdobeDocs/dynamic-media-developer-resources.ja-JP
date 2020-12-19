---
description: パスデータを埋め込みます。 レイヤー0のソース画像ファイルからのPhotoshopパスを応答画像に含めるかどうかを指定します。
seo-description: パスデータを埋め込みます。 レイヤー0のソース画像ファイルからのPhotoshopパスを応答画像に含めるかどうかを指定します。
seo-title: pathEmbed
solution: Experience Manager
title: pathEmbed
topic: Scene7 Image Serving - Image Rendering API
uuid: 93e63c7c-c091-4bb1-baff-45706fd611ea
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 2%

---


# pathEmbed{#pathembed}

パスデータを埋め込みます。 レイヤー0のソース画像ファイルからのPhotoshopパスを応答画像に含めるかどうかを指定します。

`pathEmbed=0|1`

## プロパティ {#section-26eb1c9e13574a0eae39f6d5b92c8995}

要求属性。 ソース画像にパスデータが含まれていない場合は無視されます。 パスデータは、画像データと同様に拡大・縮小・回転される。 `layer=0`のソースイメージからのパスのみが処理されます。他のレイヤー画像からのパスは無視されます。

出力画像形式でパスの埋め込みがサポートされていない場合は無視されます。 パスの埋め込みをサポートする出力画像形式のリストについては、`fmt=`の説明を参照してください。

## 制限{#section-697cddb79a1542bc8457d2f4f59eec69}

現在、オープンPhotoshopパス（閉じたループを形成しないパス）は、応答画像への埋め込みに対してはサポートされていません。

## 初期設定 {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`を使用します。出力画像にパスを埋め込む必要はありません。

## 関連項目 {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
