---
description: req=tmbリクエストに応じてクライアントに返される画像は、次の値wid=、hei=、attribute DefaultThumbPixおよびattribute MaxPixを考慮して、合成画像から得られます。
seo-description: req=tmbリクエストに応じてクライアントに返される画像は、次の値wid=、hei=、attribute DefaultThumbPixおよびattribute MaxPixを考慮して、合成画像から得られます。
seo-title: サムネールの表示変換
solution: Experience Manager
title: サムネールの表示変換
topic: Scene7 Image Serving - Image Rendering API
uuid: 29924bc1-ada1-420f-aef7-bf9a7db7065b
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---


# サムネールの表示変換{#view-transform-for-thumbnails}

req=tmb要求に応じてクライアントに返される画像は、次の値を考慮して、複合画像から得られます。wid=、hei=、attribute::DefaultThumbPix、およびattribute::MaxPix。

1. **表示rect** -表示rectの幅に対し `wid=` て使用または幅 `attribute::DefaultThumbPix` の値を使用します。高さには`hei=`または`attribute::DefaultThumbPix`の高さの値を使用します。 この手順では、表示rectを完全に指定する必要があります。 (レイヤー0に対して`size=`を指定しない場合、表示rectはレイヤー0のrectと同じになります)。
1. **合成画像の拡大縮小**  — この場合 `catalog::ThumbType=Crop`、合成画像は表示領域全体を埋めつつ、可能な限り小さい画像に拡大縮小されます。余分な画像データが切り抜かれる。`catalog::ThumbType= Fit`の場合、合成画像は可能な限り大きい表示に合わせて拡大縮小され、合成画像全体は画像rectに合わせて調整されます。 `catalog::ThumbType=Texture`の場合、`catalog::ThumbRes`で指定された解像度を維持するために、合成画像は全く拡大縮小されません。
1. **塗りと切り抜き** -表示rectは、 `bgc=` 色で塗りつぶされます(指定しない場合は、 `attribute::ThumbBkgColor`色)。拡大縮小された合成画像は、次の属性を使用して、表示rectと整列します。`ThumbHorizAlign`と属性：`ThumbVertAlign`. 次に、拡大/縮小された合成画像を、それ以上拡大/縮小することなく、塗りつぶされた表示rectと結合します。 合成画像の表示範囲を超える領域は、すべて切り抜かれます。

