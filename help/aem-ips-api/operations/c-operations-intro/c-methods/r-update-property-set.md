---
description: プロパティ配列を使用して、プロパティセットを更新します。
solution: Experience Manager
title: updatePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: bbe6a664-b6e1-4b46-867d-a134070b13da
TQID: 'https://experienceleague.adobe.com/-z-ZUe9SO-HG05Gv6XQAlREi2wrP93lH-HFEwNOxENI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 85
ht-degree: 11%

---

# updatePropertySet{#updatepropertyset}

プロパティ配列を使用して、プロパティセットを更新します。

構文

## 承認済みユーザータイプ {#section-116693bbfb5d44219e62bbb1ba19de96}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-98361b063e9c41e8b2f744fabc0e13ed}

**入力（updatePropertySetParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| setHandle | `xsd:string` | はい | プロパティセットへのハンドル。 |
| replaceProperties | `xsd:string` | いいえ | プロパティを置換するには、`true`に設定します。 |
| propertyArray | `types:PropertyArray` | はい | プロパティセットの更新されたプロパティの配列。 |

**出力（updatePropertySetReturn）**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-55d1c9dcd0174c6b9b52b4709f7c8bf9}

このコードのサンプルでは、プロパティ配列のプロパティでプロパティ セットを更新します。

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

