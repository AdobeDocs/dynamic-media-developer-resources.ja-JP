---
description: 画像レンダリングは、ISO-8859-1およびUTF-8エンコードのマテリアルカタログをサポートします。
seo-description: 画像レンダリングは、ISO-8859-1およびUTF-8エンコードのマテリアルカタログをサポートします。
seo-title: 文字エンコーディング
solution: Experience Manager
title: 文字エンコーディング
topic: Scene7 Image Serving - Image Rendering API
uuid: efc3971b-dca1-4b47-a197-c10270ce17c9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# 文字エンコーディング{#character-encoding}

画像レンダリングは、ISO-8859-1およびUTF-8エンコードのマテリアルカタログをサポートします。

バイトオーダーマーク(BOM)を使用して、各ファイルのエンコードを指定します。 UTF-8の場合、BOMはバイトシーケンス`EF BB BF`です。 UTF-8エンコードは、各マテリアルカタログファイルの最初でこの文字シーケンスが検出された場合に想定されます。 その他のバイトシーケンスを使用すると、ファイルはISO-8859-1標準にエンコードされたものとして解釈されます。

多くの現在のアプリケーションは、UTF-8用に設定されている場合、BOMを自動的に挿入します。
