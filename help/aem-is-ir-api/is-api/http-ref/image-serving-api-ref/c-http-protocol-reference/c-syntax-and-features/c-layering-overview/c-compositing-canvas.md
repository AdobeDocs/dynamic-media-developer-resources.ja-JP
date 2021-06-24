---
description: レイヤは、 layer=コマンドで指定された順序で合成されます。ここで、番号の大きいレイヤは、番号の小さいレイヤを非表示にします。
solution: Experience Manager
title: 合成キャンバス
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# 合成キャンバス{#the-compositing-canvas}

レイヤは、 layer=コマンドで指定された順序で合成されます。ここで、番号の大きいレイヤは、番号の小さいレイヤを非表示にします。

レイヤー0は、常に必要で、合成画像のサイズを定義する背景レイヤーを構成します。 レイヤ0に対しては、任意のレイヤタイプを使用できます。 レイヤー0のサイズは、`size=`を使用して明示的に定義するか、コンテンツの画像またはテキストに基づいて暗黙的に定義する必要があります。 その他のレイヤーの領域のうち、レイヤー0の領域外にある領域は、出力イメージに含まれません。

>[!NOTE]
>
>すべてのレイヤが統合された後、合成画像は、[viewコマンドと属性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90)で指定された最終応答画像に変換されます。
