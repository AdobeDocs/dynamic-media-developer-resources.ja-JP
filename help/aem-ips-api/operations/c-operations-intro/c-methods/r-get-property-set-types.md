---
description: 指定した会社に関連付けられたプロパティセットの種類を取得します。会社が指定されていない場合は、グローバルプロパティセットの種類を取得します。
solution: Experience Manager
title: getPropertySetTypes
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7686d30b-e071-4950-8af1-4dd25312ce4b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 13%

---

# getPropertySetTypes{#getpropertysettypes}

指定した会社に関連付けられたプロパティセットの種類を取得します。会社が指定されていない場合は、グローバルプロパティセットの種類を取得します。

構文

## 認証済みユーザータイプ {#section-9c7c0d2cd2c94dfca3f96774b3a9a2c6}

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

**入力 (getPropertySetTypesParam)**

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4">プロパティセットタイプが関連付けられている会社へのハンドル。 <p>グローバルプロパティセットタイプを返す場合は、省略します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**出力 (getPropertySetTypesReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| typeArray | `types:PropertySetTypeArray` | はい | 指定した会社に関連付けられたプロパティセットタイプの配列、または会社が指定されていない場合はグローバルプロパティセットタイプ。 |

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
