---
description: プレフィックスリクエスト修飾子文字列。 なしまたはそれ以上の画像サービングコマンドを「&」文字で区切って指定します。
solution: Experience Manager
title: 修飾子
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 6eef3159-c082-469b-b9dc-29acb28560d6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 7%

---

# 修飾子{#modifier}

プレフィックスリクエスト修飾子文字列。 なしまたはそれ以上の画像サービングコマンドを「&amp;」文字で区切って指定します。

画像を永続的に変更し、テンプレートの本文を保存するために使用します。

このフィールドのコマンドは、このレコードが参照されるリクエストまたはテンプレート内の同じコマンドと`catalog::PostModifier`内のコマンドによって上書きされます。

マクロは、同じカタログまたはデフォルトのカタログで定義されている限り、`catalog::Modifier`で許可されます。 カスタム変数も使用できます。

## プロパティ {#section-6674388f77d644469371a17e8809c45f}

テキスト文字列。 （オプション）

## 初期設定 {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

なし

## 関連項目 {#section-7a67803d141b442180c418c1f3cff029}

[catalog::PostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
