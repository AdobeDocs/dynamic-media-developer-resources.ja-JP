---
description: 指定した会社に関連付けられたプロパティセットの種類を取得します。会社が指定されていない場合は、グローバルプロパティセットの種類を取得します。
seo-description: 指定した会社に関連付けられたプロパティセットの種類を取得します。会社が指定されていない場合は、グローバルプロパティセットの種類を取得します。
seo-title: getPropertySetTypes
solution: Experience Manager
title: getPropertySetTypes
topic: Scene7 Image Production System API
uuid: b707344d-5571-45eb-9e37-cf0894ee81a0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getPropertySetTypes{#getpropertysettypes}

指定した会社に関連付けられたプロパティセットの種類を取得します。会社が指定されていない場合は、グローバルプロパティセットの種類を取得します。

構文

## 認証されたユーザータイプ {#section-9c7c0d2cd2c94dfca3f96774b3a9a2c6}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-ac3ed9e036b54ea993f544046ff0e15d}

**入力(getPropertySetTypesParam)**

<table id="table_2590368FEEF04AD4B074412CBBA90F88"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名前 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 必須 </th> 
   <th colname="col4" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">プロパティセットの種類が関連付けられている会社のハンドル。 <p>グローバルプロパティセットタイプを返す場合は省略します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**出力(getPropertySetTypesReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`typeArray`*` | `types:PropertySetTypeArray` | はい | 指定した会社に関連付けられたプロパティセットタイプの配列、または会社が指定されていない場合はグローバルプロパティセットタイプ。 |

## 例 {#section-280c406a90864409856aee44d4069a52}

**リクエスト**

```java
<getPropertySetTypesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
  <companyHandle>c|1</companyHandle>
</getPropertySetTypesParam>
```

**応答**

```java
<getPropertySetTypesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
  <typeArray>
    <items>
      <typeHandle>pt|1</typeHandle>
      <companyHandle>c|1</companyHandle>
      <name>SavedSearch</name>
      <propertyType>UserCompanyProperty</propertyType>
      <alllowMultiple>true</alllowMultiple>
    </items>
    <items>
      <typeHandle>pt|2</typeHandle>
      <companyHandle>c|1</companyHandle>
      <name>CompanyMetadata</name>
      <propertyType>CompanyProperty</propertyType>
      <alllowMultiple>true</alllowMultiple>
    </items>
  </typeArray>
</getPropertySetTypesReturn>
```

