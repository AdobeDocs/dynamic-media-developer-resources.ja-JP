---
description: ポストフィックスリクエスト修飾子文字列 なしまたは複数の画像サービングコマンドを「&」文字で区切って指定します。
seo-description: ポストフィックスリクエスト修飾子文字列 なしまたは複数の画像サービングコマンドを「&」文字で区切って指定します。
seo-title: PostModifier
solution: Experience Manager
title: PostModifier
topic: Scene7 Image Serving - Image Rendering API
uuid: 8800a9b2-e9c0-498b-b4e1-37952ba7c842
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PostModifier{#postmodifier}

ポストフィックスリクエスト修飾子文字列 なしまたは複数の画像サービングコマンドを「&amp;」文字で区切って指定します。

このフィールドのコマンドは、HTTPリクエストおよびでのコマンドを常に上書きしま `catalog::Modifier`す。

`catalog::PostModifier` は、特定の画像が、通常はURLから制御される特別な設定（やなど）を必要とする場合に役 `qlt=` 立ちま `resmode=`す。 `catalog::Modifier` は、画像カタログ内のほとんどのISコマンドを設定するために使用します。

マクロは、同じカタ `catalog::PostModifier`ログまたはデフォルトのカタログで定義されている限り、で使用できます。 カスタム変数も使用できます。

>[!NOTE]
>
>リクエストに複数のレイヤーが含まれる場合は、レイヤー0の `catalog::PostModifier` コンテンツのみが適用されます。 `catalog::PostModifier` の値を含まないレイヤーは無視されます。

## プロパティ {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

テキスト文字列。 （オプション）

## 初期設定 {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

なし

## 関連項目 {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
