---
description: 会社へのハンドルを使用してプロパティセットの種類とプロパティセットの種類の名前を取得します。 型に対するハンドルとプロパティ型を持つ型構造体を取得します。
solution: Experience Manager
title: getPropertySetType
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: ff9c3d24-577c-4a9c-8820-60c2a33773bc
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 11%

---

# getPropertySetType{#getpropertysettype}

会社へのハンドルを使用してプロパティセットの種類とプロパティセットの種類の名前を取得します。 型に対するハンドルとプロパティ型を持つ型構造体を取得します。

構文

## 許可されたユーザーの種類 {#section-2b291d32f95b4a3d854429124cbae24c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-c9a53400c44744668bd7915f72d2bf3d}

**入力(getPropertySetTypeParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | いいえ | 会社の取っ手。 プロパティセットタイプは複数の会社に属することができるので、オプションです。 |
| `*`name`*` | `xsd:string` | はい | プロパティセットの種類名。 |

**出力(getPropertySetTypeReturn)**

<table id="table_F2724F6B706C4F658AED99290E29F3E6"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:PropertySetType</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4">次を含むタイプ構造。 
    <ul id="ul_FC028882124D4CD6870A076CBFB80333"> 
     <li id="li_9F36539C51ED48EDBECCD6A07A4FDD4A">ハンドル。 </li> 
     <li id="li_6004406A0D1341648A714FF3C61E4004">型名。 </li> 
     <li id="li_29F6CA9D8B134ED3B10B6BDBB41BF607">プロパティタイプ。 </li> 
     <li id="li_A2354354541A4F1AB7234F65F2B61A40">タイプが複数のプロパティタイプを許可するかどうかを示す値。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-1b57199415e34a8fa449f864f8895b14}

このコードサンプルは、名前別にプロパティセットタイプを返します。

**リクエスト**

```java
<getPropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <name>Adobe.UserProperty</name>
</getPropertySetTypeParam>
```

**応答**

```java
<getPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <type>
      <typeHandle>pt|10801</typeHandle>
      <name>Adobe.UserProperty</name>
      <propertyType>UserProperty</propertyType>
      <allowMultiple>false</allowMultiple></type>
</getPropertySetTypeReturn>
```
