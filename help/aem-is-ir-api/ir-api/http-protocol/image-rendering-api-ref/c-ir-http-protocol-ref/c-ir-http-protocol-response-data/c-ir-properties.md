---
description: 次のreq=タイプのimagepropおよびpropに応答してプロパティデータが返されます。
solution: Experience Manager
title: プロパティ
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: a27ec5e4-7499-44ac-8db1-bf5d67f59632
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 4%

---

# プロパティ{#properties}

プロパティデータは、次のreq=タイプに応答して返されます。imagepropとprop。

返信データは、Javaプロパティとして読み取り可能な形式に設定されます。 一般的なテキストプロパティの応答は、次の一般的な構造を持ちます。

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` は空にできます。各行の先頭と末尾、および区切り文字「=」の前後の空白は省略可能です。 文字列値は一重引用符または二重引用符で囲むことができますが、必須ではありません。

文字列値には、`\n`、`\t`、`\:`など、JAVA形式のエスケープ文字を含めることができます。 または `\\`.

**関連項目**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
