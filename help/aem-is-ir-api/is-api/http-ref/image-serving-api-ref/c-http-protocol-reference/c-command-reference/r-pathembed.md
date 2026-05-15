---
title: pathEmbed
description: パスのデータを埋め込みます。 レイヤー0のソース画像ファイルのPhotoshop パスをレスポンス画像に含めるかどうかを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a3b305eb-0313-4c58-bd47-4f87e09d0e0b
TQID: 'https://experienceleague.adobe.com/ES7nAoYjO6Y4naU2c5TIPotPUTjncwjRMLL7-4--XpE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 146
ht-degree: 2%

---

# pathEmbed{#pathembed}

パスのデータを埋め込みます。 レイヤー0のソース画像ファイルのPhotoshop パスをレスポンス画像に含めるかどうかを指定します。

`pathEmbed=0|1`

## プロパティ {#section-26eb1c9e13574a0eae39f6d5b92c8995}

リクエスト属性： ソース画像にパスデータが含まれていない場合は無視されます。 パスのデータは、画像データと同様に拡大・縮小および回転されます。 ソース画像`layer=0`のパスのみが処理されます。他のレイヤー画像のパスは無視されます。

出力画像フォーマットがパス埋め込みをサポートしていない場合は無視されます。 パスの埋め込みをサポートする出力画像形式の一覧については、`fmt=`の説明を参照してください。

## 制限 {#section-697cddb79a1542bc8457d2f4f59eec69}

現時点では、オープン Photoshop パス（クローズドループを形成しないパス）は、レスポンス画像への埋め込みはサポートされていません。

## 初期設定 {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`。出力画像にパスを埋め込みません。

## 関連項目 {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
