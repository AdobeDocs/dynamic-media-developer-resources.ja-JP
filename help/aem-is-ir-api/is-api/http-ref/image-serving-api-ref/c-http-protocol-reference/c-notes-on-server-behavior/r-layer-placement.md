---
description: レイヤーは、レイヤー接触チャネル(接触チャネル=)と背景レイヤー接触チャネルを、pos=で指定したオフセットで整列して配置されます。
seo-description: レイヤーは、レイヤー接触チャネル(接触チャネル=)と背景レイヤー接触チャネルを、pos=で指定したオフセットで整列して配置されます。
seo-title: レイヤーの配置
solution: Experience Manager
title: レイヤーの配置
uuid: d9d778f2-13dd-4ea1-a703-52eac70bb3d8
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# レイヤーの配置{#layer-placement}

レイヤーは、レイヤー接触チャネル(接触チャネル=)と背景レイヤー接触チャネルを、pos=で指定したオフセットで整列して配置されます。

イメージレイヤに対してレイヤ接触チャネルを明示的に指定しない場合、次のように計算されます。

1. 画像アンカーを決定します。 `anchor=`を使用するか、指定しない場合は`catalog::Anchor`を使用します。
1. イメージアンカーを定義した場合は、レイヤ変換を適用し、`extend=`を実行して接触チャネル=値に変換します。
1. 画像アンカーが定義されていない場合、レイヤー接触チャネルは、（`extend=`を適用した後で）レイヤーの長方形の中央に配置されます。

![](assets/layerplacement.png)

