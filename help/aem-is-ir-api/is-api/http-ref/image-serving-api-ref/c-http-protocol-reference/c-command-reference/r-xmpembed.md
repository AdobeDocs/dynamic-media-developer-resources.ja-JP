---
title: xmpEmbed
description: XMPメタデータを埋め込みます。 XMPメタデータを応答画像に含めるかどうかを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 353b6ac4-1141-4f17-a3ad-ad48b321b36f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# xmpEmbed{#xmpembed}

XMPメタデータを埋め込みます。 XMPメタデータを応答画像に含めるかどうかを指定します。

`xmpEmbed=0|1`

>[!NOTE]
>
>XMPのデータは、変更されずにソース画像から応答画像に渡されます。 その結果、誤ったデータが応答画像に埋め込まれる可能性があります。

## プロパティ {#section-27024c4272f44d9a8c264a0629193af2}

要求属性。 ソース画像にXMPデータが含まれていない場合は無視されます。 のソース画像からのXMPデータのみ `layer=0` 処理されます。 他のレイヤー画像からのXMPデータは無視されます。

出力画像形式がXMPの埋め込みをサポートしていない場合は無視されます。 詳しくは、 `fmt=` XMPの埋め込みをサポートする出力画像形式のリストを参照してください。

## 初期設定 {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`（出力画像にパスを埋め込まない場合）

## 関連項目 {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
