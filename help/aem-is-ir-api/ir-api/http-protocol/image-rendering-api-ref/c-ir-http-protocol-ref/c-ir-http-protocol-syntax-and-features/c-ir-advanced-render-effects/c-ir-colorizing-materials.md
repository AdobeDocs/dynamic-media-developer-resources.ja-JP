---
title: 材料の着色
description: ほとんどのマテリアルは動的にカラー化できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# 材料の着色{#colorizing-materials}

ほとんどのマテリアルは動的にカラー化できます。

色付けアルゴリズムは単純で、色相範囲が限られたマテリアル イメージに最適です。 マテリアルに色を付けるには、レンダラーは単に `bgc=` 値を減算し、`color=` 値を各ピクセル値に加算します。

`color=` が指定されていない場合、色付けは無効になります。 キャビネット マテリアルでは `bgc=` 属性は無視されます。代わりに、[!DNL vnc] ファイルに埋め込まれた基本色の値が使用されます。
