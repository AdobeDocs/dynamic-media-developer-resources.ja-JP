---
description: req=imgの場合、合成キャンバスのサイズは、レイヤ0のサイズだけで決まります。
seo-description: req=imgの場合、合成キャンバスのサイズは、レイヤ0のサイズだけで決まります。
seo-title: 合成キャンバス
solution: Experience Manager
title: 合成キャンバス
topic: Scene7 Image Serving - Image Rendering API
uuid: 7ec2f1b3-61fc-4bfe-96d2-a5946a238e74
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 0%

---


# 合成キャンバス{#the-compositing-canvas}

req=imgの場合、合成キャンバスのサイズは、レイヤ0のサイズだけで決まります。

レイヤ0の`size=`を明示的に指定しない場合、レイヤ変換を使用して合成キャンバスのサイズが計算されます（以下を参照）。

`req=tmb`の場合、合成キャンバスのサイズはレイヤ0に対して指定された`size=`によって決まります。サイズが指定されていない場合は、合成キャンバスのサイズが表示rectに設定されます（以下を参照）。
