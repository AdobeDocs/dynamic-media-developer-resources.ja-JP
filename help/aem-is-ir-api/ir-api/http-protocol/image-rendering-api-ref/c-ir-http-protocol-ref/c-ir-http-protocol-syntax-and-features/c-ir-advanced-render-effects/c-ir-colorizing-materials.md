---
description: ほとんどのマテリアルは動的にカラー付けできます。
seo-description: ほとんどのマテリアルは動的にカラー付けできます。
seo-title: 素材の色彩の統一
solution: Experience Manager
title: 素材の色彩の統一
topic: Scene7 Image Serving - Image Rendering API
uuid: 3f5a9089-6e35-446c-89f9-71b067e0d1df
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# 材料に色を付ける{#colorizing-materials}

ほとんどのマテリアルは動的にカラー付けできます。

色彩化アルゴリズムは非常に単純で、色相の範囲が限られた素材画像に最適です。 マテリアルに色を付けるには、レンダラーは単に`bgc=`値を減算し、`color=`値を各ピクセル値に加算します。

`color=`が指定されていない場合、色彩の統一は無効になります。 `bgc=` は、キャビネットのマテリアルには無視されます。代わりに、 [!DNL vnc] ファイルに埋め込まれたベースカラーの値が使用されます。
