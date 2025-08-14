---
title: createMetadataField
description: これにより、管理者は、メタデータフィールドを作成してコンテンツ管理システムと連携させたり、テンプレート操作をしたりすることができます。 作成されるメタデータフィールドの例としては、キーワード、画像の作成者に関する情報、著作権保持者の情報などがあります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: eac7fa54-ebe2-4f42-a478-d9a6fb54d1b6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 6%

---

# createMetadataField{#createmetadatafield}

これにより、管理者は、メタデータフィールドを作成してコンテンツ管理システムと連携させたり、テンプレート操作をしたりすることができます。 作成されるメタデータフィールドの例としては、キーワード、画像の作成者に関する情報、著作権保持者の情報などがあります。

構文

## 許可されているユーザータイプ {#section-2f61d79f8cac4692bfa53b95035ddd89}

* `IpsAdmin`

## パラメーター {#section-f8260bc8dd0a4570bc7f714f81ab975f}

**入力（createMetadataFieldParam）**

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
   <td colname="col4"> アセットタイプ。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> の名前 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 作成するメタデータフィールドの名前。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4">メタデータフィールドタイプ。 <p>メタデータフィールドのタイプ定数は、使用可能なタイプを定義します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>作成するメタデータフィールドのデフォルト値（例：<span class="codeph"> Scene7</span>）。 </p> <p>デフォルト値はタグフィールドタイプではサポートされていないので、省略する必要があります。 タグフィールドタイプに空でないデフォルトが指定されている場合は、エラーが返されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> IPS システム固有のメタデータを表示または非表示にします。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>値の設定時にメタデータフィールドを適用（検証）するかどうかを示すブール値フラグ。 </p> <p>true に設定した場合、setAssetMetadata<span class="codeph"> /</span> batchSetAssetMetadata<span class="codeph"> に無効な値が設定されてい </span> とエラーが発生します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 選択したタグが指し示すことができる共有特定の値のセットを作成できます。 </td> 
  </tr> 
 </tbody> 
</table>

**出力（createMetadataFieldReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| fieldHandle | `xsd:string` | はい | 新しいメタデータフィールドへのハンドル。 |

## 例 {#section-ba66be30f36b4aeba1bc721b0b92fdfc}

このコードサンプルは、`createMetadataField` という文字列タイプのメタデータフィールドを作成します。 応答は、新しいメタデータフィールドへのハンドルを返します。

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
