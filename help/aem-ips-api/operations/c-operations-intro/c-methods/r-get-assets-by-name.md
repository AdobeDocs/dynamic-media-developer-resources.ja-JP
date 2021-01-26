---
description: アセット名の配列に基づいてアセットを返します。
seo-description: アセット名の配列に基づいてアセットを返します。
seo-title: getAssetsByName
solution: Experience Manager
title: getAssetsByName
topic: Dynamic Media Image Production System API
uuid: e86b3b16-ad93-4f70-9f59-b72395513c4c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 10%

---


# getAssetsByName{#getassetsbyname}

アセット名の配列に基づいてアセットを返します。

構文

## 認証済みユーザータイプ{#section-754790841ea242d5ae8bedd587d7730e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>ユーザーが読み取りアクセス権を持つアセットのみを返します。

## パラメータ {#section-f64e93c127b84a29aa3bf2fdd916cca9}

**入力(getAssetsByNameParam)**

<table id="table_CE7B503B0E074719A523B458DF3A7286"> 
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
   <td colname="col3"> はい </td> 
   <td colname="col4"> 会社へのハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 別のユーザーとしてアクセスを提供します。 管理者のみが使用できます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 特定のグループでフィルターするために使用します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nameArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 取得するアセット名の配列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 取得したアセットに対して許可されるアセットタイプの配列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 取得したアセットに対して除外されるアセットタイプの配列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 取得したアセットに対して許可されるアセットのサブタイプの配列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> strictSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p><span class="codeph"> true</span>および<span class="codeph"> assetSubTypeArray</span>が空でない場合、<span class="codeph"> assetSubTypeArray</span>にサブタイプを持つアセットのみが返されます。 </p> <p><span class="codeph"> false</span>の場合、サブタイプが定義されていないアセットが含まれます。 </p> <p>デフォルト値は<span class="codeph"> false</span>です。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 応答に含まれるフィールドとサブフィールドのリストが含まれます。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型：StringArray</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 応答から除外されたフィールドとサブフィールドのリストが含まれます。 </td> 
  </tr> 
 </tbody> 
</table>

**出力(getAssetsByNameReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`assetArray`*` | `types:AssetArray` | いいえ | フィルター条件に一致するアセットの配列。 |

## 例 {#section-3b7447398e574c88aeaf8ca159cc78dd}

このコードのサンプルを使用すると、2つのイメージタイプアセットを返すことができます。

**リクエスト**

```java
<getAssetsByNameParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <nameArray>
      <items>B010</items>
      <items>IMG_0103</items>
   </nameArray>
   <assetTypeArray>
      <items>Image</items>
   </assetTypeArray>
</getAssetsByNameParam>
```

**応答**

```java
<getAssetsByNameReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <assetArray>
      <items>
         <assetHandle>a|210</assetHandle>
         <type>Image</type>
         <name>B010</name>
         ...</items>
      <items>
         <assetHandle>a|189</assetHandle>
         <type>Image</type>
         <name>IMG_0103</name>
         ...
      </items>
   </assetArray>
</getAssetsByNameReturn>
```

