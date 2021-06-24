---
description: 応答形式としてxmlを指定した場合、応答データはXMLドキュメントとしてフォーマットされ、標準のXMLパーサーで解析できます。
solution: Experience Manager
title: XMLプロパティ
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 84cae0cd-d13b-409e-bd65-71c7e973d4b8
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

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

`<prop-group>`要素は、最も外側のコンテナとして、また、グループ化プロパティとして使用されます。 グループの名前がの場合、名前はJava/JavaScriptのオブジェクト名に対応します。

>[!NOTE]
>
>文字エンコーディングは、一部の`req=`型に対して指定できます。 詳しくは、特定の`req=`コマンドの説明を参照してください。
