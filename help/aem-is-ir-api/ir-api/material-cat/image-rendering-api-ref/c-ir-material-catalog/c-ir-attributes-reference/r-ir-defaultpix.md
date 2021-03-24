---
description: 初期設定のレンダリングイメージサイズ リクエストでwid=またはhei=を使用して明示的に表示サイズが指定されていない場合、応答画像はこの幅と高さ以下に制限されます。
solution: Experience Manager
title: DefaultPix
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 3%

---


# DefaultPix{#defaultpix}

初期設定のレンダリングイメージサイズ リクエストでwid=またはhei=を使用して明示的に表示サイズが指定されていない場合、応答画像はこの幅と高さ以下に制限されます。

## プロパティ {#section-9dc5474fc75842308796ab6440b29611}

0以上の2つの整数で、カンマで区切ります。 幅と高さ（ピクセル単位） どちらかまたは両方の値を0に設定して、拘束を適用しないようにすることができます。

ネストされた/埋め込まれたリクエストには適用されません。

## 初期設定 {#section-1935781c561e4679aa87a5bcced8df90}

定義されていない場合や空の場合は`default::DefaultPix`から継承されます。

## 関連項目 {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
