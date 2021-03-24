---
description: XMPメタデータを埋め込みます。 XMPメタデータを応答画像に含めるかどうかを指定します。
solution: Experience Manager
title: xmpEmbed
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 2%

---


# xmpEmbed{#xmpembed}

XMPメタデータを埋め込みます。 XMPメタデータを応答画像に含めるかどうかを指定します。

`xmpEmbed=0|1`

>[!NOTE]
>
>XMPデータは、ソース画像から応答画像に変更なしで渡されます。 これにより、応答画像に誤ったデータが埋め込まれる可能性があります。

## プロパティ {#section-27024c4272f44d9a8c264a0629193af2}

要求属性。 ソース画像にXMPデータが含まれていない場合は無視されます。 `layer=0`のソース画像からのXMPデータのみが処理されます。 他のレイヤー画像のXMPデータは無視されます。

出力画像形式がXMP埋め込みをサポートしていない場合は無視されます。 XMPの埋め込みをサポートする出力画像形式のリストについては、`fmt=`の説明を参照してください。

## 初期設定 {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`を使用します。出力画像にパスを埋め込む必要はありません。

## 関連項目 {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
