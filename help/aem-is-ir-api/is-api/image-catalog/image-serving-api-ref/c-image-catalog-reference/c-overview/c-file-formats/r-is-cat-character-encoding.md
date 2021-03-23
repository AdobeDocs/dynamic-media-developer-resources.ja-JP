---
description: 画像サービングは、ISO-8859-1およびUTF-8エンコードの画像カタログをサポートしています。
seo-description: 画像サービングは、ISO-8859-1およびUTF-8エンコードの画像カタログをサポートしています。
seo-title: 文字エンコーディング
solution: Experience Manager
title: 文字エンコーディング
uuid: dfb56411-40d1-4bac-9213-9104ecba2a02
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# 文字エンコーディング{#character-encoding}

画像サービングは、ISO-8859-1およびUTF-8エンコードの画像カタログをサポートしています。

バイトオーダーマーク(BOM)を使用して、各ファイルのエンコードを指定します。 UTF-8の場合、BOMはバイトシーケンス`EF BB BF`です。 UTF-8エンコードは、各画像カタログファイルの最初にこの文字シーケンスが検出された場合に想定されます。 その他のバイトシーケンスを使用すると、ファイルはISO-8859-1標準にエンコードされたものとして解釈されます。

多くの現在のアプリケーションは、UTF-8用に設定されている場合、BOMを自動的に挿入します。
