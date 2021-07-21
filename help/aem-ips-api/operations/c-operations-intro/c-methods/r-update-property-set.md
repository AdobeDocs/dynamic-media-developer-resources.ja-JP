---
description: プロパティ配列を使用してプロパティセットを更新します。
solution: Experience Manager
title: updatePropertySet
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: bbe6a664-b6e1-4b46-867d-a134070b13da
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 14%

---

# updatePropertySet{#updatepropertyset}

プロパティ配列を使用してプロパティセットを更新します。

構文

## 許可されたユーザーの種類 {#section-116693bbfb5d44219e62bbb1ba19de96}

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
| `*`setHandle`*` | `xsd:string` | はい | プロパティセットに対するハンドル。 |
| `*`replaceProperties`*` | `xsd:string` | いいえ | `true`に設定すると、プロパティが置き換えられます。 |
| `*`propertyArray`*` | `types:PropertyArray` | はい | プロパティセットの更新されたプロパティの配列。 |

**出力(updatePropertySetReturn)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-55d1c9dcd0174c6b9b52b4709f7c8bf9}

次のコードのサンプルを使用すると、プロパティ配列内のプロパティを使用してプロパティセットを更新できます。

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
