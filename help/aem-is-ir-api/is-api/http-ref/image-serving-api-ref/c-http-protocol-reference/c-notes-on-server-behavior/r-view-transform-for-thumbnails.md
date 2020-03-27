---
description: req=tmb要求に応じてクライアントに返される画像は、次の値wid=、hei=、attribute DefaultThumbPix、およびattribute MaxPixを考慮して、合成画像から得られます。
seo-description: req=tmb要求に応じてクライアントに返される画像は、次の値wid=、hei=、attribute DefaultThumbPix、およびattribute MaxPixを考慮して、合成画像から得られます。
seo-title: サムネールの変換の表示
solution: Experience Manager
title: サムネールの変換の表示
topic: Scene7 Image Serving - Image Rendering API
uuid: 29924bc1-ada1-420f-aef7-bf9a7db7065b
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b

---


# サムネールの変換の表示{#view-transform-for-thumbnails}

req=tmb要求に応じてクライアントに返される画像は、次の値を考慮して、合成画像から得られます。wid=、hei=、attribute::DefaultThumbPix、attribute::MaxPix。

1. **ビューrect** — ビューレク `wid=` トの幅に対して、ま `attribute::DefaultThumbPix` たはの幅の値を使用します。 高さに `hei=` は、またはの高さの値 `attribute::DefaultThumbPix` を使用します。 この手順では、ビューレクトを完全に指定する必要があります。 (レイヤー0に対して何も指定されていない場合、ビューレクトはレイヤー0 `size=`rectと同じになります)。
1. **合成の拡大・縮小** - `catalog::ThumbType=Crop`合成は、ビュー領域全体を埋めながら、可能な限り小さい画像に拡大・縮小されます。余分な画像データが切り抜かれる。 この場 `catalog::ThumbType= Fit`合、合成画像は可能な限り大きい画像に合わせて拡大され、合成画像全体がビューレクトに合わせられます。 の場合 `catalog::ThumbType=Texture`、で指定した解像度を維持するために、コンポジットは全く拡大縮小されませ `catalog::ThumbRes`ん。
1. **塗りつぶしと切り抜き** — ビューの長方形が色で塗りつぶさ `bgc=` れます(指定しなかった場合は、色で塗りつぶされ `attribute::ThumbBkgColor`ます)。 次の属性を使用して、拡大/縮小された合成画像をビューレクトと位置合わせします。 `ThumbHorizAlign` と属性： `ThumbVertAlign`. 次に、拡大/縮小された合成画像が、それ以上拡大/縮小されることなく、塗りつぶされたビューレクトと結合されます。 合成画像のビュー領域を越える領域は、すべて切り抜かれます。

