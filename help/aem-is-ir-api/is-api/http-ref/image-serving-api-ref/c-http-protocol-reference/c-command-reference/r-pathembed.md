---
title: pathEmbed
description: パスデータを埋め込みます。 レイヤ 0 ソース イメージ ファイルのPhotoshop パスをレスポンス イメージに含めるかどうかを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a3b305eb-0313-4c58-bd47-4f87e09d0e0b
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 2%

---

# pathEmbed{#pathembed}

パスデータを埋め込みます。 レイヤ 0 ソース イメージ ファイルのPhotoshop パスをレスポンス イメージに含めるかどうかを指定します。

`pathEmbed=0|1`

## プロパティ {#section-26eb1c9e13574a0eae39f6d5b92c8995}

リクエスト属性。 ソース画像にパスデータが含まれていない場合は無視されます。 パスデータは、画像データと同様に拡大縮小および回転されます。 `layer=0` のソース画像からのパスのみが処理され、その他のレイヤー画像からのパスは無視されます。

出力画像形式がパスの埋め込みをサポートしていない場合は無視されます。 パスの埋め込みをサポートする出力画像形式のリストについては、`fmt=` の説明を参照してください。

## 制限 {#section-697cddb79a1542bc8457d2f4f59eec69}

現時点では、Photoshopのオープンパス（クローズドループを形成しないパス）をレスポンシブイメージに埋め込むことはできません。

## 初期設定 {#section-62f113ad71c04517a2741d93319a2b5d}

出力画像にパスを埋め込まない場合は `pathEmbed=0` です。

## 関連項目 {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
