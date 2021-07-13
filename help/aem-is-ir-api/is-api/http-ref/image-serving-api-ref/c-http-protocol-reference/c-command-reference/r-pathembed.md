---
description: パスデータを埋め込みます。 レイヤー0のソース画像ファイルのPhotoshopパスを応答画像に含めるかどうかを指定します。
solution: Experience Manager
title: pathEmbed
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: a3b305eb-0313-4c58-bd47-4f87e09d0e0b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---

# pathEmbed{#pathembed}

パスデータを埋め込みます。 レイヤー0のソース画像ファイルのPhotoshopパスを応答画像に含めるかどうかを指定します。

`pathEmbed=0|1`

## プロパティ {#section-26eb1c9e13574a0eae39f6d5b92c8995}

リクエスト属性。 ソース画像にパスデータが含まれていない場合は無視されます。 パスデータは、画像データと同様に、拡大/縮小および回転されます。 `layer=0`のソースイメージからのパスのみが処理されます。他のレイヤーイメージからのパスは無視されます。

出力画像形式がパスの埋め込みをサポートしていない場合は無視されます。 パスの埋め込みをサポートする出力画像形式のリストについては、 `fmt=`の説明を参照してください。

## 制限事項 {#section-697cddb79a1542bc8457d2f4f59eec69}

現時点では、開いたPhotoshopパス（閉じたループを形成しないパス）の応答画像への埋め込みはサポートされていません。

## 初期設定 {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`（出力画像にパスを埋め込まない場合）。

## 関連項目 {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
