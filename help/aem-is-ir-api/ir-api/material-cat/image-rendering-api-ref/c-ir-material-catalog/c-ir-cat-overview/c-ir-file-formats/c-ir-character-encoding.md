---
title: 文字エンコーディング
description: 画像レンダリングでは、ISO-8859-1 および UTF-8 エンコーディングのマテリアルカタログがサポートされています。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ee7b33fd-7607-4bff-867b-6e7a837a9ed4
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# 文字エンコーディング{#character-encoding}

画像レンダリングでは、ISO-8859-1 および UTF-8 エンコーディングのマテリアルカタログがサポートされています。

各ファイルのエンコードを指定するには、バイト順マーク （BOM）を使用します。 UTF-8 の場合、BOM はバイト シーケンス `EF BB BF` です。 UTF-8 エンコーディングは、この文字シーケンスが各材料カタログファイルの最初に検出された場合に想定されます。 その他のバイトシーケンスを使用すると、ファイルは ISO-8859-1 規格にエンコードされたものとして解釈されます。

最新のアプリケーションの多くは、UTF-8 で設定されている場合、BOM を自動的に挿入します。
