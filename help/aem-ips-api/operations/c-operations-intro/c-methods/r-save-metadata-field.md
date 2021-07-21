---
description: メタデータフィールドを作成または編集します。 新しいメタデータフィールドを作成するには、オプションのフィールドハンドルを省略します。
solution: Experience Manager
title: saveMetadataField
feature: Dynamic Media Classic,SDK/API，メタデータ
role: Developer,Admin
exl-id: 56a45324-5027-4375-a790-c965f682e4b9
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 8%

---

# saveMetadataField{#savemetadatafield}

メタデータフィールドを作成または編集します。 新しいメタデータフィールドを作成するには、オプションのフィールドハンドルを省略します。

>[!NOTE]
>
>このメソッドは非推奨です。

## 許可されたユーザーの種類 {#section-0c1cbde0863346f8a31b32fd06ab2926}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-ec6827d485a143f4a059a92b18e40f4e}

**入力(saveMetadataFieldParam)**

<table id="table_C944A44352F2475A89CE86F3DB1B648A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> パラメーター名 </th> 
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
   <td colname="col4"> 会社の取っ手。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> フィールドハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> メタデータの保存元となるアセットタイプの選択。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> フィールド名。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> メタデータフィールドタイプの選択。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> すべてのアセットのフィールドのデフォルト値。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> IPSシステム固有のメタデータを非表示または公開します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>値が設定されたときにメタデータフィールドが適用される（検証される）かどうかを示すbooleanフラグ。 </p> <p>trueに設定すると、<span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>に無効な値が設定された場合に、フォルトがスローされます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**出力(saveMetadataFieldReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`fieldHandle`*` | `xsd:string` | はい | 新しいメタデータフィールドのハンドル。 |

## 例 {#section-4441c26d1f41466ba972b43dd5189e89}

このコードサンプルを使用すると、 Asset TypeとMetadata Field Typesの文字列定数で制限される新しいメタデータフィールドが作成されます。 `fieldHandle`要素に有効なフィールドハンドル値がある場合、メタデータ値を変更し、リクエストで指定したのと同じフィールドハンドルを取得します。

**リクエスト**

```java
<ns1:saveMetadataFieldParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetType>Pdf</ns1:assetType>
   <ns1:name>Resolution</ns1:name>
   <ns1:fieldType>String</ns1:fieldType>
   <ns1:defaultValue>120</ns1:defaultValue>
</ns1:saveMetadataFieldParam>
```

**応答**

```java
<saveMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <fieldHandle>47|ALL|Resolution</fieldHandle>
</saveMetadataFieldReturn>
```
