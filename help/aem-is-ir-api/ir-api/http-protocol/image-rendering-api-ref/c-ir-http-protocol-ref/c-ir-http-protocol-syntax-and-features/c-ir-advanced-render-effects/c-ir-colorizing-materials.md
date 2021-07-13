---
description: ほとんどのマテリアルは動的にカラー化できます。
solution: Experience Manager
title: 材料の色付け
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# 材料の色付け{#colorizing-materials}

ほとんどのマテリアルは動的にカラー化できます。

カラー化アルゴリズムは非常に単純で、色合い範囲が限られた素材画像に最適です。 マテリアルに色を付けるには、レンダラーは単に`bgc=`値を引き、各ピクセル値に`color=`値を追加します。

`color=`が指定されていない場合、色付けは無効になります。 `bgc=` は、キャビネットマテリアルでは無視されます。代わりに、ファイルに埋め込まれ [!DNL vnc] た基本色の値が使用されます。
