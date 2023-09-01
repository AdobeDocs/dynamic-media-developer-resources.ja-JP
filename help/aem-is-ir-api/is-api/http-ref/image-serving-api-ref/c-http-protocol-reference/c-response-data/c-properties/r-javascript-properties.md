---
title: JavaScript プロパティ
description: 応答形式として JavaScript を指定した場合、返信データは JavaScript&trade；インクルードファイルとして解析されるように形式設定されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---

# JavaScript プロパティ{#javascript-properties}

応答形式として JavaScript を指定した場合、返信データは JavaScript インクルードファイルとして解析されるように形式設定されます。

一般的な JavaScript プロパティの応答は、次の一般的な構造を持ちます。

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

The *`propertyValue`* は空にすることができます。 各行の先頭と末尾、および=区切り文字の前後の空白はオプションです。 すべての値は一重引用符で囲まれます。 文字列内の一重引用符は、連続する 2 つの一重引用符でエスケープされます。

JavaScript プロパティ応答を解析するには、プロパティファイルが読み込まれる前に、応答で参照されるオブジェクトまたはオブジェクトを作成する必要があります。 次に、 `req=props` 応答の画像サイズを JavaScript で取得するには：

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```
