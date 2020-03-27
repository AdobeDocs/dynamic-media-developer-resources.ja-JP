---
description: フィールドのメタデータを更新します。
seo-description: フィールドのメタデータを更新します。
seo-title: updateMetadataField
solution: Experience Manager
title: updateMetadataField
topic: Scene7 Image Production System API
uuid: 8712b09b-b02a-4fb3-a0ed-084dc48a717a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# updateMetadataField{#updatemetadatafield}

フィールドのメタデータを更新します。

構文

## 認証されたユーザータイプ {#section-540e91823fee49a4920ca738f7bfeb99}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-69681ed1ddff437ca1c73f46fe835c96}

**Input (updateMetadataFieldParam)**

<table id="table_65D6EE6C402E4F01819822A855B6BB7F"> 
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
   <td colname="col4"> 会社の担当。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> メタデータフィールドハンドル。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 名 <span class="varname"> 前</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> メタデータフィールド名。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> メタデータフィールドの値。 </td> 
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
  <tr> 
   <td colname="col1"> <span class="codeph"> initialTagValue <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 選択したタグが参照できる共有列挙値のセットを作成できます。 </td> 
  </tr> 
 </tbody> 
</table>

**出力(updateMetadataFieldReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`fieldHandle`*` | `xsd:string` | はい | メタデータフィールドハンドル。 |

## 例 {#section-bb7d93ab6d914ddfa294e08983e589ee}

このコードサンプルの更新では、メタデータフィールドに新しい名前とデフォルト値を割り当てます。 応答は、更新されたフィールドにハンドルを返します。

**リクエスト**

```java
<updateMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <fieldHandle>m|21|IMAGE|createMetadataField</fieldHandle>
   <name>updateMetadataField</name>
   <defaultValue>Default</defaultValue>
</updateMetadataFieldParam>
```

**応答**

```java
<updateMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <fieldHandle>m|21|IMAGE|updateMetadataField</fieldHandle>
</updateMetadataFieldReturn>
```

