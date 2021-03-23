---
description: 応答形式としてxmlを指定した場合、応答データはXMLドキュメントとして形式設定され、標準のXMLパーサーで解析できます。
seo-description: 応答形式としてxmlを指定した場合、応答データはXMLドキュメントとして形式設定され、標準のXMLパーサーで解析できます。
seo-title: XMLプロパティ
solution: Experience Manager
title: XMLプロパティ
uuid: 9d169ad2-e466-4ab3-8900-ea9c6125edad
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '145'
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

