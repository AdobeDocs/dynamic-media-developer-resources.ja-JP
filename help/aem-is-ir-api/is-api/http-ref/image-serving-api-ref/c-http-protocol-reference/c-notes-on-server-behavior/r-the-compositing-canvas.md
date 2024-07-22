---
description: req=img の場合、合成キャンバスのサイズはレイヤー 0 のサイズで決まります。
solution: Experience Manager
title: 合成キャンバス
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# 合成キャンバス{#the-compositing-canvas}

req=img の場合、合成キャンバスのサイズはレイヤー 0 のサイズで決まります。

レイヤー 0 の `size=` が明示的に指定されていない場合、レイヤー変換を使用して合成キャンバスのサイズが計算されます（以下を参照）。

`req=tmb` の場合、合成キャンバスのサイズはレイヤ 0 に指定された `size=` によって決まります。サイズが指定されていない場合、合成キャンバスのサイズはビューの rect に設定されます（以下を参照）。
