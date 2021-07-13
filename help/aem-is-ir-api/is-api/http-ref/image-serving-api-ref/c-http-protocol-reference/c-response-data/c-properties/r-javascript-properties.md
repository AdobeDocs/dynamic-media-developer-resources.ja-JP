---
description: 応答形式としてJavaScript™を指定した場合、応答データはJavaScript™インクルードファイルとして解析されるように形式設定されます。
solution: Experience Manager
title: JavaScript™のプロパティ
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---

# JavaScript™のプロパティ{#javascript-properties}

応答形式としてJavaScript™を指定した場合、応答データはJavaScript™インクルードファイルとして解析されるように形式設定されます。

一般的なJavaScript™プロパティ応答は、次の一般的な構造を持ちます。

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* は空にできます。各行の先頭と末尾、および=区切り文字の前と後の空白は省略可能です。 すべての値は一重引用符で囲まれます。 文字列内の一重引用符は、連続する2つの一重引用符でエスケープされます。

JavaScript™プロパティ応答を解析するには、プロパティファイルが読み込まれる前に、応答で参照されるオブジェクトまたはオブジェクトを作成する必要があります。 次に、`req=props`を使用してJavaScript™で応答画像のサイズを取得する例を示します。

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```
