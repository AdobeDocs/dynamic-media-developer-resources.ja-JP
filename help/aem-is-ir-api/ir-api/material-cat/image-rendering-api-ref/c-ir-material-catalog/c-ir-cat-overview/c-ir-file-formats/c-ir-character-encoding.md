---
title: 文字エンコーディング
description: 画像レンダリングは、ISO-8859-1 および UTF-8 エンコーディングのマテリアルカタログをサポートします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ee7b33fd-7607-4bff-867b-6e7a837a9ed4
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# 文字エンコーディング{#character-encoding}

画像レンダリングは、ISO-8859-1 および UTF-8 エンコーディングのマテリアルカタログをサポートします。

バイトオーダーマーク (BOM) は、各ファイルのエンコーディングを指定するために使用されます。 UTF-8 の場合、BOM はバイトシーケンスです `EF BB BF`. UTF-8 エンコーディングは、各マテリアルカタログファイルの最初にこの文字列が検出された場合に想定されます。 その他のバイトシーケンスを使用すると、そのファイルは ISO-8859-1 標準に従ってエンコードされていると解釈されます。

多くの現代アプリケーションは、UTF-8 用に設定されている場合、BOM を自動的に挿入します。
