---
description: レイヤーは、layer=コマンドで指定された順序で合成されます。番号の大きいレイヤーは、番号の小さいレイヤーを非表示にします。
seo-description: レイヤーは、layer=コマンドで指定された順序で合成されます。番号の大きいレイヤーは、番号の小さいレイヤーを非表示にします。
seo-title: 合成キャンバス
solution: Experience Manager
title: 合成キャンバス
topic: Scene7 Image Serving - Image Rendering API
uuid: 057b11cb-36f3-40f8-b095-9ad05da858a9
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---


# 合成キャンバス{#the-compositing-canvas}

レイヤーは、layer=コマンドで指定された順序で合成されます。番号の大きいレイヤーは、番号の小さいレイヤーを非表示にします。

レイヤー0は、常に必須で、合成画像のサイズを定義する背景レイヤーを構成します。 レイヤー0には、任意のレイヤータイプを使用できます。 レイヤー0のサイズは、コンテンツの画像またはテキストに基づいて、`size=`を使用して明示的に、または暗黙的に定義する必要があります。 レイヤー0の領域外にある他のレイヤーの領域は、出力画像に含まれません。

>[!NOTE]
>
>すべてのレイヤーが統合された後、合成画像は、[表示コマンドと属性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90)で指定された最終応答画像に変換されます。

