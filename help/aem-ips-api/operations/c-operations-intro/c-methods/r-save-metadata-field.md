---
description: メタデータフィールドを作成または編集します。 新しいメタデータフィールドを作成するには、オプションのフィールドハンドルを省略します。
seo-description: メタデータフィールドを作成または編集します。 新しいメタデータフィールドを作成するには、オプションのフィールドハンドルを省略します。
seo-title: saveMetadataField
solution: Experience Manager
title: saveMetadataField
topic: Scene7 Image Production System API
uuid: ccd84366-732a-4caf-914d-3bc5fe499e7a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# saveMetadataField{#savemetadatafield}

メタデータフィールドを作成または編集します。 新しいメタデータフィールドを作成するには、オプションのフィールドハンドルを省略します。

>[!NOTE]
>
>このメソッドは非推奨です。

## 認証されたユーザータイプ {#section-0c1cbde0863346f8a31b32fd06ab2926}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-ec6827d485a143f4a059a92b18e40f4e}

**Input (saveMetadataFieldParam)**

<table id="table_C944A44352F2475A89CE86F3DB1B648A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> パラメータ名 </th> 
   <th colname="col2" class="entry"> 種類 </th> 
   <th colname="col3" class="entry"> 必須 </th> 
   <th colname="col4" class="entry"> 説明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 会社の取っ手。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> フィールドハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> メタデータの保存元のアセットタイプの選択。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 名 <span class="varname"> 前</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> フィールド名。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> メタデータフィールドタイプの選択。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> すべてのアセットのフィールドのデフォルト値。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> IPSシステム固有のメタデータを表示または非表示にします。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>値が設定されたときにメタデータフィールドが適用（検証）されるかどうかを示すbooleanフラグです。 </p> <p>trueに設定した場合、setAssetMetadata <span class="codeph"> /batchSetAssetMetadataに無効な値が設定された場合にエラーが発生し</span> ます<span class="codeph"></span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**出力(saveMetadataFieldReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`fieldHandle`*` | `xsd:string` | はい | 新しいメタデータフィールドのハンドル。 |

## 例 {#section-4441c26d1f41466ba972b43dd5189e89}

このコードサンプルを使用すると、アセットタイプとメタデータフィールドタイプの文字列定数で制約された新しいメタデータフィールドを作成できます。 要素に有効 `fieldHandle` なフィールドハンドル値がある場合は、メタデータ値を変更し、要求で指定したのと同じフィールドハンドルを取得します。

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

