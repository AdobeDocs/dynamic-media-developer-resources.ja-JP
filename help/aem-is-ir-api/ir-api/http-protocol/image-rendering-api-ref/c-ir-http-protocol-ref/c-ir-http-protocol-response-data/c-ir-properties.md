---
description: プロパティデータは、次のreq=タイプの画像propとpropに応じて返されます。
seo-description: プロパティデータは、次のreq=タイプの画像propとpropに応じて返されます。
seo-title: プロパティ
solution: Experience Manager
title: プロパティ
topic: Scene7 Image Serving - Image Rendering API
uuid: b4e1de52-db0a-43dc-aefe-26e8f5020e79
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5

---


# プロパティ{#properties}

プロパティデータは、次のreq=タイプに応じて返されます。imagepropとprop

返信データは、Javaプロパティとして読み取り可能な形式になっています。 一般的なテキストプロパティの応答は、次のような一般的な構造を持ちます。

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` は空にできます。 各行の先頭と末尾、および「=」区切り文字の前後の空白はオプションです。 一重引用符または重複引用符を使用して文字列値を囲むことはできますが、必須ではありません。

文字列値には、、などのJAVAスタイルのエスケープ文字を含める `\n`ことがで `\t`きま `\:`す。 または `\\`.

**関連項目**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
