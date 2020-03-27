---
description: レイヤーは、layer=コマンドで指定された順序で合成されます。大きい方の番号のレイヤーでは、小さい方の番号のレイヤーは非表示になります。
seo-description: レイヤーは、layer=コマンドで指定された順序で合成されます。大きい方の番号のレイヤーでは、小さい方の番号のレイヤーは非表示になります。
seo-title: 合成キャンバス
solution: Experience Manager
title: 合成キャンバス
topic: Scene7 Image Serving - Image Rendering API
uuid: 057b11cb-36f3-40f8-b095-9ad05da858a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 合成キャンバス{#the-compositing-canvas}

レイヤーは、layer=コマンドで指定された順序で合成されます。大きい方の番号のレイヤーでは、小さい方の番号のレイヤーは非表示になります。

レイヤー0は背景レイヤーを構成し、常に必須で、合成画像のサイズを定義します。 レイヤー0に対しては、任意のレイヤータイプを使用できます。 レイヤー0のサイズは、コンテンツの画像またはテキストに基づいて、を使用し `size=` て明示的に、または暗黙的に定義する必要があります。 レイヤー0の領域外にある他のレイヤーの領域は、出力画像に含まれません。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>すべてのレイヤーを統合した後、合成画像は、ビューコマンドと属性で指定した最終応答画像 [に変換されます](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90)。

