---
title: DefaultPix
description: 初期設定のレンダリング画像サイズ。 要求で wid=または hei=を使用して表示サイズが明示的に指定されていない場合、サーバーは返信画像がこの幅と高さ以下になるように制限します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d60f2b8c-5213-42ad-8ec9-7e7797d74e09
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 3%

---

# DefaultPix{#defaultpix}

初期設定のレンダリング画像サイズ。 要求で wid=または hei=を使用して表示サイズが明示的に指定されていない場合、サーバーは返信画像がこの幅と高さ以下になるように制限します。

## プロパティ {#section-9dc5474fc75842308796ab6440b29611}

0 以上の 2 つの整数で、コンマで区切ります。 幅と高さ（ピクセル単位）。 値を 0 に設定すると、制約なしの状態を維持できます。

ネストされたリクエストや埋め込みリクエストには適用できません。

## 初期設定 {#section-1935781c561e4679aa87a5bcced8df90}

継承元 `default::DefaultPix` が定義されていない場合、または空の場合は。

## 関連項目 {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
