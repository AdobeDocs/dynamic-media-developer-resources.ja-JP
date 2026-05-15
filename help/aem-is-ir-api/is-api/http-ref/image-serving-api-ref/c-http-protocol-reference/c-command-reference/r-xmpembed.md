---
title: xmpEmbed
description: XMP メタデータを埋め込みます。 レスポンス画像にXMP メタデータを含めるかどうかを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 353b6ac4-1141-4f17-a3ad-ad48b321b36f
TQID: 'https://experienceleague.adobe.com/2pISbWU-Y-4szY0jmZswDIxvBrPlJ1yZmQby0sZ1v-o'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 2%

---

# xmpEmbed{#xmpembed}

XMP メタデータを埋め込みます。 レスポンス画像にXMP メタデータを含めるかどうかを指定します。

`xmpEmbed=0|1`

>[!NOTE]
>
>XMP データは、ソースイメージからレスポンス画像に変更なしで渡されます。 これにより、応答イメージに誤ったデータが埋め込まれる可能性があります。

## プロパティ {#section-27024c4272f44d9a8c264a0629193af2}

リクエスト属性： ソースイメージにXMP データが含まれていない場合は無視されます。 `layer=0`のソースイメージからのXMP データのみが処理されます。 他のレイヤー画像からのXMP データは無視されます。

出力イメージのフォーマットがXMPの埋め込みをサポートしていない場合は無視されます。 XMPの埋め込みをサポートする出力画像フォーマットの一覧については、`fmt=`の説明を参照してください。

## 初期設定 {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`。出力画像にパスを埋め込みません。

## 関連項目 {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
