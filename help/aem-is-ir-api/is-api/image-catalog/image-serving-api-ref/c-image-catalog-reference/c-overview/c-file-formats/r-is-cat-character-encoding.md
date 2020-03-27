---
description: 画像サービングは、ISO-8859-1およびUTF-8エンコードの画像カタログをサポートします。
seo-description: 画像サービングは、ISO-8859-1およびUTF-8エンコードの画像カタログをサポートします。
seo-title: 文字エンコーディング
solution: Experience Manager
title: 文字エンコーディング
topic: Scene7 Image Serving - Image Rendering API
uuid: dfb56411-40d1-4bac-9213-9104ecba2a02
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Character encoding{#character-encoding}

画像サービングは、ISO-8859-1およびUTF-8エンコードの画像カタログをサポートします。

バイトオーダーマーク(BOM)を使用して、各ファイルのエンコーディングを指定します。 UTF-8の場合、BOMはバイトシーケンスです `EF BB BF`。 各画像カタログファイルの最初でこの文字シーケンスが検出された場合、UTF-8エンコーディングが想定されます。 その他のバイトシーケンスを使用すると、ファイルはISO-8859-1標準にエンコードされたものとして解釈されます。

UTF-8用に設定された最新のアプリケーションの多くは、BOMを自動的に挿入します。
