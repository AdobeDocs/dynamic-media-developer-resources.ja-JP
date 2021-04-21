---
description: 画像レンダリングは、ISO-8859-1およびUTF-8エンコードのマテリアルカタログをサポートします。
solution: Experience Manager
title: 文字エンコーディング
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# 文字エンコーディング{#character-encoding}

画像レンダリングは、ISO-8859-1およびUTF-8エンコードのマテリアルカタログをサポートします。

バイトオーダーマーク(BOM)を使用して、各ファイルのエンコードを指定します。 UTF-8の場合、BOMはバイトシーケンス`EF BB BF`です。 UTF-8エンコードは、各マテリアルカタログファイルの最初でこの文字シーケンスが検出された場合に想定されます。 その他のバイトシーケンスを使用すると、ファイルはISO-8859-1標準にエンコードされたものとして解釈されます。

多くの現在のアプリケーションは、UTF-8用に設定されている場合、BOMを自動的に挿入します。
