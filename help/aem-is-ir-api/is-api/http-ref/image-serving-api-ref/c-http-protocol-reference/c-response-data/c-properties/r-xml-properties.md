---
description: 応答形式としてxmlを指定した場合、応答データはXMLドキュメントとしてフォーマットされ、標準のXMLパーサーで解析できます。
seo-description: 応答形式としてxmlを指定した場合、応答データはXMLドキュメントとしてフォーマットされ、標準のXMLパーサーで解析できます。
seo-title: XMLプロパティ
solution: Experience Manager
title: XMLプロパティ
topic: Scene7 Image Serving - Image Rendering API
uuid: 9d169ad2-e466-4ab3-8900-ea9c6125edad
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# XMLプロパティ{#xml-properties}

応答形式としてxmlを指定した場合、応答データはXMLドキュメントとしてフォーマットされ、標準のXMLパーサーで解析できます。

一般的なプロパティ応答ドキュメントの構造は次のとおりです。

```
<?xml version="1.0" encoding="UTF-8" ?>
<prop-group>
   <prop-group name="
<varname>
  objectName
</varname>">
       <property name="
<varname>
  propertyName
</varname>" value="
<varname>
  propertyValue
</varname>" />
       ...
    </prop-group>
 ...
</prop-group>
```

要素は `<prop-group>` 最も外側のコンテナとして、またプロパティのグループ化に使用されます。 グループ名が付けられている場合、その名前はJava/JavaScriptのオブジェクト名に対応します。

>[!NOTE]
>
>文字エンコーディングは、一部のタイプに対して指定で `req=` きます。 詳しくは、特定のコマンドの説明を `req=`参照してください。

