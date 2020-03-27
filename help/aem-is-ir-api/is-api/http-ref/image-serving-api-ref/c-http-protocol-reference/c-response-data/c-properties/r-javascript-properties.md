---
description: javascriptを応答形式として指定した場合、応答データはJavaScriptインクルードファイルとして解析されるように形式設定されます。
seo-description: javascriptを応答形式として指定した場合、応答データはJavaScriptインクルードファイルとして解析されるように形式設定されます。
seo-title: JavaScriptプロパティ
solution: Experience Manager
title: JavaScriptプロパティ
topic: Scene7 Image Serving - Image Rendering API
uuid: 832a927e-ecaf-438c-8fbf-a702d58902d8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# JavaScriptプロパティ{#javascript-properties}

javascriptを応答形式として指定した場合、応答データはJavaScriptインクルードファイルとして解析されるように形式設定されます。

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

*`propertyValue`* は空の場合があります。 各行の先頭と末尾、および=区切り文字の前後の空白はオプションです。 すべての値は一重引用符で囲まれます。 文字列内の一重引用符は、2つの連続した一重引用符でエスケープされます。

JavaScriptプロパティの応答を解析するには、応答内で参照されるすべてのオブジェクトを作成してから、プロパティファイルを読み込む必要があります。 を使用して、JavaScriptで応答 `req=props` 画像のサイズを取得する例を次に示します。

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

