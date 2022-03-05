---
title: プロパティ
description: プロパティデータは、次の req=タイプの imageprop および prop に応答して返されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a27ec5e4-7499-44ac-8db1-bf5d67f59632
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# プロパティ{#properties}

プロパティデータは、次の req=タイプに応答して返されます。imageprop と prop。

返信データは、Java™プロパティとして読み取り可能な形式に設定されます。 一般的なテキストプロパティ応答の一般的な構造は次のとおりです。

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` 空にすることができます。 各行の先頭と末尾、「=」区切り文字の前後の空白はオプションです。 一重引用符または二重引用符を使用して文字列値を囲むことができますが、必須ではありません。

文字列値には、次のような JAVA 形式のエスケープ文字が含まれる場合があります。 `\n`, `\t`, `\:`または `\\`.

**関連項目**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
