---
title: 材料の色彩の統一
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

# 材料の色彩の統一{#colorizing-materials}

ほとんどのマテリアルは動的にカラー化できます。

色彩化アルゴリズムは単純で、色相範囲が限られた素材画像に最適です。 マテリアルに色を付けるには、レンダラーは単に `bgc=` の値を指定し、 `color=` の値を各ピクセル値に設定します。

次の場合、色付けは無効になります `color=` が指定されていません。 この `bgc=` 属性は、キャビネットのマテリアルでは無視されます。基本色の値が [!DNL vnc] ファイルが代わりに使用されます。
