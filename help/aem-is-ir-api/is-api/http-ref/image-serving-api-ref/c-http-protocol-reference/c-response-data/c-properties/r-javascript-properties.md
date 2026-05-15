---
title: JavaScript properties
description: JavaScriptをレスポンス形式として指定した場合、応答データはJavaScript&trade; インクルード ファイルとして解析されるようにフォーマットされます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
TQID: 'https://experienceleague.adobe.com/T6xqUHtT9XX4b9bP-wi-b0dDBe2LHE3vcBcJI6cMKqE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 137
ht-degree: 0%

---

# JavaScript properties{#javascript-properties}

JavaScriptがレスポンス形式として指定されている場合、応答データはJavaScript インクルードファイルとして解析されるようにフォーマットされます。

JavaScriptの一般的なプロパティレスポンスには、次の一般的な構造があります。

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`*&#x200B;は空にできます。 空白は、各行の先頭と末尾、=区切り記号の前後でオプションです。 すべての値は、一重引用符で囲まれます。 文字列内の一重引用符は、2つの連続する一重引用符でエスケープされます。

JavaScriptのプロパティレスポンスを解析するには、プロパティファイルを読み込む前に、レスポンスで参照されているすべてのオブジェクトまたはオブジェクトを作成する必要があります。 次に、`req=props`を使用してJavaScriptでレスポンス画像サイズを取得する例を示します。

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```
