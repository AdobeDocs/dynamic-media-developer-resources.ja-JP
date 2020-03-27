---
description: XMPメタデータを埋め込みます。 XMPメタデータを応答画像に含めるかどうかを指定します。
seo-description: XMPメタデータを埋め込みます。 XMPメタデータを応答画像に含めるかどうかを指定します。
seo-title: xmpEmbed
solution: Experience Manager
title: xmpEmbed
topic: Scene7 Image Serving - Image Rendering API
uuid: c0dfd0e5-16d1-4a6e-957a-ecc276b9361a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# xmpEmbed{#xmpembed}

XMPメタデータを埋め込みます。 XMPメタデータを応答画像に含めるかどうかを指定します。

`xmpEmbed=0|1`

>[!NOTE]
>
>XMPデータは、ソース画像から応答画像に変更なしで渡されます。 これにより、応答画像に誤ったデータが埋め込まれる可能性があります。

## プロパティ {#section-27024c4272f44d9a8c264a0629193af2}

リクエスト属性。 ソース画像にXMPデータが含まれていない場合は無視されます。 のソース画像のXMPデータのみが処理 `layer=0` されます。 他のレイヤー画像のXMPデータは無視されます。

出力画像形式がXMP埋め込みをサポートしていない場合は無視されます。 XMP埋め込みをサポート `fmt=` する出力画像形式のリストについては、の説明を参照してください。

## 初期設定 {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`を指定します。出力画像にパスを埋め込むことはありません。

## 関連項目 {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
