---
description: プロパティデータは、次のreq=タイプの画像propとpropに応じて返されます。
seo-description: プロパティデータは、次のreq=タイプの画像propとpropに応じて返されます。
seo-title: プロパティ
solution: Experience Manager
title: プロパティ
topic: Scene7 Image Serving - Image Rendering API
uuid: b4e1de52-db0a-43dc-aefe-26e8f5020e79
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# プロパティ{#properties}

プロパティデータは、次のreq=タイプに応じて返されます。imagepropとprop

返信データは、Javaプロパティとして読み取り可能な形式になっています。 一般的なテキストプロパティの応答は、次のような一般的な構造を持ちます。

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` は空にできます。 各行の先頭と末尾、および「=」区切り文字の前後の空白はオプションです。 文字列値は一重引用符または二重引用符で囲むことができますが、必須ではありません。

文字列値には、JAVAスタイルのエスケープ文字（¥n、¥t、¥：など）を含めることができます。 または \\.

**関連項目**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
