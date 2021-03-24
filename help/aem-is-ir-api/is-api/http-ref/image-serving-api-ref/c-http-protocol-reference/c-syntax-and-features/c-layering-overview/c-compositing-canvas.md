---
description: レイヤーは、layer=コマンドで指定された順序で合成されます。番号の大きいレイヤーは、番号の小さいレイヤーを非表示にします。
solution: Experience Manager
title: 合成キャンバス
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# 合成キャンバス{#the-compositing-canvas}

レイヤーは、layer=コマンドで指定された順序で合成されます。番号の大きいレイヤーは、番号の小さいレイヤーを非表示にします。

レイヤー0は、常に必須で、合成画像のサイズを定義する背景レイヤーを構成します。 レイヤー0には、任意のレイヤータイプを使用できます。 レイヤー0のサイズは、コンテンツの画像またはテキストに基づいて、`size=`を使用して明示的に、または暗黙的に定義する必要があります。 レイヤー0の領域外にある他のレイヤーの領域は、出力画像に含まれません。

>[!NOTE]
>
>すべてのレイヤーが統合された後、合成画像は、[表示コマンドと属性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90)で指定された最終応答画像に変換されます。

