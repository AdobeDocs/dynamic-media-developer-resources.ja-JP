---
description: 応答形式としてテキストを指定した場合、返信データはJavaプロパティとして読み取り可能な形式になります。
solution: Experience Manager
title: テキスト(Java)プロパティ
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '107'
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
