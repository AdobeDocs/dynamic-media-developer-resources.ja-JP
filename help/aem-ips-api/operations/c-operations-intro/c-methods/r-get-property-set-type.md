---
description: 会社へのハンドルを使用してプロパティセットの種類とプロパティセットの種類の名前を取得します。 型に対するハンドルとプロパティ型を持つ型構造を取得します。
seo-description: 会社へのハンドルを使用してプロパティセットの種類とプロパティセットの種類の名前を取得します。 型に対するハンドルとプロパティ型を持つ型構造を取得します。
seo-title: getPropertySetType
solution: Experience Manager
title: getPropertySetType
topic: Dynamic Media Image Production System API
uuid: 203fa949-a81e-455a-a83e-576b6f65e3af
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 9%

---


# getPropertySetType{#getpropertysettype}

会社へのハンドルを使用してプロパティセットの種類とプロパティセットの種類の名前を取得します。 型に対するハンドルとプロパティ型を持つ型構造を取得します。

構文

## 認証済みユーザータイプ{#section-2b291d32f95b4a3d854429124cbae24c}

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
| `*`companyHandle`*` | `xsd:string` | いいえ | 会社へのハンドル。 プロパティセットタイプは複数の会社に属することがあるので、オプションです。 |
| `*`name`*` | `xsd:string` | はい | プロパティセットの種類の名前。 |

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
   <td colname="col2"> <span class="codeph"> タイプ：PropertySetType</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4">次の要素を含む型構造。 
    <ul id="ul_FC028882124D4CD6870A076CBFB80333"> 
     <li id="li_9F36539C51ED48EDBECCD6A07A4FDD4A">ハンドル。 </li> 
     <li id="li_6004406A0D1341648A714FF3C61E4004">タイプ名。 </li> 
     <li id="li_29F6CA9D8B134ED3B10B6BDBB41BF607">プロパティタイプ。 </li> 
     <li id="li_A2354354541A4F1AB7234F65F2B61A40">タイプで複数のプロパティタイプを許可するかどうかを示す値。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-1b57199415e34a8fa449f864f8895b14}

次のコードのサンプルを使用すると、名前別のプロパティセットタイプを返すことができます。

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

