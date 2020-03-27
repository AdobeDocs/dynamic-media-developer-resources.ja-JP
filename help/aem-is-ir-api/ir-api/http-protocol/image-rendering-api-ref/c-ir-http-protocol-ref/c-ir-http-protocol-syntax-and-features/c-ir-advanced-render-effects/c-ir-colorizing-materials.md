---
description: ほとんどのマテリアルは動的に色付けできます。
seo-description: ほとんどのマテリアルは動的に色付けできます。
seo-title: 材料の色彩の統一
solution: Experience Manager
title: 材料の色彩の統一
topic: Scene7 Image Serving - Image Rendering API
uuid: 3f5a9089-6e35-446c-89f9-71b067e0d1df
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 材料の色彩の統一{#colorizing-materials}

ほとんどのマテリアルは動的に色付けできます。

色付けアルゴリズムは非常に単純で、色相の範囲が限られた素材画像に最適です。 マテリアルに色を付けるには、レンダラーは単に値を減 `bgc=` 算し、値を各ピクセ `color=` ル値に加算するだけです。

を指定しない場合、色付け `color=` は無効になります。 `bgc=` は、キャビネットのマテリアルでは無視されます。代わりに、ファイルに埋め込まれたベ [!DNL vnc] ースカラー値が使用されます。
