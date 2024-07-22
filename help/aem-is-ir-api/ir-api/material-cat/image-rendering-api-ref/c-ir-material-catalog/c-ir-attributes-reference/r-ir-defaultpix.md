---
title: DefaultPix
description: デフォルトのレンダリング画像サイズ。 リクエストで wid=または hei=を使用して表示サイズが明示的に指定されていない場合、サーバーによって、返信画像がこの幅と高さを超えないように制限されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d60f2b8c-5213-42ad-8ec9-7e7797d74e09
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# DefaultPix{#defaultpix}

デフォルトのレンダリング画像サイズ。 リクエストで wid=または hei=を使用して表示サイズが明示的に指定されていない場合、サーバーによって、返信画像がこの幅と高さを超えないように制限されます。

## プロパティ {#section-9dc5474fc75842308796ab6440b29611}

コンマで区切られた 0 以上の 2 つの整数。 幅と高さ（ピクセル単位）。 一方または両方の値を 0 に設定すると、制限なしにすることができます。

ネストされたリクエストまたは埋め込まれたリクエストには適用されません。

## 初期設定 {#section-1935781c561e4679aa87a5bcced8df90}

定義されていない場合または空の場合は `default::DefaultPix` から継承します。

## 関連項目 {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
