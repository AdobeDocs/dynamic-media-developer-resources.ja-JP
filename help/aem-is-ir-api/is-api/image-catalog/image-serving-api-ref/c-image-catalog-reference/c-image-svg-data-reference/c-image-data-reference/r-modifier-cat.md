---
description: プリフィックス要求修飾子文字列 「&」文字で区切られた1つ以上の画像サービングコマンド。
seo-description: プリフィックス要求修飾子文字列 「&」文字で区切られた1つ以上の画像サービングコマンド。
seo-title: 修飾子
solution: Experience Manager
title: 修飾子
topic: Scene7 Image Serving - Image Rendering API
uuid: eb17d115-22ec-4b1b-9039-9bd2bc256f48
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 7%

---


# 修飾子{#modifier}

プリフィックス要求修飾子文字列 「&amp;」文字で区切られた1つ以上の画像サービングコマンド。

画像を永続的に変更し、テンプレートの本文を保存するために使用します。

このフィールドのコマンドは、このレコードが参照されるリクエストまたはテンプレート内の同じコマンドと、`catalog::PostModifier`内のコマンドによって上書きされます

マクロは、同じカタログまたは初期設定のカタログで定義されている限り、`catalog::Modifier`で許可されます。 カスタム変数も使用できます。

## プロパティ {#section-6674388f77d644469371a17e8809c45f}

テキスト文字列。 （オプション）

## 初期設定 {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

なし

## 関連項目 {#section-7a67803d141b442180c418c1f3cff029}

[catalog::PostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
