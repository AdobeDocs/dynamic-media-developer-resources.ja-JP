---
title: マテリアルの不透明度の変更
description: 不透明度の変更は、重なり合うオブジェクトに適用される単色および繰り返し可能なテクスチャのほか、デカールおよび窓覆いマテリアルに対してサポートされています。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# マテリアルの不透明度の変更{#varying-material-opacity}

不透明度の変更は、重なり合うオブジェクトに適用される単色および繰り返し可能なテクスチャのほか、デカールおよび窓覆いマテリアルに対してサポートされています。

アルファチャンネル付きRGB像を用いるだけで不透明度情報を提供することができる。 また、`opacity=` コマンド（RGB画像と RGBA 画像の両方）で全体的な不透明度を変更できます。

壁の境界も RGBA 画像をサポートしており、主にダイカットの境界をサポートします。

ウィンドウカバーを定義する [!DNL vnw] ファイルには、不透明度チャネルを含めることができます。 この値は、繰り返し可能なテクスチャのアルファ チャンネルおよび `opacity=` の値とレンダラーによって結合され、薄暗く半透明のウィンドウ処理に対する全範囲の不透明効果を提供します。
