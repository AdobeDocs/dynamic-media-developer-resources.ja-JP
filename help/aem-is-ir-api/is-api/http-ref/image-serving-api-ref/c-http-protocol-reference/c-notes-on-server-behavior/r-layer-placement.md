---
description: レイヤーの位置は、レイヤーの原点(origin=)と背景レイヤーの原点を、pos=で指定されたオフセットで揃えることで決まります。
solution: Experience Manager
title: レイヤーの配置
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---

# レイヤーの配置{#layer-placement}

レイヤーの位置は、レイヤーの原点(origin=)と背景レイヤーの原点を、pos=で指定されたオフセットで揃えることで決まります。

イメージレイヤに対してレイヤ原点が明示的に指定されていない場合、次のように計算されます。

1. 画像アンカーを決定します。 `anchor=`を使用するか、指定しない場合は`catalog::Anchor`を使用します。
1. イメージアンカーが定義されている場合は、レイヤー変換を適用し、 `extend=`をorigin=値に変換します。
1. イメージアンカーが定義されていない場合、レイヤーの原点はレイヤーの長方形の中央（`extend=`を適用した後）に配置されます。

![](assets/layerplacement.png)
