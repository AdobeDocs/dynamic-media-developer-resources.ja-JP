---
description: 次のreq=タイプの画像propとpropに応答して、プロパティデータが返されます。
seo-description: 次のreq=タイプの画像propとpropに応答して、プロパティデータが返されます。
seo-title: プロパティ
solution: Experience Manager
title: プロパティ
uuid: b4e1de52-db0a-43dc-aefe-26e8f5020e79
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---


# プロパティ{#properties}

プロパティデータは、次のreq=タイプに応じて返されます。imagepropsとprops

返信データは、Javaプロパティとして読み取り可能な形式になっています。 一般的なテキストプロパティの応答は、次の一般的な構造を持ちます。

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` は空にできます。各行の先頭と末尾、および「=」区切り文字の前後に空白を入れることはできません。 文字列値は一重引用符または重複引用符で囲むことができますが、必須ではありません。

文字列値には、`\n`、`\t`、`\:`など、JAVAスタイルのエスケープ文字を含めることができます。 または `\\`.

**関連項目**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
