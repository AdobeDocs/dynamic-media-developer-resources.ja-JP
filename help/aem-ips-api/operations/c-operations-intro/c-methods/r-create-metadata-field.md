---
title: createMetadataField
description: 管理者は、コンテンツ管理システムと連携したり、テンプレートを操作したりするためのメタデータフィールドを作成できます。 作成されたメタデータフィールドの例には、キーワード、画像の作成者に関する情報、著作権者情報などがあります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: eac7fa54-ebe2-4f42-a478-d9a6fb54d1b6
TQID: 'https://experienceleague.adobe.com/ktUyxtUtzmL7lHqtepLiu9qhFdk1r6FOgP2af1fUogM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 279
ht-degree: 6%

---

# createMetadataField{#createmetadatafield}

管理者は、コンテンツ管理システムと連携したり、テンプレートを操作したりするためのメタデータフィールドを作成できます。 作成されたメタデータフィールドの例には、キーワード、画像の作成者に関する情報、著作権者情報などがあります。

構文

## 承認済みユーザータイプ {#section-2f61d79f8cac4692bfa53b95035ddd89}

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
   <td colname="col4"> アセットタイプ： </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">名</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4"> 作成するメタデータフィールドの名前。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> はい </td> 
   <td colname="col4">メタデータフィールドタイプ： <p>メタデータフィールドタイプ定数は、使用可能なタイプを定義します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> <p>作成するメタデータフィールドのデフォルト値（例：<span class="codeph"> Scene 7</span>）。 </p> <p>タグフィールドタイプではデフォルト値はサポートされていないので、省略する必要があります。 タグフィールドタイプに空でないデフォルトが指定されている場合、障害が返されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">は非表示</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> IPS システム固有のメタデータを非表示または公開します。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname">は強制</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>値が設定されたときにメタデータフィールドが適用（検証）されるかどうかを示すブール値フラグ。 </p> <p>trueに設定すると、<span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>で不正な値が設定された場合、障害がスローされます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> いいえ </td> 
   <td colname="col4"> 選択したタグが指す共有固有の値のセットを作成できます。 </td> 
  </tr> 
 </tbody> 
</table>

**出力（createMetadataFieldReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| fieldHandle | `xsd:string` | はい | 新しいメタデータフィールドへのハンドル。 |

## 例 {#section-ba66be30f36b4aeba1bc721b0b92fdfc}

このコード サンプルでは、`createMetadataField`という文字列タイプのメタデータ フィールドを作成します。 応答は、ハンドルを新しいメタデータフィールドに返します。

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
