---
description: req=tmb要求に応じてクライアントに返される画像は、次の値wid=、hei=、attribute DefaultThumbPixおよびattribute MaxPixを考慮して合成画像から得られます。
solution: Experience Manager
title: サムネールの変換の表示
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# サムネールの変換の表示{#view-transform-for-thumbnails}

req=tmb要求に応じてクライアントに返される画像は、次の値を考慮して、合成画像から派生します。wid=、hei=、attribute::DefaultThumbPixおよびattribute::MaxPix。

1. **ビューの直角を計算**  — ビ `wid=` ューの直角の幅に `attribute::DefaultThumbPix` は、またはの幅の値を使用します。高さには`hei=`または`attribute::DefaultThumbPix`の高さ値を使用します。 この手順では、表示方向を完全に指定する必要があります。 （レイヤ0に`size=`を指定しない場合、ビューの直角はレイヤ0の直角と同じになります）。
1. **合成を拡大/縮小**  -  `catalog::ThumbType=Crop`の場合、合成は可能な限り小さい画像に拡大/縮小され、ビュー全体を塗りつぶします。余分な画像データが切り抜かれます。`catalog::ThumbType= Fit`の場合、コンポジット全体をビューの直線に合わせながら、可能な限り大きいイメージに合わせてコンポジットが拡大縮小されます。 `catalog::ThumbType=Texture`の場合、`catalog::ThumbRes`で指定された解像度を維持するために、コンポジットは全く拡大/縮小されません。
1. **塗りつぶしと切り抜き**  — ビューの直角が色で塗りつぶさ `bgc=` れます(指定しない場合は `attribute::ThumbBkgColor`)。次の属性を使用して、拡大/縮小された合成はビューの直接位置に合わせられます。`ThumbHorizAlign`と属性：:`ThumbVertAlign`. 次に、拡大/縮小された合成は、拡大/縮小を行わずに、塗り潰されたビューの直角と結合されます。 合成の、表示領域を越えた領域は切り抜かれます。
