---
description: テキストを応答形式として指定した場合、応答データはJava プロパティとして読み取り可能な形式になります。
solution: Experience Manager
title: テキスト（Java）プロパティ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
TQID: 'https://experienceleague.adobe.com/WNIuNvCPLdbeweHB5gkcFfeZu2WDDUk53us6SHtmO-A'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 0%

---

# テキスト（Java）プロパティ{#text-java-properties}

テキストを応答形式として指定した場合、応答データはJava プロパティとして読み取り可能な形式になります。

一般的なテキストプロパティの応答には、次の一般的な構造があります。

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

*`propertyValue`*&#x200B;は空である可能性があります。 空白は、各行の先頭と末尾、=区切り記号の前後でオプションです。 文字列の値を囲むには、一重引用符または二重引用符を使用できますが、必須ではありません。

文字列値には、`\n`、`\t`、`\:`、`\\`などのJAVA スタイルのエスケープ文字を含めることができます。
