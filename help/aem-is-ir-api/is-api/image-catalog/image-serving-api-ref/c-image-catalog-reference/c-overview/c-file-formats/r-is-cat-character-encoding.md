---
description: 画像サービングは、ISO-8859-1およびUTF-8エンコードの画像カタログをサポートしています。
solution: Experience Manager
title: 文字エンコーディング
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# 文字エンコーディング{#character-encoding}

画像サービングは、ISO-8859-1およびUTF-8エンコードの画像カタログをサポートしています。

バイトオーダーマーク(BOM)を使用して、各ファイルのエンコードを指定します。 UTF-8の場合、BOMはバイトシーケンス`EF BB BF`です。 UTF-8エンコードは、各画像カタログファイルの最初にこの文字シーケンスが検出された場合に想定されます。 その他のバイトシーケンスを使用すると、ファイルはISO-8859-1標準にエンコードされたものとして解釈されます。

多くの現在のアプリケーションは、UTF-8用に設定されている場合、BOMを自動的に挿入します。
