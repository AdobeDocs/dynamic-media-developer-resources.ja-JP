---
description: Postfix リクエスト修飾子文字列。 「&」文字で区切られた画像サービングコマンドはありません。
solution: Experience Manager
title: PostModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d6c9408-1f09-464d-8a69-eabdf7c0117d
TQID: 'https://experienceleague.adobe.com/hPHoHlBkRN-eXFvLzZ2LpWhmtiT4lGyehTvwFw9ItJo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 128
ht-degree: 3%

---

# PostModifier{#postmodifier}

Postfix リクエスト修飾子文字列。 「&amp;」文字で区切られた画像サービングコマンドはありません。

このフィールドのコマンドは、常にHTTP リクエストおよび`catalog::Modifier`のコマンドを上書きします。

`catalog::PostModifier`は、特定の画像で、通常URLから制御される特別な設定（`qlt=`や`resmode=`など）が必要な場合に便利です。 `catalog::Modifier`は、画像カタログのほとんどのIS コマンドの設定に使用する必要があります。

マクロは、同じカタログまたはデフォルトのカタログで定義されている限り、`catalog::PostModifier`で許可されます。 カスタム変数も使用できます。

>[!NOTE]
>
>リクエストに複数のレイヤーが含まれる場合、レイヤー0の`catalog::PostModifier`のコンテンツのみが適用されます。 他のすべてのレイヤーの`catalog::PostModifier`は無視されます。

## プロパティ {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

テキスト文字列。 オプション。

## 初期設定 {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

なし

## 関連項目 {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catalog::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
