---
description: Postfixリクエスト修飾子文字列 「&」文字で区切られた1つ以上の画像サービングコマンド。
seo-description: Postfixリクエスト修飾子文字列 「&」文字で区切られた1つ以上の画像サービングコマンド。
seo-title: PostModifier
solution: Experience Manager
title: PostModifier
topic: Scene7 Image Serving - Image Rendering API
uuid: 8800a9b2-e9c0-498b-b4e1-37952ba7c842
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 4%

---


# PostModifier{#postmodifier}

Postfixリクエスト修飾子文字列 「&amp;」文字で区切られた1つ以上の画像サービングコマンド。

このフィールドのコマンドは、HTTPリクエストおよび`catalog::Modifier`内のコマンドを常に上書きします。

`catalog::PostModifier` は、特定の画像が、 `qlt=` やなど、通常URLから制御される特別な設定を必要とする場合に役立ち `resmode=`ます。`catalog::Modifier` は、画像カタログのほとんどのISコマンドを設定するために使用します。

マクロは、同じカタログまたは初期設定のカタログで定義されている限り、`catalog::PostModifier`で許可されます。 カスタム変数も使用できます。

>[!NOTE]
>
>要求に複数のレイヤーが含まれる場合は、レイヤー0の`catalog::PostModifier`の内容だけが適用されます。 `catalog::PostModifier` の値以外は無視されます。

## プロパティ {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

テキスト文字列。 （オプション）

## 初期設定 {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

なし

## 関連項目 {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
