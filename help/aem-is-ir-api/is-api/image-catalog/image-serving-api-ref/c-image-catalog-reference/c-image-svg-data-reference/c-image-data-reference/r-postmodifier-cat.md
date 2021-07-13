---
description: ポストフィックスリクエスト修飾子文字列 なしまたはそれ以上の画像サービングコマンドを「&」文字で区切って指定します。
solution: Experience Manager
title: PostModifier
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 7d6c9408-1f09-464d-8a69-eabdf7c0117d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 4%

---

# PostModifier{#postmodifier}

ポストフィックスリクエスト修飾子文字列 なしまたはそれ以上の画像サービングコマンドを「&amp;」文字で区切って指定します。

このフィールドのコマンドは、常にHTTPリクエスト内および`catalog::Modifier`内のコマンドを上書きします。

`catalog::PostModifier` は、特定の画像で、通常はURLから制御される特別な設定（やなど）が必要な場合に `qlt=` 役立ちま `resmode=`す。`catalog::Modifier` は、画像カタログ内のほとんどのISコマンドを設定するために使用する必要があります。

マクロは、同じカタログまたはデフォルトのカタログで定義されている限り、`catalog::PostModifier`で許可されます。 カスタム変数も使用できます。

>[!NOTE]
>
>リクエストに複数のレイヤーが含まれる場合、レイヤー0の`catalog::PostModifier`の内容のみが適用されます。 `catalog::PostModifier` その他のすべてのレイヤは無視されます。

## プロパティ {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

テキスト文字列。 （オプション）

## 初期設定 {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

なし

## 関連項目 {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
