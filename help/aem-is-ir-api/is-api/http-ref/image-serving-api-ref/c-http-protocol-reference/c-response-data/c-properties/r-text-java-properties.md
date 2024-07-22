---
description: 応答形式としてテキストを指定した場合、返信データは Java プロパティとして読み取り可能な形式になります。
solution: Experience Manager
title: テキスト（Java）プロパティ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# テキスト（Java）プロパティ{#text-java-properties}

応答形式としてテキストを指定した場合、返信データは Java プロパティとして読み取り可能な形式になります。

一般的なテキストプロパティの応答は、次のような一般的な構造になっています。

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

*`propertyValue`* は空の場合があります。 各行の先頭と末尾、および=区切り記号の前後には、空白は任意です。 一重引用符または二重引用符は、文字列値を囲むために使用できますが、必須ではありません。

文字列値には、`\n`、`\t`、`\:`、`\\` など、JAVA スタイルのエスケープ文字を含めることができます。
