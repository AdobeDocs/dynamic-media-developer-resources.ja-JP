---
description: 画像レンダリングで使用されるメモリ量は、実際のサーバの負荷と使用量に大きく左右されます（例えば、ビネットの数が少ない場合と多くの場合）。ビネットのサイズや複雑さなどが異なります。
seo-description: 画像レンダリングで使用されるメモリ量は、実際のサーバの負荷と使用量に大きく左右されます（例えば、ビネットの数が少ない場合と多くの場合）。ビネットのサイズや複雑さなどが異なります。
seo-title: メモリの考慮事項
solution: Experience Manager
title: メモリの考慮事項
topic: Scene7 Image Serving - Image Rendering API
uuid: 21247081-ff27-4237-93da-5fc996417dfd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# メモリの考慮事項{#memory-considerations}

画像レンダリングで使用されるメモリ量は、実際のサーバの負荷と使用量に大きく左右されます（例えば、ビネットの数が少ない場合と多くの場合）。ビネットのサイズや複雑さなどが異なります。

最高のパフォーマンスを得るために、メモリのページング（スワップ）は避ける必要があります。

イメージレンダリングは、Image Serverのメモリ管理を共有します。 画像レンダリングを使用する場合は、追加のメモリを割り当てる必要があります。 物理メモリの30～50%は妥当です。

Image Serverのメモリ割り当て(ImageServer::PhysicalMemory)を変更する方法については、画像サービングのドキュメントを参照してください。
