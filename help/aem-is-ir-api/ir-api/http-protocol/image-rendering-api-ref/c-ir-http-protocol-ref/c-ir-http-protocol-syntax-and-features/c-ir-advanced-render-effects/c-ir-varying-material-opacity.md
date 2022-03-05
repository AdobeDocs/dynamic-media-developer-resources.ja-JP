---
title: 変化するマテリアルの不透明度
description: 可変不透明度は、重なり合うオブジェクトに適用されるべた塗りや繰り返し可能なテクスチャ、デカールやウィンドウカバーのマテリアルに対してサポートされます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# 変化するマテリアルの不透明度{#varying-material-opacity}

可変不透明度は、重なり合うオブジェクトに適用されるべた塗りや繰り返し可能なテクスチャ、デカールやウィンドウカバーのマテリアルに対してサポートされます。

アルファチャンネル付きのRGB画像を使用するだけで、不透明度情報を提供できます。 また、全体の不透明度は `opacity=` コマンドを使用します (RGBと RGBA 画像の両方 )。

壁の境界は、主にダイカット境界をサポートするために、RGBA 画像もサポートします。

この [!DNL vnw] ウィンドウカバリングを定義するファイルには、不透明度チャネルを含めることができます。 これは、レンダラーと繰り返し可能なテクスチャのアルファチャンネルと `opacity=` 値を指定すると、透明と半透明の窓処理に対して、完全な不透明度効果が得られます。
