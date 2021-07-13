---
description: 応答形式にテキストを指定した場合、返信データは、Javaプロパティとして読み取り可能な形式に設定されます。
solution: Experience Manager
title: テキスト(Java)プロパティ
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# テキスト(Java)プロパティ{#text-java-properties}

応答形式にテキストを指定した場合、返信データは、Javaプロパティとして読み取り可能な形式に設定されます。

一般的なテキストプロパティの応答は、次の一般的な構造を持ちます。

```
#S7Z OK
#
<varname>
  timeStamp
</varname>
<varname>
  objectName.propertyName
</varname>=
<varname>
  propertyValue
</varname>
...
```

*`propertyValue`* は空の場合があります。各行の先頭と末尾、および=区切り文字の前と後の空白は省略可能です。 文字列値は一重引用符または二重引用符で囲むことができますが、必須ではありません。

文字列値には、`\n`、`\t`、`\:`、`\\`など、JAVA形式のエスケープ文字を含めることができます。
