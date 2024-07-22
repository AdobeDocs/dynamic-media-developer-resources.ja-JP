---
description: レイヤは layer= コマンドで指定した順序で合成されます。このコマンドでは、番号の大きいレイヤは番号の小さいレイヤを隠します。
solution: Experience Manager
title: 合成キャンバス
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# 合成キャンバス{#the-compositing-canvas}

レイヤは layer= コマンドで指定した順序で合成されます。このコマンドでは、番号の大きいレイヤは番号の小さいレイヤを隠します。

レイヤー 0 は背景レイヤーを構成します。背景レイヤーは常に必要であり、合成画像のサイズを定義します。 レイヤ 0 には、どのレイヤ タイプも使用できます。 レイヤー 0 のサイズは、コンテンツ画像またはテキストに基づいて、`size=` を明示的に使用するか暗黙的に定義する必要があります。 レイヤー 0 の領域外にある他のレイヤーの領域は、出力イメージには含まれません。

>[!NOTE]
>
>すべてのレイヤーが統合された後、合成画像は、[view コマンドおよび属性 ](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90) で指定されたとおりに、最終的な応答画像に変換されます。
