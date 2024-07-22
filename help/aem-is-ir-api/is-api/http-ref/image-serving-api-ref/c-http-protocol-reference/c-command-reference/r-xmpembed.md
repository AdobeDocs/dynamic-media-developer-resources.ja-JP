---
title: xmpEmbed
description: XMP メタデータを埋め込みます。 XMP メタデータをレスポンス画像に含めるかどうかを指定します。
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

XMP メタデータを埋め込みます。 XMP メタデータをレスポンス画像に含めるかどうかを指定します。

`xmpEmbed=0|1`

>[!NOTE]
>
>XMP データは、ソース画像から応答画像に変更なしで渡されます。 これにより、誤ったデータが応答画像に埋め込まれる可能性があります。

## プロパティ {#section-27024c4272f44d9a8c264a0629193af2}

リクエスト属性。 ソース画像にXMP データが含まれていない場合は無視されます。 `layer=0` のソース画像のXMP データのみが処理されます。 他のレイヤー画像のXMP データは無視されます。

出力画像フォーマットがXMPの埋め込みをサポートしていない場合は無視されます。 XMPの埋め込みをサポートする出力画像フォーマットのリストについては、`fmt=` の説明を参照してください。

## 初期設定 {#section-aedbedd04d664ba184b2cfe35644b960}

出力画像にパスを埋め込まない場合は `xmpEmbed=0` です。

## 関連項目 {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
