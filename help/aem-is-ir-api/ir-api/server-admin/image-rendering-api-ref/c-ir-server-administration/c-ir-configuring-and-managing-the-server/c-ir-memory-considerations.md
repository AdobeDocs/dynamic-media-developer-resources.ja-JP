---
description: 画像レンダリングで使用されるメモリの量は大きく異なる可能性があり、実際のサーバーの負荷と使用状況に大きく依存します（例えば、少ない対多の異なる周辺光量補正、周辺光量補正のサイズと複雑さなど）。
solution: Experience Manager
title: メモリの考慮事項
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
TQID: 'https://experienceleague.adobe.com/l41dx4mMn82TvImVVCJJKgJZbP-mWT5KbnzfZ5xFJqg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 129
ht-degree: 0%

---

# メモリの考慮事項{#memory-considerations}

画像レンダリングで使用されるメモリの量は大きく異なる可能性があり、実際のサーバーの負荷と使用状況に大きく依存します（例えば、少ない対多の異なる周辺光量補正、周辺光量補正のサイズと複雑さなど）。

最高のパフォーマンスを得るには、メモリページング（スワップ）を避ける必要があります。

Image Renderingは、Image Serverのメモリ管理を共有します。 画像レンダリングを使用する場合は、追加のメモリを割り当てる必要があります。 物理メモリの30～50%が妥当な場合があります。

Image Serverのメモリ割り当てを変更する方法（ImageServer::PhysicalMemory）については、Image Servingのドキュメントを参照してください。
