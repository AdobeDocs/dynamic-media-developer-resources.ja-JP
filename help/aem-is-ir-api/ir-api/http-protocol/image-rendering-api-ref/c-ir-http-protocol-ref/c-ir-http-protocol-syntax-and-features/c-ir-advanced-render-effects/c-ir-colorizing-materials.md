---
description: ほとんどのマテリアルは動的にカラー付けできます。
solution: Experience Manager
title: 素材の色彩の統一
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# 材料に色を付ける{#colorizing-materials}

ほとんどのマテリアルは動的にカラー付けできます。

色彩化アルゴリズムは非常に単純で、色相の範囲が限られた素材画像に最適です。 マテリアルに色を付けるには、レンダラーは単に`bgc=`値を減算し、`color=`値を各ピクセル値に加算します。

`color=`が指定されていない場合、色彩の統一は無効になります。 `bgc=` は、キャビネットのマテリアルには無視されます。代わりに、 [!DNL vnc] ファイルに埋め込まれたベースカラーの値が使用されます。
