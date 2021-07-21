---
description: 管理者は、コンテンツ管理システムとの連携やテンプレート操作のために、新しいメタデータフィールドを作成できます。 作成されたメタデータフィールドの例としては、キーワード、画像の作成者に関する情報、著作権者情報などがあります。
solution: Experience Manager
title: createMetadataField
feature: Dynamic Media Classic,SDK/API，メタデータ
role: Developer,Admin
exl-id: eac7fa54-ebe2-4f42-a478-d9a6fb54d1b6
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# createMetadataField{#createmetadatafield}

管理者は、コンテンツ管理システムとの連携やテンプレート操作のために、新しいメタデータフィールドを作成できます。 作成されたメタデータフィールドの例としては、キーワード、画像の作成者に関する情報、著作権者情報などがあります。

構文

## 許可されたユーザーの種類 {#section-2f61d79f8cac4692bfa53b95035ddd89}

* `IpsAdmin`

## パラメータ {#section-f8260bc8dd0a4570bc7f714f81ab975f}

**入力(createMetadataFieldParam)**

<table id="table_E5B249BBED3B4D2F9CEE2CCF27472D1B"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> メタデータフィールドが属する会社の名前。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> アセットタイプ. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 作成するメタデータフィールドの名前。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4">メタデータフィールドタイプ。 <p>メタデータフィールドタイプ定数は、使用可能なタイプを定義します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>作成するメタデータフィールドのデフォルト値（例：<span class="codeph"> Scene 7</span>）。 </p> <p>デフォルト値はタグフィールドタイプではサポートされていないので、省略する必要があります。 タグフィールドタイプに空でないデフォルト値を指定すると、フォルトが返されます。 </p> </td> 
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
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 選択したタグが指す共有列挙値のセットを作成できます。 </td> 
  </tr> 
 </tbody> 
</table>

**出力(createMetadataFieldReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`fieldHandle`*` | `xsd:string` | はい | 新しいメタデータフィールドへのハンドル。 |

## 例 {#section-ba66be30f36b4aeba1bc721b0b92fdfc}

このコードサンプルは、`createMetadataField`という名前の文字列タイプメタデータフィールドを作成します。 応答は、ハンドルを新しいメタデータフィールドに返します。

**リクエスト**

```java
<createMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetType>Image</assetType>
   <name>createMetadataField</name>
   <fieldType>String</fieldType>
   <initialTagValue>Fall</initialTagValue>
   <defaultValue>Default</defaultValue>
</createMetadataFieldParam>
```

**応答**

```java
<createMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <fieldHandle>m|21|IMAGE|createMetadataField</fieldHandle>
</createMetadataFieldReturn>
```
