---
description: レイヤーは、layer= コマンドで指定した順序で合成されます。この場合、番号の大きいレイヤーは番号の小さいレイヤーを非表示にします。
solution: Experience Manager
title: 合成キャンバス
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
TQID: 'https://experienceleague.adobe.com/WNvq6dLRetz3iEbtP0ugmOPagUfTCaa5eXdB3lEzEaQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 136
ht-degree: 0%

---

# 合成キャンバス{#the-compositing-canvas}

レイヤーは、layer= コマンドで指定した順序で合成されます。この場合、番号の大きいレイヤーは番号の小さいレイヤーを非表示にします。

レイヤー0は背景レイヤーを構成します。背景レイヤーは常に必要であり、合成画像のサイズを定義します。 レイヤー0には、いずれかのレイヤータイプを使用できます。 レイヤー0のサイズは、`size=`を使用して明示的に定義するか、コンテンツ画像またはテキストに基づいて暗黙的に定義する必要があります。 レイヤー0の領域の外側にある他のレイヤーの領域は、出力画像に含まれません。

>[!NOTE]
>
>すべてのレイヤーを統合した後、合成画像は、[表示コマンドと属性](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90)で指定されたとおりに、最終的な応答画像に変換されます。
