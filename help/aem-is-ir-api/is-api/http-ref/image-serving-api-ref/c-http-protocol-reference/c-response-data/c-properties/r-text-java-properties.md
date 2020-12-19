---
description: 応答形式としてテキストを指定した場合、返信データはJavaプロパティとして読み取り可能な形式になります。
seo-description: 応答形式としてテキストを指定した場合、返信データはJavaプロパティとして読み取り可能な形式になります。
seo-title: テキスト(Java)プロパティ
solution: Experience Manager
title: テキスト(Java)プロパティ
topic: Scene7 Image Serving - Image Rendering API
uuid: 5dba4cf7-9172-4195-968e-9ef76c25e90c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# テキスト(Java)プロパティ{#text-java-properties}

応答形式としてテキストを指定した場合、返信データはJavaプロパティとして読み取り可能な形式になります。

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

*`propertyValue`* は空にすることができます。各行の先頭と末尾、および=区切り文字の前後の空白は省略可能です。 文字列値は一重引用符または重複引用符で囲むことができますが、必須ではありません。

文字列値には、`\n`、`\t`、`\:`、`\\`などのJAVAスタイルのエスケープ文字を含めることができます。
