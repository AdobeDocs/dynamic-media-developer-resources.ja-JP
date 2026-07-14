---
description: 会社へのハンドルとプロパティセットタイプの名前を使用して、プロパティセットタイプを取得します。 型とプロパティタイプのハンドルを持つ型構造を取得します。
solution: Experience Manager
title: getPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ff9c3d24-577c-4a9c-8820-60c2a33773bc
TQID: 'https://experienceleague.adobe.com/E29wMANMzGAGzRtpw5GuV5dPYNHb0eSxOU4IBhiLYWQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 152
ht-degree: 9%

---

# getPropertySetType{#getpropertysettype}

会社へのハンドルとプロパティセットタイプの名前を使用して、プロパティセットタイプを取得します。 型とプロパティタイプのハンドルを持つ型構造を取得します。

構文

## 承認済みユーザータイプ {#section-2b291d32f95b4a3d854429124cbae24c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-c9a53400c44744668bd7915f72d2bf3d}

**入力（getPropertySetTypeParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | いいえ | 会社のハンドルです。 プロパティセットタイプは複数の会社に属することができるため、オプションです。 |
| name | `xsd:string` | はい | プロパティセットタイプ名。 |

**出力（getPropertySetTypeReturn）**

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
   <td colname="col2"> <span class="codeph"> タイプ：PropertySetType</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4">を含むタイプ構造： 
    <ul id="ul_FC028882124D4CD6870A076CBFB80333"> 
     <li id="li_9F36539C51ED48EDBECCD6A07A4FDD4A">ハンドル名： </li> 
     <li id="li_6004406A0D1341648A714FF3C61E4004">名前を入力します。 </li> 
     <li id="li_29F6CA9D8B134ED3B10B6BDBB41BF607">プロパティタイプ： </li> 
     <li id="li_A2354354541A4F1AB7234F65F2B61A40">型が複数のプロパティ型を許可するかどうかを示す値。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-1b57199415e34a8fa449f864f8895b14}

このコードサンプルは、名前でプロパティセットタイプを返します。

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

