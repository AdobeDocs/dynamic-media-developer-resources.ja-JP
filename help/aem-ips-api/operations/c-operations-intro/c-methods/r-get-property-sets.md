---
description: タイプハンドルに関連付けられたプロパティセットを取得します。
solution: Experience Manager
title: getPropertySets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: da6923c3-9b86-4595-8205-645fb10e03b0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 18%

---

# getPropertySets{#getpropertysets}

タイプハンドルに関連付けられたプロパティセットを取得します。

構文

## 認証済みユーザータイプ {#section-da858360b72941bfa8d9558b4da7d4da}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-d8da2847e77e4a95a4441d9848cac775}

**入力 (getPropertySetsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| typeHandle | `xsd:string` | はい | プロパティセットタイプのハンドル。 |
| primaryOwnerHandle | `xsd:string` | はい | データベースオブジェクトに連結されたデータの主所有者。 |
| secondaryOwnerHandle | `xsd:string` | いいえ | データのセカンダリ所有者（オプション）。 |

**出力 (getPropertySetsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| setArray | `types:PropertySetArray` | はい | プロパティセットの配列。 |

## 例 {#section-1358af974eab4259864910337a6f0bd2}

このコード例は、タイプハンドルで指定された主所有者のプロパティセットを返します。

**リクエスト**

```java
<getPropertySetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
   <primaryOwnerHandle>u|41|strangio@adobe.com</primaryOwnerHandle>
</getPropertySetsParam>
```

**応答**

```java
<getPropertySetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setArray>
      <items>
         <setHandle>ps|941</setHandle>
         <typeHandle>pt|10801</typeHandle>
         <propertyArray>
            <items>
               <name>application_server_prefix_published_test</name>
               <value>http://s7teton.macromedia.com:8080/is/image/</value>
            </items>
            <items>
               <name>application_project_whatever</name>
               <value>false</value>
            </items>
            <items>
               <name>application_server_prefix_origin_test</name>
               <value>http://s7teton:8080/is/image</value>
            </items>
         </propertyArray>
      </items>
   </setArray>
</getPropertySetsReturn>
```
