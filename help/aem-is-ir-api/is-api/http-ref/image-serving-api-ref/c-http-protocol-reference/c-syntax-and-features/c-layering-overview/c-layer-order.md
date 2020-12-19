---
description: レイヤー番号によって、z順序も決まります。
seo-description: レイヤー番号によって、z順序も決まります。
seo-title: レイヤーの順序
solution: Experience Manager
title: レイヤーの順序
topic: Scene7 Image Serving - Image Rendering API
uuid: 090f3873-8355-4b11-b05f-f34c74f02a5b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---


# レイヤーの順序{#layer-order}

レイヤー番号によって、z順序も決まります。

レイヤー0（背景レイヤー）は必須です。他のレイヤー番号は連続している必要はなく、レイヤー番号を昇順にして背景レイヤーの上に描画されます。 レイヤ番号が最も大きいレイヤは上にレンダリングされ、他のレイヤに隠れることはありません。
