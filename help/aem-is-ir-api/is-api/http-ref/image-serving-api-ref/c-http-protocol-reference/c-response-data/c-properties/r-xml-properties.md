---
description: 応答形式としてxmlを指定した場合、応答データはXMLドキュメントとして形式設定され、標準のXMLパーサーで解析できます。
solution: Experience Manager
title: XMLプロパティ
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---


# XMLプロパティ{#xml-properties}

応答形式としてxmlを指定した場合、応答データはXMLドキュメントとして形式設定され、標準のXMLパーサーで解析できます。

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

`<prop-group>`要素は、最も外側のコンテナとして、また、プロパティのグループ化に使用されます。 グループに名前を付けた場合、名前はJava/JavaScriptのオブジェクト名に対応します。

>[!NOTE]
>
>一部の`req=`型に対して文字エンコーディングを指定できます。 詳しくは、特定の`req=`コマンドの説明を参照してください。

