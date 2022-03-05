---
description: req=tmb 要求に応じてクライアントに返される画像は、次の値 wid=、hei=、attribute DefaultThumbPix および attribute MaxPix を考慮して、複合画像から派生されます。
solution: Experience Manager
title: サムネールの変換を表示
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# サムネールの変換を表示{#view-transform-for-thumbnails}

req=tmb 要求に応じてクライアントに返される画像は、次の値を考慮して、複合画像から派生します。wid=、hei=、attribute::DefaultThumbPix および attribute::MaxPix。

1. **表示方向を計算する**  — 用途 `wid=` または幅の値 `attribute::DefaultThumbPix` は、ビューの直角の幅です。 用途 `hei=` またはの高さの値 `attribute::DefaultThumbPix` 高さに対して この手順では、ビューの正しい指定を完全に行う必要があります。 ( ビューの直角は、レイヤ 0 の直角と同じです。 `size=`は、レイヤ 0 に対して指定されます )。
1. **コンポジットをスケール** - If `catalog::ThumbType=Crop`を指定した場合、合成画像は、ビュー全体を埋めながら、可能な限り小さい画像に合わせて拡大縮小されます。余分な画像データが切り抜かれます。 If `catalog::ThumbType= Fit`を指定した場合、合成画像全体がビューレクトにフィッティングされた状態で、可能な限り大きな画像に合わせて拡大縮小されます。 If `catalog::ThumbType=Texture`を指定した場合、コンポジットは、で指定した解像度を維持するために、全く拡大・縮小されません。 `catalog::ThumbRes`.
1. **塗りつぶしと切り抜き**  — ビューの直接値は `bgc=` 色（指定されていない場合はで） `attribute::ThumbBkgColor`) をクリックします。 次の属性を使用して、尺度が設定された合成は、ビューの直接位置に合わせられます。 `ThumbHorizAlign` および属性： `ThumbVertAlign`. 次に、拡大・縮小された合成は、拡大・縮小せずに、塗り潰されたビューの直接と結合されます。 合成のビューの直線を越えた領域は切り抜かれます。
