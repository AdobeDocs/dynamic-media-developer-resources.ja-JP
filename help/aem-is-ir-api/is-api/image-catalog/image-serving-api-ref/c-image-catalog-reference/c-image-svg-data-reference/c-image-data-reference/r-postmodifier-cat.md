---
description: 接尾辞リクエスト修飾子の文字列。 「&」文字で区切られた画像サービングコマンドがない、または複数の画像サービングコマンドがない。
solution: Experience Manager
title: PostModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d6c9408-1f09-464d-8a69-eabdf7c0117d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---

# PostModifier{#postmodifier}

接尾辞リクエスト修飾子の文字列。 「&amp;」文字で区切られた画像サービングコマンドがない、または複数の画像サービングコマンドがない。

このフィールドのコマンドは、常に HTTP リクエストおよび `catalog::Modifier` のコマンドを上書きします。

`catalog::PostModifier` は、特定の画像が、通常は URL から制御される特別な設定（`qlt=` や `resmode=` など）を必要とする場合に役立ちます。 `catalog::Modifier` は、画像カタログ内のほとんどの IS コマンドの設定に使用します。

マクロは、同じカタログまたはデフォルトのカタログで定義されている限り、`catalog::PostModifier` で使用できます。 カスタム変数も使用できます。

>[!NOTE]
>
>リクエストに複数のレイヤーが含まれる場合は、レイヤー 0 の `catalog::PostModifier` のコンテンツのみが適用されます。 他のすべてのレイヤーの `catalog::PostModifier` は無視されます。

## プロパティ {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

テキスト文字列 オプション。

## 初期設定 {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

なし

## 関連項目 {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[カタログ：：モディファイヤ](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
