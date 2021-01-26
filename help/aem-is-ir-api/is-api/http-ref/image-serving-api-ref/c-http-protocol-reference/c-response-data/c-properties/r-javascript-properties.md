---
description: 応答形式としてjavascriptを指定した場合、応答データはJavaScriptインクルードファイルとして解析されるように形式設定されます。
seo-description: 応答形式としてjavascriptを指定した場合、応答データはJavaScriptインクルードファイルとして解析されるように形式設定されます。
seo-title: JavaScriptプロパティ
solution: Experience Manager
title: JavaScriptプロパティ
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 832a927e-ecaf-438c-8fbf-a702d58902d8
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---


# JavaScriptプロパティ{#javascript-properties}

応答形式としてjavascriptを指定した場合、応答データはJavaScriptインクルードファイルとして解析されるように形式設定されます。

一般的なJavaScriptプロパティの応答は、次の一般的な構造を持ちます。

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* は空にすることができます。各行の先頭と末尾、および=区切り文字の前後の空白は省略可能です。 すべての値は一重引用符で囲まれます。 文字列内の一重引用符は、2つの連続した一重引用符でエスケープされます。

JavaScriptプロパティの応答を解析するには、応答で参照されるオブジェクトを作成してから、プロパティファイルを読み込む必要があります。 以下は、`req=props`を使用してJavaScriptで応答画像サイズを取得する例です。

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

