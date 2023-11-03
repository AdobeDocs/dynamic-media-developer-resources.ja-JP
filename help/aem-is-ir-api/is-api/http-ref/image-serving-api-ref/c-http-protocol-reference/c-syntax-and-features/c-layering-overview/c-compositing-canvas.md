---
description: レイヤーは、 layer=コマンドで指定された順序で合成されます。この場合、番号の大きいレイヤーは、番号の小さいレイヤーを非表示にします。
solution: Experience Manager
title: 合成キャンバス
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# 合成キャンバス{#the-compositing-canvas}

レイヤーは、 layer=コマンドで指定された順序で合成されます。この場合、番号の大きいレイヤーは、番号の小さいレイヤーを非表示にします。

レイヤー 0 は背景レイヤーを構成し、常に必要で、合成イメージのサイズを定義します。 レイヤ 0 に対しては、任意のレイヤタイプを使用できます。 レイヤー 0 のサイズは、 `size=` または暗黙的に、コンテンツの画像またはテキストに基づいて設定されます。 その他のレイヤーのうち、レイヤー 0 の領域の外側にある領域は、出力イメージに含まれません。

>[!NOTE]
>
>すべてのレイヤーが統合された後、合成イメージは、 [コマンドと属性を表示](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).
