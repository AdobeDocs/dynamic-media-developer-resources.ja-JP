---
description: 応答形式としてJavaScript™を指定した場合、応答データはJavaScript™インクルードファイルとして解析されるように形式設定されます。
solution: Experience Manager
title: JavaScript™プロパティ
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---


# JavaScript™プロパティ{#javascript-properties}

応答形式としてJavaScript™を指定した場合、応答データはJavaScript™インクルードファイルとして解析されるように形式設定されます。

一般的なJavaScript™プロパティの応答は、次の一般的な構造を持ちます。

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* は空にできます。各行の先頭と末尾、および=区切り文字の前後の空白は省略可能です。 すべての値は一重引用符で囲まれます。 文字列内の一重引用符は、2つの連続した一重引用符でエスケープされます。

JavaScript™のプロパティ応答を解析するには、応答で参照されるオブジェクトまたはオブジェクトを作成してから、プロパティファイルを読み込む必要があります。 以下は、`req=props`を使用してJavaScript™の応答画像サイズを取得する例です。

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

