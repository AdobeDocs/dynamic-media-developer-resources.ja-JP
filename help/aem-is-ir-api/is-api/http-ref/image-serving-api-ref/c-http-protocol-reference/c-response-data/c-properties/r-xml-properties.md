---
description: XML が応答形式として指定されている場合、応答データは、標準の XML パーサーで解析できる XML ドキュメントとしてフォーマットされます。
solution: Experience Manager
title: XML プロパティ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84cae0cd-d13b-409e-bd65-71c7e973d4b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---

# XML プロパティ{#xml-properties}

XML が応答形式として指定されている場合、応答データは、標準の XML パーサーで解析できる XML ドキュメントとしてフォーマットされます。

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

`<prop-group>` 要素は、最も外側のコンテナとして、またプロパティのグループ化に使用されます。 グループに名前を付けると、名前は Java/JavaScript オブジェクト名に対応します。

>[!NOTE]
>
>文字エンコーディングは、一部の `req=` タイプで指定できます。 詳細については、特定の `req=` コマンドの説明を参照してください。
