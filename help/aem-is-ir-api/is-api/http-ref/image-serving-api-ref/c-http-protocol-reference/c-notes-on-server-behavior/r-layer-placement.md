---
title: レイヤーの配置
escription: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# レイヤーの配置{#layer-placement}

レイヤーの位置は、レイヤーの原点 (origin=) と背景のレイヤーの原点を、pos=で指定されたオフセットで揃えることで決まります。

画像レイヤーに対してレイヤーの原点が明示的に指定されていない場合は、次のように計算されます。

1. 画像アンカーを決定します。 `anchor=` を使用するか、指定しない場合は `catalog::Anchor` を使用します。
1. 画像アンカーが定義されている場合は、レイヤー変換を適用し、 `extend=` を origin=値に変換します。
1. イメージアンカーが定義されていない場合、レイヤーの原点は、（`extend=` を適用した後の）レイヤーの長方形の中心に配置されます。

![レイヤー配置画像](assets/layerplacement.png)
