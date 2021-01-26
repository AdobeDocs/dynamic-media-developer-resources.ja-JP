---
description: プロパティ配列を使用してプロパティセットを更新します。
seo-description: プロパティ配列を使用してプロパティセットを更新します。
seo-title: updatePropertySet
solution: Experience Manager
title: updatePropertySet
topic: Dynamic Media Image Production System API
uuid: 21a59c5a-7799-4af6-ab9f-b0311f5f7254
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 13%

---


# updatePropertySet{#updatepropertyset}

プロパティ配列を使用してプロパティセットを更新します。

構文

## 認証済みユーザータイプ{#section-116693bbfb5d44219e62bbb1ba19de96}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-98361b063e9c41e8b2f744fabc0e13ed}

**入力(updatePropertySetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`setHandle`*` | `xsd:string` | はい | プロパティセットへのハンドル。 |
| `*`replaceProperties`*` | `xsd:string` | いいえ | プロパティを置き換えるには、`true`に設定します。 |
| `*`propertyArray`*` | `types:PropertyArray` | はい | プロパティセットの更新されたプロパティの配列。 |

**出力(updatePropertySetReturn)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-55d1c9dcd0174c6b9b52b4709f7c8bf9}

次のコードの例では、プロパティ配列内のプロパティを使用してプロパティセットを更新します。

**リクエスト**

```java
<updatePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
   <replaceProperties>true</replaceProperties>
   <propertyArray>
      <items>
         <name>application_project_whatever</name>
         <value>false</value>
      </items>
      <items>
         <name>application_server_prefix_published_test</name>
         <value>http://s7teton.macromedia.com:8080/is/image/</value>
      </items>
      <items>
         <name>application_server_prefix_origin_test</name>
         <value>http://s7teton:8080/is/image/</value>
      </items>
   </propertyArray>
</updatePropertySetParam>
```

**応答**

なし
