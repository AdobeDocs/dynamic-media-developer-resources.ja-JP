---
title: JavaScript プロパティ
description: JavaScriptを応答形式として指定した場合、返信データはJavaScript&trade; インクルードファイルとして解析されるように形式が設定されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# JavaScript プロパティ{#javascript-properties}

JavaScriptを応答形式として指定した場合、返信データはJavaScript インクルードファイルとして解析されるように形式が設定されます。

一般的なJavaScript プロパティの応答は、次のような一般的な構造になっています。

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* は空にできます。 各行の先頭と末尾、および=区切り記号の前後には、空白は任意です。 すべての値は一重引用符で囲まれています。 文字列の一重引用符は、2 つの連続する一重引用符でエスケープされます。

JavaScript プロパティの応答を解析するには、プロパティファイルが読み込まれる前に、応答で参照されるオブジェクトを作成する必要があります。 次に、`req=props` を使用してJavaScriptでレスポンス画像のサイズを取得する例を示します。

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```
