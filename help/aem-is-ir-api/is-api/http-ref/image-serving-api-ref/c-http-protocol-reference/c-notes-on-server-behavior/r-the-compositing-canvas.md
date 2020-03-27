---
description: req=imgの場合、合成キャンバスのサイズは、レイヤー0のサイズだけで決まります。
seo-description: req=imgの場合、合成キャンバスのサイズは、レイヤー0のサイズだけで決まります。
seo-title: 合成キャンバス
solution: Experience Manager
title: 合成キャンバス
topic: Scene7 Image Serving - Image Rendering API
uuid: 7ec2f1b3-61fc-4bfe-96d2-a5946a238e74
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 合成キャンバス{#the-compositing-canvas}

req=imgの場合、合成キャンバスのサイズは、レイヤー0のサイズだけで決まります。

レイヤ0の `size=` 値を明示的に指定しない場合、レイヤ変換を使用して合成キャンバスのサイズが計算されます（以下を参照）。

合成キ `req=tmb``size=` ャンバスのサイズは、レイヤ0に対して指定されたサイズによって決まります。サイズが指定されていない場合は、合成キャンバスのサイズがビューレクトに設定されます（以下を参照）。
