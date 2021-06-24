---
description: 可変不透明度は、重なり合うオブジェクトに適用されるべた塗りおよび繰り返し可能なテクスチャ、デカールやウィンドウカバーマテリアルに対してサポートされています。
solution: Experience Manager
title: マテリアルの不透明度の変化
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# マテリアルの不透明度の変化{#varying-material-opacity}

可変不透明度は、重なり合うオブジェクトに適用されるべた塗りおよび繰り返し可能なテクスチャ、デカールやウィンドウカバーマテリアルに対してサポートされています。

アルファチャンネル付きのRGB画像を使用するだけで、不透明度情報を提供できます。 また、`opacity=`コマンドを使用して、全体の不透明度を変更できます（RGB画像とRGBA画像の両方）。

壁の境界は、主にダイカット境界をサポートするために、RGBA画像もサポートします。

ウィンドウのカバーを定義する[!DNL vnw]ファイルには、不透明度チャンネルを含めることができます。このチャンネルは、繰り返し可能なテクスチャのアルファチャンネルと`opacity=`値を組み合わせて、透明度効果を完全に適用します。
