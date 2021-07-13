---
description: デフォルトのレンダリングイメージサイズ。 サーバーによって、要求でwid=またはhei=を使用してビューサイズが明示的に指定されていない場合、返信画像はこの幅と高さ以下に制限されます。
solution: Experience Manager
title: DefaultPix
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: d60f2b8c-5213-42ad-8ec9-7e7797d74e09
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---

# DefaultPix{#defaultpix}

デフォルトのレンダリングイメージサイズ。 サーバーによって、要求でwid=またはhei=を使用してビューサイズが明示的に指定されていない場合、返信画像はこの幅と高さ以下に制限されます。

## プロパティ {#section-9dc5474fc75842308796ab6440b29611}

0以上の2つの整数で、コンマで区切ります。 幅と高さ（ピクセル単位）。 値を0に設定すると、値は制約なしに保たれます。

ネストされた/埋め込みリクエストには適用できません。

## 初期設定 {#section-1935781c561e4679aa87a5bcced8df90}

`default::DefaultPix`から継承されます（定義されていない場合または空の場合）。

## 関連項目 {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
