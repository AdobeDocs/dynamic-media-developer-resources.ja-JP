---
description: xmlが応答形式として指定されている場合、応答データは、任意の標準XML パーサーで解析できるXML ドキュメントとしてフォーマットされます。
solution: Experience Manager
title: XML プロパティ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84cae0cd-d13b-409e-bd65-71c7e973d4b8
TQID: 'https://experienceleague.adobe.com/Nljy83DDIbeY6l-d6F02NlaFzyCFJny7iesxnF9mFyo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 109
ht-degree: 0%

---

# XML プロパティ{#xml-properties}

xmlが応答形式として指定されている場合、応答データは、任意の標準XML パーサーで解析できるXML ドキュメントとしてフォーマットされます。

一般的なプロパティの応答ドキュメントには、次の一般的な構造があります。

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

`<prop-group>`要素は、最も外側のコンテナとして、およびプロパティのグループ化に使用されます。 グループ名が指定されている場合、その名前はJava/JavaScript オブジェクト名に対応します。

>[!NOTE]
>
>文字エンコーディングは、一部の`req=`種類に対して指定できます。 詳しくは、特定の`req=` コマンドの説明を参照してください。
