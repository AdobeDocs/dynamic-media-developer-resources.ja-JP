---
description: req=tmb リクエストに応答してクライアントに返される画像は、次の値wid=、hei=、属性DefaultThumbPix、属性MaxPixを考慮して、合成画像から派生されます。
solution: Experience Manager
title: サムネールの変形を表示
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7db6736f-0b49-4c4f-89c5-e89d4752f339
TQID: 'https://experienceleague.adobe.com/yx1jgWnx-cwMDmBY2NOzYEyEjCqehPqGBK31MvGo-4o'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 245
ht-degree: 0%

---

# サムネールの変形を表示{#view-transform-for-thumbnails}

req=tmb リクエストに応答してクライアントに返される画像は、次の値を考慮して、複合画像から派生します。wid=、hei=、attribute::DefaultThumbPix、attribute::MaxPix。

1. **ビューrect**&#x200B;を計算 – ビューrectの幅に`wid=`または`attribute::DefaultThumbPix`の幅の値を使用します。 高さには、`hei=`または`attribute::DefaultThumbPix`の高さ値を使用してください。 この手順では、ビューの直帰率を完全に指定する必要があります。 （レイヤー0に`size=`が指定されていない場合、ビューrectはレイヤー0rectと同じです）。
1. **コンポジットの拡大・縮小** - `catalog::ThumbType=Crop`の場合、コンポジットは全体の直近画像を埋めながら、可能な限り小さな画像に拡大・縮小されます。追加の画像データは切り抜かれます。 `catalog::ThumbType= Fit`の場合、コンポジット全体をビューの矩形に合わせながら、コンポジットを可能な限り大きな画像に拡大・縮小します。 `catalog::ThumbType=Texture`の場合、`catalog::ThumbRes`で指定した解像度を維持するために、コンポジットは全く拡大・縮小されません。
1. **塗りつぶしと切り抜き** - ビューの矩形は`bgc=`色で塗りつぶされます（指定されていない場合は`attribute::ThumbBkgColor`で塗りつぶされます）。 スケールされた合成は、属性：`ThumbHorizAlign`および属性：`ThumbVertAlign`を使用してビューの直腸と整列しています。 次に、拡大・縮小されたコンポジットは、拡大・縮小を加えることなく、塗りつぶされたビューの直列と結合されます。 ビュー直方体を超えて広がるコンポジットの領域は、切り抜かれます。
