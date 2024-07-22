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

レイヤーは、レイヤーの原点（origin=）を背景レイヤーの原点の pos=で指定されたオフセットに揃えることで配置されます。

イメージレイヤに対してレイヤの原点が明示的に指定されていない場合は、次のように計算されます。

1. 画像アンカーを決定します。 `anchor=` を使用するか、指定しない場合は `catalog::Anchor` を使用します。
1. 画像アンカーが定義されている場合は、レイヤーの変換と `extend=` を適用して、原点=値に変換します。
1. イメージアンカーが定義されていない場合、レイヤーの原点はレイヤーの長方形の中央に配置されます（`extend=` の適用後）。

![ レイヤーの配置画像 ](assets/layerplacement.png)
