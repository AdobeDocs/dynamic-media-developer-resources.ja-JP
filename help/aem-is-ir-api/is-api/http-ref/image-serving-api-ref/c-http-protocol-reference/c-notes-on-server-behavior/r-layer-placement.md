---
description: レイヤーの位置は、レイヤーの原点(origin=)を背景レイヤーの原点と、pos=で指定されたオフセットで揃えることで決まります。
seo-description: レイヤーの位置は、レイヤーの原点(origin=)を背景レイヤーの原点と、pos=で指定されたオフセットで揃えることで決まります。
seo-title: レイヤーの配置
solution: Experience Manager
title: レイヤーの配置
topic: Scene7 Image Serving - Image Rendering API
uuid: d9d778f2-13dd-4ea1-a703-52eac70bb3d8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# レイヤーの配置{#layer-placement}

レイヤーの位置は、レイヤーの原点(origin=)を背景レイヤーの原点と、pos=で指定されたオフセットで揃えることで決まります。

イメージレイヤに対してレイヤの原点が明示的に指定されていない場合、次のように計算されます。

1. 画像アンカーを決定します。 またはを `anchor=`使用します（指定しなかった場合） `catalog::Anchor`。
1. 画像アンカーが定義されている場合は、レイヤー変換を適用 `extend=` し、origin=値に変換します。
1. 画像アンカーが定義されていない場合、レイヤーの原点は、レイヤーの長方形の中央（適用後）に配置され `extend=`ます。

![](assets/layerplacement.png)

