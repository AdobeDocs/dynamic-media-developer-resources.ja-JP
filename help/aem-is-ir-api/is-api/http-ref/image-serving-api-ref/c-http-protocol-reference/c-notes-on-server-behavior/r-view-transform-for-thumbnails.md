---
description: req=tmb 要求に応答してクライアントに返される画像は、次の値 wid=、hei=、attribute DefaultThumbPix、attribute MaxPix を考慮して、合成画像から得られます。
solution: Experience Manager
title: サムネールの表示変換
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# サムネールの表示変換{#view-transform-for-thumbnails}

req=tmb 要求に応答してクライアントに返される画像は、次の値を考慮して合成画像から取得されます。wid=、hei=、attribute::DefaultThumbPix、attribute::MaxPix。

1. **ビューの rect を計算** - ビューの rect の幅に、`wid=` または `attribute::DefaultThumbPix` の幅の値を使用します。 高さには、`hei=` または高さの値 `attribute::DefaultThumbPix` を使用します。 この手順では、ビューレコードを完全に指定する必要があります。 （ビューの rect はレイヤ 0 の rect と同じです。レイヤ 0 に `size=` が指定されていない場合）。
1. **合成を拡大・縮小** -`catalog::ThumbType=Crop` の場合、合成はビューの長方形を埋めつつ、可能な限り小さい画像に縮小されます。追加の画像データは切り抜かれます。 `catalog::ThumbType= Fit` の場合、合成は、合成全体をビューの長方形に合わせたまま、可能な限り最大の画像にスケーリングされます。 `catalog::ThumbType=Texture` の場合、`catalog::ThumbRes` で指定した解像度を保持するために、合成のサイズはまったく変更されません。
1. **塗りつぶしと切り抜き** - ビューの長方形は `bgc=` の色（または指定しない場合は `attribute::ThumbBkgColor`）で塗りつぶされます。 スケールされたコンポジットは、属性：: `ThumbHorizAlign` および属性：`ThumbVertAlign` を使用してビューの長方形に位置合わせされます。 拡大縮小された合成は、さらに拡大縮小することなく、塗り潰されたビューの長方形と結合されます。 コンポジットの中で、ビューの長方形を超えて広がる領域はすべて切り抜かれます。
