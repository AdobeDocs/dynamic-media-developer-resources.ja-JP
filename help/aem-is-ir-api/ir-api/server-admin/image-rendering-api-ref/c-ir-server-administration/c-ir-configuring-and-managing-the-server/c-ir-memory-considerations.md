---
description: 画像レンダリングで使用されるメモリ量は多岐にわたり、実際のサーバーの負荷と使用状況によって大きく異なります（例えば、多数の異なるビネットに対して数が少ない、ビネットのサイズと複雑さなど）。
solution: Experience Manager
title: メモリに関する考慮事項
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---

# メモリに関する考慮事項{#memory-considerations}

画像レンダリングで使用されるメモリ量は多岐にわたり、実際のサーバーの負荷と使用状況によって大きく異なります（例えば、多数の異なるビネットに対して数が少ない、ビネットのサイズと複雑さなど）。

最高のパフォーマンスを得るには、メモリページング（スワップ）を避ける必要があります。

画像レンダリングは、Image Server のメモリ管理を共有します。 画像レンダリングを使用する場合、追加のメモリを割り当てる必要があります。 物理メモリの 30～50% が妥当な場合がある。

Image Server のメモリ割り当ての変更方法については、画像サービングに関するドキュメントを参照してください（ImageServer::PhysicalMemory）。
