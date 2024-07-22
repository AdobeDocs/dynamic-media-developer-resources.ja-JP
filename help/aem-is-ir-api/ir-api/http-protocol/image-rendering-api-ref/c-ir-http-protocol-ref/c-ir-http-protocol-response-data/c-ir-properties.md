---
title: プロパティ
description: プロパティデータは、次の req= タイプの imageprops および prop に応答して返されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a27ec5e4-7499-44ac-8db1-bf5d67f59632
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# プロパティ{#properties}

プロパティデータは、imageprops および props の req= タイプに応答して返されます。

返信データは、Java™ プロパティとして読み取れるようにフォーマットされます。 一般的なテキストプロパティの応答は、次のような一般的な構造になっています。

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` 空にすることができます。 各行の先頭と末尾、および「=」区切り記号の前後の空白は任意です。 一重引用符または二重引用符は、文字列値を囲むために使用できますが、必須ではありません。

文字列値には、`\n`、`\t`、`\:`、`\\` など、JAVA スタイルのエスケープ文字を含めることができます。

**関連トピック**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
