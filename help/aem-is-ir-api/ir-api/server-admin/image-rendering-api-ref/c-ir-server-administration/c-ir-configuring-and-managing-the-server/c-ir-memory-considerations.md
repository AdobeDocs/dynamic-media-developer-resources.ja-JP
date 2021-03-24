---
description: 画像レンダリングで使用されるメモリ量は、サーバの実際の読み込み量と使用量に大きく左右されます（例えば、ビネットの数が少ない場合、ビネットのサイズや複雑さなど）。
solution: Experience Manager
title: メモリの考慮事項
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、管理者、実業家
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# メモリの考慮事項{#memory-considerations}

画像レンダリングで使用されるメモリ量は、サーバの実際の読み込み量と使用量に大きく左右されます（例えば、ビネットの数が少ない場合、ビネットのサイズや複雑さなど）。

最良のパフォーマンスを得るために、メモリページング（スワップ）は避ける必要があります。

イメージレンダリングは、Image Serverのメモリ管理を共有します。 イメージレンダリングを使用する場合、追加のメモリを割り当てる必要があります。 物理メモリの30～50%は妥当なものです。

Image Serverのメモリ割り当て(ImageServer::PhysicalMemory)を変更する方法については、画像サービングのドキュメントを参照してください。
