---
description: XMPメタデータを埋め込む。 応答画像にXMPメタデータを含めるかどうかを指定します。
solution: Experience Manager
title: xmpEmbed
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 353b6ac4-1141-4f17-a3ad-ad48b321b36f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---

# xmpEmbed{#xmpembed}

XMPメタデータを埋め込む。 応答画像にXMPメタデータを含めるかどうかを指定します。

`xmpEmbed=0|1`

>[!NOTE]
>
>XMPのデータは、ソース画像から応答画像に変更されずに渡されます。 その結果、誤ったデータが応答画像に埋め込まれる可能性があります。

## プロパティ {#section-27024c4272f44d9a8c264a0629193af2}

リクエスト属性。 ソース画像にXMPデータが含まれていない場合は無視されます。 `layer=0`のソース画像からのXMPデータのみが処理されます。 他のレイヤー画像のXMPデータは無視されます。

出力画像形式がXMPの埋め込みをサポートしていない場合は無視されます。 XMPの埋め込みをサポートする出力画像形式のリストについては、 `fmt=`の説明を参照してください。

## 初期設定 {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`（出力画像にパスを埋め込まない場合）。

## 関連項目 {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
