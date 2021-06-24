---
description: req=imgの場合、合成キャンバスのサイズはレイヤ0のサイズによって完全に決まります。
solution: Experience Manager
title: 合成キャンバス
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---

# 合成キャンバス{#the-compositing-canvas}

req=imgの場合、合成キャンバスのサイズはレイヤ0のサイズによって完全に決まります。

レイヤ0の`size=`を明示的に指定しない場合は、レイヤ変換を使用して合成キャンバスのサイズを計算します（以下を参照）。

`req=tmb`の場合、合成キャンバスのサイズはレイヤ0に指定された`size=`によって決まります。サイズが指定されていない場合は、合成キャンバスのサイズがビューの正しいサイズに設定されます（以下を参照）。
