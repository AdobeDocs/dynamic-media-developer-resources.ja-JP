---
description: 画像レンダリングで使用されるメモリ量は、実際のサーバー負荷と使用状況に大きく依存し、大きく異なる場合があります（例えば、少数のビネット、ビネットのサイズ、複雑さなど）。
solution: Experience Manager
title: メモリに関する考慮事項
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: 62eaa41c-a61c-4bcd-8dd9-9c3423bf82ef
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# メモリに関する考慮事項{#memory-considerations}

画像レンダリングで使用されるメモリ量は、実際のサーバー負荷と使用状況に大きく依存し、大きく異なる場合があります（例えば、少数のビネット、ビネットのサイズ、複雑さなど）。

最高のパフォーマンスを得るには、メモリページング（スワップ）を回避する必要があります。

画像レンダリングは、Image Serverのメモリ管理を共有します。 画像レンダリングを使用する場合は、追加のメモリを割り当てる必要があります。 物理メモリの30～50%は合理的な場合があります。

Image Serverのメモリ割り当て(ImageServer::PhysicalMemory)を変更する方法については、画像サービングのドキュメントを参照してください。
